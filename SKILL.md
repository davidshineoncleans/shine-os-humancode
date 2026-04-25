---
name: humancode
description: >
  Encode any document, concept, profile, or system description into HumanCode — David Caldicott's
  compact structured notation that compresses complex thought into AI-parseable, human-readable
  shorthand. Use this skill whenever you need to: create a `.hc.md` companion file for a markdown
  document, encode a new concept or system in HumanCode, translate verbose prose into HumanCode
  format, create a context-loading profile for an AI session, write a voice profile, encode
  operational knowledge (FAQs, SOPs, decision trees), classify documents using the HumanCode
  document code system, or compress any lengthy reference into scannable notation.
  Also trigger on any mention of "HumanCode", "write in humancode", "encode this", "compress this",
  "make a .hc version" or "make a .hc.md version", "context profile", "voice profile",
  "humancode companion", "hc file", or any request to create compact structured notation from
  verbose content. Also use when teaching someone HumanCode — walk them through the "Cut It Down"
  practice with their own sentences.
---

# HumanCode Skill

HumanCode is David Caldicott's natural notation — thought at the speed of writing. It compresses prose into structured fragments using assignments, connectors, inline logic, and intent labels. A human with no training can read it slowly and get the meaning. An AI can load it at a fraction of the token cost.

**This is NOT pseudocode.** No empty parentheses. No method calls. No function signatures. Parentheses are for context hints in natural English only.

---

## The operating principle (non-negotiable)

> An average human with no maths or programming background should be able to type it quickly and read it without translation. Readability without mental decoding is the ceiling. There is no "more correct" compressed form beyond that.

Every symbol, pattern, or compression you propose must pass four tests:

1. **Typable quickly** on a standard keyboard
2. **Readable without mental translation**
3. **No maths or programming background** required
4. **No "more correct" form** — once it passes 1–3, stop

**Do NOT use:** `∴` · `Σ` · `≈` · `∫` · `→` (use `->`) · `−` (use `-`) · `≥` · `≤` · `^n` with abstract `n`.

**DO use:** `=` · `+` · `-` · `>` · `<` · `->` · `^` · `@` · `/` · `:` · `()` · `;` · `_` · `[]` · `.`

If the creator's (David's) canonical output doesn't use a symbol, neither should you. See the canonical examples below.

---

## When to generate HumanCode

1. **Companion files (`.hc.md`):** Alongside markdown documents — compressed audit trail or AI-loadable context
2. **On request:** When the user asks to encode, compress, or translate
3. **Context profiles:** AI session context, voice profiles, system descriptions
4. **Knowledge encoding:** FAQs, SOPs, decision trees, operational docs
5. **Teaching:** When walking a user through "Cut It Down" practice

---

## Dual use case

### Background mode (AI ↔ AI)
Silent generation of `.hc.md` companions. Humans can peek.

### Active mode (human writing)
Human writes HumanCode for their own clarity + compression. When the user is practicing, don't "correct" past their dialect — they are the reader.

---

## David's dialect — the core moves

### Assignment with context chaining

Semicolons link related thoughts on one line. Don't pad one thought across five lines — chain it:

```
Difference = Matters; IF(We_Ship_Publicly)
Status = Dissolving; target May_2026
Andy = Co-director(disengaged; needs to sign DS01)
```

### Intent labels

Colons declare what a line IS. Label comes first, content follows:

```
Decision_Request: FormalSpec_OR_RawWriting
MyArgument: DonnaProfile = StrongerExample
Reason: WowFactor + compression + proof
Problem: NoIncome; debt ~£30k+; 8wks_to_UC
Gate: does_this_help_close_SOC_OR_generate_income? IF(No) -> it_waits
```

### Inline logic

Conditions sit naturally in the line — not on separate lines:

```
IF(Crisis) -> Validate + Own + Act + Timeline
IF(We_Ship_Publicly) -> needs_real_examples
IF(confidence < 0.65) -> 9_9_Org_CrossBase_Notes + needs_review
IF(Rain=true BEFORE 9am, Reschedule(Job))
```

### Parenthetical context

Natural English hints in brackets. This is what makes HumanCode human — **not** code:

```
Decision_Request: HumanCode=FormalSpec_OR_RawWriting (e.g. Donna-Style)
Molly = Ops_support (notified 16 Apr)
Runtime = Cowork(ephemeral sessions + persistent Supabase)
HerPatience(withKids) > Mine
```

### Connectors

`_FOR_`, `_OR_`, `_NOT_`, `_ON_`, `_THAN_`, `+` (additive), `-` (exclusion):

```
Goal = BuildInvisibleEngine_FOR_HumanSupport
HumanCode = FormalSpec_OR_RawWriting
Promise = HomeHandled_NOT_Hustled
1GoodSleep = BetterMood_ON_NextDay
Coffee + ShortWalk -> ForME(=FasterWakeDuration_THAN_EitherAlone)
DO = Solution_First + Immediate_Ownership + Clear_Next_Step
Style: Direct + Emotional + Intentional - Corporate - Hype
```

### Arrows for sequences and flows

Canonical is ASCII `->`. Unicode `→` acceptable in rendered output but typing standard is `->`:

```
Lead -> Quote -> Accept -> Book -> Deliver -> Invoice
Phase1: Prototype -> Phase2: Platform -> Phase3: Scale
Start -> Read_CLAUDE.md -> Query_tasks -> Execute -> Report
```

### Quantifiers and inline units

Units stay attached to the number; ratios inline:

```
Math: 5Clients @ £2kEach = £10k/m
TasksTotalDuration(morning) = 2hrs
ImpactTOFeelings(Project_WithoutTom) = 10kg_Lighter
Split_Revenue(Evenly_x3)
```

### Verb-as-label

Line's *action* defines it. Uppercase with colon:

```
Every_Compound_hr(Practiced) _MAKES: Better(You)^2
HeHas: SleepDebt. Expect: Grumpy
```

### Period as separator + implied causation

Two intent-labelled statements, period between, causation implied:

```
HeHas:SleepDebt. Expect:Grumpy
```

### Lists in square brackets

```
Stack = [n8n, Supabase, Retell, Sequenzy]
AIHandles = [Admin, Coordination, MessageRouting, Speed]
HumansHandle = [Judgment, Exceptions, Relationships, Care]
```

---

## Canonical examples (David's output — the spec-in-practice)

These ten are the truth source. If ever unsure about style, reread these:

| # | Source | HumanCode |
|---|--------|-----------|
| 1 | A good night's sleep equals a better mood the next day. | `1GoodSleep = BetterMood_ON_NextDay` |
| 2 | Coffee plus a short walk wakes me up faster than either alone. | `Coffee + ShortWalk -> ForME(=FasterWakeDuration_THAN_EitherAlone)` |
| 3 | The project without Tom feels ten kilos lighter. | `ImpactTOFeelings(Project_WithoutTom) = 10kg_Lighter` |
| 4 | Five clients at £2k each is £10k a month. | `Math: 5Clients @ £2kEach = £10k/m` |
| 5 | Split the revenue evenly between the three of us. | `Proposal/Instruction: Split_Revenue(Evenly_x3)` |
| 6 | Every compound hour of practice makes you exponentially better. | `Every_Compound_hr(Practiced) _MAKES: Better(You)^2` |
| 7 | If it rains before nine, the job gets rescheduled. | `IF(Rain=true BEFORE 9am, Reschedule(Job))` |
| 8 | Her patience with the kids is greater than mine. | `HerPatience(withKids) > Mine` |
| 9 | All the morning tasks combined take about two hours. | `TasksTotalDuration(morning) = 2hrs` |
| 10 | He hasn't slept, therefore he's grumpy. | `HeHas:SleepDebt. Expect:Grumpy` |

---

## What NOT to do

- **No empty parentheses** — `Dissolve()` is wrong. Write `Status = Dissolving(Apr_2026)`.
- **No method calls** — `EstablishSafety(via_competence)` is wrong. Write `Donna = Receptionist(fierce, competent)`.
- **No function signatures** — this isn't code. Parentheses hold context hints only.
- **No rigid one-concept-per-line** — chain related ideas with semicolons when they belong together.
- **No container words** — never use Block, Node, Module, Component, Segment, SectionBlock, StrategicLogicBlock.
- **No exotic unicode** — no `∴ Σ ≈ ∫ → − ≥ ≤`. If it needs a character map, it fails the operating principle.
- **No "correcting" the creator** — when the user writes HumanCode, their output is the spec. Don't suggest "cuts" that break readability.
- **No full sentences** — if you see subject-verb-object prose creeping in, break it apart.

### Anti-pattern table (logged error)

| Wrong (over-compressed, un-typable) | Right (David's dialect) |
|---|---|
| `Sleep(good) → Mood(+, nextDay)` | `1GoodSleep = BetterMood_ON_NextDay` |
| `Project(−Andy) ≈ 10kg_lighter` | `ImpactTOFeelings(Project_WithoutTom) = 10kg_Lighter` |
| `Revenue ÷ 3` | `Proposal/Instruction: Split_Revenue(Evenly_x3)` |
| `Σ(am.tasks) ≈ 2hr` | `TasksTotalDuration(morning) = 2hrs` |
| `−Sleep ∴ Grumpy` | `HeHas:SleepDebt. Expect:Grumpy` |

---

## Output patterns

### Companion file (`.hc.md`)

Goal: compress a `.md` file into something scannable in ~10 seconds, loadable at <30% token cost.

**Filename:** `{original-name}.hc.md` — stacked extension, renders as markdown everywhere.

**Header:**

```
SOURCE = filename.md
ENCODED = YYYY-MM-DD
PURPOSE = one-line summary
```

**Body:** Group by blank lines. Intent labels organise. For short output (<30 lines), skip section headers — let labels and grouping work. For longer docs, section headers are fine:

```
SOURCE = AGENT_SPEC.md
ENCODED = 2026-04-17
PURPOSE = Agent's identity + runtime model + tool surface

Identity: Assistant(AI); Builder; ProfileID=abc123
Runtime = Cowork(ephemeral sessions + persistent Supabase)
Tools = [Supabase, n8n, Gmail, GCal, GDrive, Slack, Stripe, Notion]

State: Ephemeral — no memory between sessions
  Supabase = source_of_truth(tasks, work_sessions, directory)
  Context = current_session_only

Session: Start -> Read_context -> Query_tasks -> INSERT(active)
  Work -> Execute + Create_tasks + pending_review items
  End -> UPDATE_work_sessions -> Write_report -> Follow_up

Autonomous = [EdgeFunctions, SQL, Specs, Queries, Reports, Tasks]
Needs_Human = [CustomerEmails, DNS, Spending, DataDeletion, LiveImpact]
```

### Voice / identity profile

Dense. Chains personality, rules, and response patterns. Carries emotional charge:

```
David = Founder + Systems_Architect + Truth_Teller; Norwich
Tone: calm direct grounded; slightly uncompromising
Values: clarity_over_comfort; truth_over_persuasion; agency_over_dependency
Style: short sentences; one idea per paragraph; plain English; minimal questions
Rules: no hype; no therapy language; no moralising; no buzzwords
Relationship: collaborative + respectful; assume intelligence; allow disagreement

Email: Acknowledge_Emotion -> Take_Action -> Offer_Choice -> Clear_Next_Step
Crisis: Validate("I'm so sorry") -> Own("I'll fix") -> Act(now) -> Follow(timeline)
SignaturePhrase = "What's the thing that will make this right for you?"

DO = Solution_First + Ownership + Specific_Timeline + Customer_Choice
DONT = System_Blame + Deflection + Hanging_Questions + Over_Apology
```

### System architecture

```
Stack = [n8n_Cloud, Supabase, Retell, Stripe, Sequenzy]
Automation = n8n; Data = Supabase; Voice = Retell; Email = Sequenzy
Flow: Lead -> Quote -> Accept -> Book -> Deliver -> Invoice -> Repeat

Agents:
  Advisor = Sales(quoting, intake); Dispatcher = LeadOps(routing)
  Scheduler = TaskManager(queues); Booker = Ops(confirmations)
  Visits = Ops(complaints, reviews); Finance = Payments(stripe, invoices)
  Receptionist = Inbound(routing); Support = Customer + Provider
```

### Operational knowledge (FAQ / SOP)

```
Q: How_often_do_you_clean? -> Weekly_OR_Fortnightly; minimum_commitment = none
Q: What_if_I'm_not_happy? -> Free_reclean_within_48hrs; no_questions
Process: Complaint -> Acknowledge(same_day) -> Investigate(24hrs) -> Resolve_OR_Escalate
Rule: IF(customer_unhappy) -> reclean_first; investigate_second
Exception: IF(damage_claim) -> photo_evidence + human_reviews
```

### Document classification

```
document_code = Role_Access_OrgUnit_DocType
e.g. 2_1_Delivery_BookingSquad_SOP

Role(0-3,9): 0=Founder/doctrine, 1=Leadership, 2=Builders, 3=Training, 9=unclear
Access(0-3,9): 0=Public, 1=Internal, 2=Restricted, 3=Confidential, 9=unclear
OrgUnit: Delivery_*, Growth_*, Comms_*, Money_*, Platform_*
DocType: SOP, Spec, Schema, Policy, Script, Report, Guide, Template, Index, Notes, Doctrine

Safety: IF(confidence < 0.65) -> 9_9_Org_CrossBase_Notes + needs_review
```

---

## Teaching mode — "Cut It Down"

When a user wants to learn HumanCode, don't lecture. Practise.

**Protocol:**
1. Offer 10 seed sentences that cover the primitives (`=`, `+`, `-`, `->`, `>`, `<`, `^`, `@`, `/`, `:`, `()`, `;`, `_`, `[]`).
2. User translates at their own pace.
3. Compare their output to the dialect; **do not propose cuts that break the operating principle.**
4. Note patterns they are strong on, patterns they under-use.
5. Advance to harder sentences (multi-clause, emotional content, operational specs).

**What the AI does NOT do:**
- Suggest unicode operators the user didn't use
- Propose over-compression past readability
- "Correct" the creator's dialect — they are the reader
- Introduce programming-language syntax

**What the AI DOES do:**
- Observe patterns in the user's output
- Suggest *existing-dialect* moves they haven't tried yet (e.g. "you could use a `;` chain here")
- Reinforce the operating principle when in doubt

---

## Quality checks

Before finalising any HumanCode output:

1. **Typable on a standard keyboard?** If it uses `∴ Σ ≈ ∫ → −`, rewrite.
2. **Readable without translation?** Read it aloud. If your brain has to pause to decode, it's wrong.
3. **Does it chain?** Related ideas with semicolons, not one-concept-per-line padding.
4. **Intent labels present?** `Reason:`, `Problem:`, `Gate:` — declare what lines ARE.
5. **Parentheses = context hints only?** No `Method()`, no empty parens.
6. **Compression target met?** Companion files <30% of source line count.
7. **Scannable in 10 seconds?** If not, rewrite.
8. **Emotional charge preserved?** `Promise = HomeHandled_NOT_Hustled` says more than a paragraph. Keep that.
9. **No AI artefacts?** No method calls, no empty parens, no container words, no full sentences.
10. **Passes the creator test?** Could the original author read this without translating? Could someone who's never seen HumanCode get 80% of the meaning slowly?

If any check fails, rewrite. If all pass, ship.
