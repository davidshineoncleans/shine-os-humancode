SOURCE = customer-onboarding-system-v2.md
ENCODED = 2026-04-24
PURPOSE = onboarding system architecture: sources, flow, agents, data contracts, failure modes

System = CustomerOnboarding_v2; Owner=GrowthOps; Status=Live(since_2026-02)

Stack = [Stripe, Postgres, n8n, Sendgrid, Slack, Segment]
Entry_Points = [website_signup_form, stripe_checkout_success_webhook, sales_team_manual_entry]
Exit_States = [Activated, Churned_Within_30d, StuckInProgress_Flagged]

Flow:
  Entry -> CreateRecord(customers) -> EnrichFromSegment -> AssignSuccessOwner -> TriggerEmail1
  Email1(Welcome) -> Wait(24hr) -> CheckLogin
    IF(HasLoggedIn) -> TriggerEmail2(FirstWinChecklist)
    IF(NotLoggedIn) -> TriggerNudgeEmail_AND_SlackAlert(successOwner)
  Email2 -> Wait(72hr) -> CheckFirstAction
    IF(FirstActionCompleted) -> MarkActivated + LogToAnalytics
    IF(NotCompleted) -> ScheduleCall(successOwner); AddTo(StuckList)

Data_Contracts:
  customers(id, email, created_at, plan, enriched_fields, success_owner_id, activation_status)
  events(id, customer_id, event_type, payload_json, created_at)
  emails_sent(id, customer_id, template_key, sent_at, opened_at, clicked_at)

Agents:
  Intake = n8n_workflow(stripe_webhook -> enrich -> insert)
  Nudger = n8n_workflow(cron_hourly + check_activation_state)
  SlackNotifier = n8n_workflow(sends_alerts_to #customer-success)

Failure_Modes:
  StripeWebhookTimeout -> Retries=3; IF(all_fail) -> DeadLetterQueue + PagerDuty(growth-ops)
  SendgridBounce -> LogBounce + RemoveFromSequence + SlackAlert(successOwner)
  SegmentEnrichmentMiss -> SkipEnrichment + ContinueFlow + FlagForReview

Metrics:
  North_Star = 7d_Activation_Rate (target 65%); current ~58%
  Guardrail = DeliverabilityRate (target >99%); current 99.2%
  Diagnostic = [TimeToFirstLogin, TimeToFirstAction, NudgeOpen_vs_Base]

Owners:
  OnCall = successOwner_by_segment (enterprise -> Riley; SMB -> Taylor; self-serve -> nobody)
  CodeOwner = GrowthEngineering; escalation = head_of_growth

Runbook: IF(SystemDown) -> check_n8n_status_page + stripe_webhook_history + segment_delivery_logs
  IF(enrichment_broken) -> fallback_flow_skips_enrichment_safely; alert before 50 records stack up
