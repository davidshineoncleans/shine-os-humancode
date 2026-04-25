# Canonical Examples

**The spec-in-practice. Authored by the creator (David Caldicott). This is the truth source for what HumanCode is.**

When [`REFERENCE.md`](./REFERENCE.md) and [`SKILL.md`](./SKILL.md) describe HumanCode, they describe the notation the creator uses here. If ever in conflict, these examples win. The creator's output is the canonical reference, not AI-derived "cuts."

---

## Operating constraint

Any proposed symbol, pattern, or compression must pass all four tests:

1. **Typable quickly** by an average human on a standard keyboard
2. **Readable without translation** — no mental decode step
3. **No maths or programming background** required
4. **No "more correct" form** — once it passes 1–3, it's done

Symbols that fail (examples): `∴`, `Σ`, `≈`, `∫`, `−` (unicode minus), `→` (prefer `->`), `≥`, `≤`, `^n` with abstract `n`.

Symbols that pass: `=`, `+`, `-`, `>`, `<`, `->`, `^`, `@`, `/`, `:`, `(`, `)`, `;`, `_`, `[`, `]`.

---

## The 10 — source → HumanCode (Round 1)

Live-practice session, 2026-04-24. The creator translating after not writing HumanCode for a while.

### 1. Assignment with temporal modifier

Source:

> A good night's sleep equals a better mood the next day.

HumanCode:

```
1GoodSleep=BetterMood_ON_NextDay
```

Moves demonstrated: `=` assignment; PascalCase concept-binding; `_ON_` as ALL-CAPS preposition; leading `1` as quantifier.

---

### 2. Combination with effect and comparison

Source:

> Coffee plus a short walk wakes me up faster than either alone.

HumanCode:

```
Coffee+ShortWalk->ForME(=FasterWakeDuration_THAN_EitherAlone)
```

Moves demonstrated: `+` additive; `->` effect/leads-to; parenthetical sub-clause; `_THAN_` preposition in caps.

---

### 3. Contextual weight of a relationship change

Source:

> The project without Tom feels ten kilos lighter.

HumanCode:

```
ImpactTOFeelings(Project_WithoutTom)= 10kg_Lighter
```

Moves demonstrated: function-call framing for subjective impact; embedded prepositional compound `_WithoutX`; unit-preserving literal `10kg_Lighter`.

---

### 4. Math with scope label

Source:

> Five clients at two thousand pounds each is ten thousand pounds a month.

HumanCode:

```
Math: 5Clients@£2kEach=£10k/m
```

Moves demonstrated: `Math:` intent label; `@` for rate-of; `/m` for per-month; compressed currency.

---

### 5. Instruction with even-split

Source:

> Split the revenue evenly between the three of us.

HumanCode:

```
Proposal/Instruction: Split_Revenue(Evenly_x3)
```

Moves demonstrated: dual-intent label `Proposal/Instruction:`; function-style carrying natural English modifier `Evenly_x3`; `x3` as multiplier.

---

### 6. Compounding with power notation

Source:

> Every compound hour of practice makes you exponentially better.

HumanCode:

```
Every_Compound_hr(Practiced)_MAKES: Better(You)^2
```

Moves demonstrated: underscore-bound subject phrase; parenthetical modifier `(Practiced)`; `_MAKES:` as verb-label; `^2` used colloquially for "exponentially" (not literal squared).

---

### 7. Conditional with time constraint

Source:

> If it rains before nine, the job gets rescheduled.

HumanCode:

```
IF(Rain=true BEFORE 9am, Reschedule(Job))
```

Moves demonstrated: Pythonic `IF(condition, action)`; `BEFORE` as time operator; boolean `=true`.

---

### 8. Direct comparison

Source:

> Her patience with the kids is greater than mine.

HumanCode:

```
HerPatience(withKids) > Mine
```

Moves demonstrated: `>` comparison; parenthetical scope `(withKids)`; implicit subject-echo on the right side.

---

### 9. Aggregate duration

Source:

> All the morning tasks combined take about two hours.

HumanCode:

```
TasksTotalDuration(morning)=2hrs
```

Moves demonstrated: variable-style naming; scope in parens; direct `=` with unit.

---

### 10. State → consequence pair

Source:

> He hasn't slept, therefore he's grumpy.

HumanCode:

```
HeHas:SleepDebt. Expect:Grumpy
```

Moves demonstrated: two chained intent-labelled statements `State. Expectation.`; `HeHas:` as possession label; `Expect:` as consequence label.

---

## Principles extracted from the creator's output

These are observations of what the creator actually does, not prescriptions:

- **PascalCase concept-binding.** `GoodSleep`, `BetterMood`, `HerPatience`. One idea = one token-like word.
- **Underscore as preposition-glue.** `_ON_`, `_THAN_`, `_WithoutTom`, `_Lighter`. Prepositions in ALL_CAPS_ between ideas; lower_case for modifiers.
- **ASCII arrows over unicode.** `->` not `→`. Typability trumps visual purity.
- **Intent labels with colons.** `Math:`, `Proposal:`, `Instruction:`, `HeHas:`, `Expect:`. Declares what the line is.
- **Parentheses for scope or modifier, never empty, never method-call.** `Project_WithoutTom`, `HerPatience(withKids)`, `Better(You)`.
- **Inline quantifiers.** `1`, `x3`, `5`, `@`, `/m`, `10kg`, `£2k`. Units stay attached.
- **`^` for colloquial "exponentially / a lot".** Not literal mathematical exponent.
- **Readable sentences survive.** The goal is compression, not cryptography.

---

## Anti-patterns (what HumanCode is NOT)

Logged from a real session error where the AI over-compressed:

| Wrong (AI overreach) | Right (creator's dialect) |
|---|---|
| `Sleep(good) → Mood(+, nextDay)` | `1GoodSleep=BetterMood_ON_NextDay` |
| `Project(−Andy) ≈ 10kg_lighter` | `ImpactTOFeelings(Project_WithoutTom)= 10kg_Lighter` |
| `Revenue ÷ 3` | `Proposal/Instruction: Split_Revenue(Evenly_x3)` |
| `Σ(am.tasks) ≈ 2hr` | `TasksTotalDuration(morning)=2hrs` |
| `−Sleep ∴ Grumpy` | `HeHas:SleepDebt. Expect:Grumpy` |

The wrong column is tighter. It's also unreadable to the target user and un-typable on a standard keyboard. That disqualifies it.

---

## Round 2 — harder sentences (2026-04-24)

Second practice set. Same session, same day. Multi-clause, operational, emotional, meta-referential. The creator introduced several new moves organically — these are logged below the table as "Extensions observed in practice."

### 11. Conditional with compound action

Source:

> If the payment doesn't clear by Friday, I'll switch Stripe off and move them onto a weekly standing order instead.

HumanCode:

```
If(Payment=NOTClearBYFriday), I_Will:DisableStripe&_Move2WeeklyStandingOrder
```

Moves: `NOT` as prefix negation; `BY` as temporal operator (cousin of `BEFORE`); `I_Will:` first-person intent label; `&_` as chained-action joiner; `2` as text-speak "to".

---

### 12. Role-chain parallelism with summary arrow

Source:

> Marshall routes the lead, Daniel books the job, Kelly checks it's done properly, and Frankie invoices — that's the entire lifecycle in four hands.

HumanCode:

```
MarshallRoutesLead, DanielBooksLead, KellyChecks, FrankieInvoices. => Lifecycle_IN_4Hands
```

Moves: comma-separated role+verb+object parallelism; period terminator on the list; `=>` summary arrow (distinct from `->` flow); `_IN_` preposition; number-prefix count (`4Hands`).

---

### 13. Trend comparison with contrast

Source:

> Revenue in April was fifty percent down on February, but costs dropped by a third, so the squeeze actually eased slightly.

HumanCode:

```
AprilRevenue = 50% Down_On_Feb. BUT: CostsDown_by_1/3__MEANING: SqueezeHasEased...Slightly
```

Moves: `BUT:` contrastive intent label; `_by_` quantified-change preposition; inline fraction `1/3`; `__MEANING:` double-underscore causal intent label (explicit "therefore"); ellipsis `...Slightly` for partial / not-fully.

---

### 14. Capacity statement with gating condition

Source:

> I can't build the new agent this week because I'm prepping the dissolution pack and anything that isn't income or DS01 waits.

HumanCode:

```
NoCapabilityToBuild_ThisWeek Reason=PreppingDissolutionPack_AND_OnlyWorkIF(Income OR DS01)
```

Moves: `Reason=` inline intent label (variant of `Reason:`); nested `OnlyWorkIF(...)` with uppercase `OR` inside parens.

---

### 15. Parallel WHEN clauses for comparison

Source:

> When she's tired she gets short with the kids, when I'm tired I go quiet — neither is great, but hers is louder.

HumanCode:

```
WHEN: She=Tired, SheGets:ShortWithKids. WHEN: He=Tired, HeGoes:Quiet. Neither=Great. Hers=Louder
```

Moves: `WHEN:` temporal intent label; mirrored structure for comparison; period-separator chain of four statements; comparative without explicit second operand (`Hers=Louder` implies "than his").

---

### 16. Meta-statement (HumanCode describing HumanCode)

Source:

> The point of HumanCode isn't compression — compression is the evidence; the point is that you can't hide a fuzzy thought behind good grammar.

HumanCode:

```
HumanCode_POINT=NotCompression Compression=EvidenceTHAT(YouCan'tHideFuzzyThoughtsBehindGoodGrammar)
```

Moves: `_POINT=` underscore-bound property assignment; `Not` as prefix negation on a concept; `EvidenceTHAT(...)` — uppercase-inside-word flags the clause-introducer.

---

### 17. Inequality with condition attached

Source:

> Three hours of deep work beats eight hours of shallow work every time, as long as the deep work is on the right thing.

HumanCode:

```
3hrsDeepWork > 8hrsShallowWork_EveryTime Condition=DeepWorkOnRightThing
```

Moves: unit+adjective+noun compound (`3hrsDeepWork`); `_EveryTime` modifier suffix; `Condition=` inline intent label.

---

### 18. Time-bound policy with judgement fallback

Source:

> If a customer complains within 48 hours we reclean free, no questions; after that it's a judgement call between Kelly and me.

HumanCode:

```
If(CustomerComplaint <=48hrsOld) Then_WE_ReCleanFree NoQuestions; OnlyJudgementCall(kellyORdavid)
```

Moves: `If(...) Then_WE_` explicit consequence; `<=48hrsOld` ASCII-safe comparison with unit; semicolon chain; lowercase subjects joined by caps `OR` inside parens.

---

### 19. Compound acceptance condition

Source:

> I'll take the consultancy gig only if it pays enough to cover the mortgage arrears AND doesn't pull me off the public release.

HumanCode:

```
ConsultancyGig_Accept_IF: Pay>Arrears & DoesNotBlock_PublicRelease
```

Moves: `_Accept_IF:` compound condition-as-label; `&` as AND conjunction (typable cousin of `+`); `DoesNotBlock_` as negated-action prefix.

---

### 20. Identity-under-loss narrative

Source:

> The company is dissolving but the IP isn't — the agents, the frameworks, the notation all survive as my portfolio, and that's the quiet win underneath the loss.

HumanCode:

```
CompanyDissolving_ButNot_IP. Agents,Frameworks,Notation_ALL_SurviveAs:Portfolio. => QuietWIN_Under_TheLoss
```

Moves: `_ButNot_` inline contrast preposition; comma-list inside subject; `_ALL_` quantifier modifier; `SurviveAs:` verb-as-label; `=>` summary arrow; `_Under_` positional preposition.

---

## Extensions observed in practice

These moves appeared in the creator's Round 2 output. They are now part of the dialect.

| Move | Meaning | Example |
|---|---|---|
| `=>` | summary / "resolves to" (distinct from `->` flow) | `...=> Lifecycle_IN_4Hands` |
| `&` | AND conjunction (typable cousin of `+`) | `Pay>Arrears & DoesNotBlock_X` |
| `&_` | chained-action joiner | `DisableStripe&_Move2StandingOrder` |
| `BUT:` | contrastive intent label | `. BUT: CostsDown_by_1/3` |
| `WHEN:` | temporal intent label (parallel to `IF:`) | `WHEN: She=Tired, SheGets:ShortWithKids` |
| `_MEANING:` | causal / "therefore" (explicit) | `...__MEANING: SqueezeHasEased` |
| `Then_WE_` | explicit consequence inside `IF(...)` | `If(X) Then_WE_ReCleanFree` |
| `<=`, `>=` | ASCII-safe comparisons | `<=48hrsOld` |
| `NOT` prefix | negation on a variable | `Payment=NOTClearBYFriday` |
| `Not` prefix | negation on a concept | `HumanCode_POINT=NotCompression` |
| Caps-inside-word | signals a connective inside a compound | `byFriday`, `EvidenceTHAT`, `kellyORdavid` |
| `2` / `4` | text-speak "to" / "four" | `Move2StandingOrder`, `4Hands` |
| Unit-adjective compound | `3hrsDeepWork` | — |
| `_by_` | quantified-change preposition | `CostsDown_by_1/3` |
| `1/3`, `50%` | inline fractions and percentages | `50% Down_On_Feb` |
| `...Slightly` | ellipsis for partial / not-fully | `Eased...Slightly` |
| `_IN_`, `_ON_`, `_THAN_`, `_Under_`, `_ButNot_`, `_AND_`, `_OR_` | ALL_CAPS prepositions | — |
| `Condition=`, `Reason=`, `_POINT=` | inline intent-label variants of `Condition:`, `Reason:`, `POINT:` | — |

---

## How to use this file

- When in doubt about style, read these examples first.
- When reviewing AI-generated HumanCode (`.hc.md` files, skill output), grade against these patterns.
- When teaching HumanCode publicly, use these as the worked examples — they're the real thing.
- When extending the notation, a new move must appear in a creator's natural output before it enters the reference.
