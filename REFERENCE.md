# HumanCode — Master Reference

> **Created by David Caldicott.** A natural shorthand for compressing complex thought into scannable, AI-parseable notation. Not designed at a desk — emerged from how David actually writes when he's thinking fast and capturing meaning.
>
> **Origin:** David's natural notation style, formalised across personal working docs (Jun 2025 – Feb 2026), recalibrated to the source dialect Apr 2026.

---

## The operating principle (governs everything else)

> An average human with no maths or programming background should be able to type it quickly and read it without translation. Readability without mental decoding is the ceiling. There is no "more correct" compressed form beyond that.

Four tests every move must pass:

1. **Typable quickly** on a standard keyboard
2. **Readable without mental translation**
3. **No maths or programming background** required
4. **No "more correct" form** — once it passes 1–3, it's done

---

## What HumanCode Is

HumanCode is thought at the speed of writing. It's what happens when someone who thinks in systems writes notes for themselves — and it turns out AI can parse it perfectly.

It compresses prose into structured fragments using assignments, connectors, inline logic, and intent labels. A human with no training can read it slowly and get the meaning. An AI can load it at a fraction of the token cost of the original prose.

```
Origin = David's_Natural_Notation; formalised_later_by_AI
CoreInsight: Human_shorthand + AI_parseability = massive_compression_WITHOUT_meaning_loss
```

---

## Symbol set

**Passes the operating-principle test (use these):**

```
=    assignment / equivalence
+    additive / combination
-    subtraction / exclusion
>    greater than
<    less than
->   leads-to / causes / flow
^    raised / exponential (colloquial)
@    at rate of
/    per (as in /m = per month)
:    intent label ("this line IS X")
()   scope / context hint (natural English only)
;    chain related thoughts on one line
_    bind preposition or modifier
[]   list
.    sentence separator (in prose-style chains)
```

**Fails the test (do not use):**

`∴` · `Σ` · `≈` · `∫` · `−` (unicode minus) · `→` (prefer `->`) · `≥` · `≤` · `^n` with abstract `n` · anything requiring a special character map to type.

---

## Dual use case

HumanCode runs in two modes. Both share the same notation.

### Background mode (AI ↔ AI)

AI generates `.hc.md` companion files alongside markdown documents, silently. Humans can peek if curious. Used for:
- Session report companions (compressed audit trail)
- Knowledge base compressions (AI context loading)
- Voice / identity profiles for agents
- System / architecture specs

### Active mode (human in the loop)

Humans write HumanCode themselves to:
- Compress prompts for AI (fit more context; cheaper; faster)
- Clarify their own thinking (force the bones of a thought to surface)
- Take scannable notes that reread in ten seconds
- Communicate dense specs to other humans who know the notation

The switch between modes is seamless. AI output in HumanCode reads the same as David's handwritten HumanCode.

---

## File extension convention

**Public standard: `.hc.md`** (stacked extension).

- Renders as markdown in every tool (GitHub, Obsidian preview, VS Code, macOS Quick Look)
- Keeps the HumanCode signal in the filename
- Fully backward compatible with markdown tooling

Bare `.md` is fine too — `.hc.md` is just the explicit signal.

---

## David's Dialect — The Core Moves

This is how David actually writes HumanCode. Everything else derives from this.

### Characteristics

Dense. Chains ideas with semicolons. Uses colons as intent labels. Drops natural English into parentheses as context hints. Packs multiple related ideas onto one line when they belong together. Doesn't explain itself — if you need an explanation, read it slower.

### Real Example

Source prose:

> "The difference matters if we're going to ship this publicly. We need to decide: is HumanCode the formal spec from the Instruction Set, or is the rawer thing you actually write — the Donna-style notation? I'd argue the Donna profile is the stronger example for a Reddit post. It's the one that makes people go 'wait, I can read that and I've never seen this notation before.' The 76% compression stat is real, but the Donna profile is the proof that the notation carries meaning, personality, and operational logic without a single sentence."

David's HumanCode:

```
Difference = Matters; IF(We_Ship_Publicly)
Decision_Request: HumanCode=FormalSpec_OR_RawWriting (e.g. Donna-Style)

MyArgument: DonnaProfile=StrongerExample_FOR_Reddit
Reason: WowFactor + 76%_compression + proof of complex meaning.
```

### Assignment with context chaining

Semicolons link related thoughts:

```
Difference = Matters; IF(We_Ship_Publicly)
Status = Active; target Q3_2026
Andy = Co-director(disengaged; needs to sign DS01)
```

### Intent labels

Colons declare what a line IS:

```
Decision_Request: FormalSpec_OR_RawWriting
MyArgument: DonnaProfile = StrongerExample
Reason: WowFactor + compression + proof
Problem: CashFlow_tight; runway ~8wks; need_revenue_now
Gate: does_this_help_ship_OR_generate_income? IF(No) -> it_waits
```

### Inline logic

Conditions sit naturally in the line, not on separate lines:

```
IF(Crisis) -> Validate + Own + Act + Timeline
IF(We_Ship_Publicly) -> needs_real_examples
IF(Rain=true BEFORE 9am, Reschedule(Job))
```

### Parenthetical context

Natural English hints in brackets. This is what makes HumanCode human — **not** code:

```
Decision_Request: HumanCode=FormalSpec_OR_RawWriting (e.g. Donna-Style)
Partner = Co-founder (remote; needs to sign agreement)
Runtime = Cowork(ephemeral sessions + persistent Supabase)
HerPatience(withKids) > Mine
```

### Connectors

`_FOR_`, `_OR_`, `_NOT_`, `_ON_`, `_THAN_`, `+`, `-`:

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

ASCII `->` is canonical. Unicode `→` is acceptable in rendered documents but the typing standard is `->`:

```
Lead -> Quote -> Accept -> Book -> Deliver -> Invoice
Phase1: Prototype -> Phase2: Platform -> Phase3: Scale
Start -> Read_CLAUDE.md -> Query_tasks -> Execute -> Report
```

### Lists in square brackets

```
Stack = [n8n, Supabase, Retell, Sequenzy]
AIHandles = [Admin, Coordination, MessageRouting, Speed]
HumansHandle = [Judgment, Exceptions, Relationships, Care]
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

Sometimes a line's *action* is what defines it. Use uppercase with a colon:

```
Every_Compound_hr(Practiced) _MAKES: Better(You)^2
HeHas: SleepDebt. Expect: Grumpy
```

### The period as separator

Two intent-labelled statements on one line, full stop between them, causal link implied by adjacency:

```
HeHas:SleepDebt. Expect:Grumpy
```

HumanCode trusts the reader to hold the chain.

---

## Cut It Down — the teaching move

The fastest way to learn HumanCode is to take one English sentence and compress it. Each pass removes more filler; each pass still has to pass the readability test.

**Source (214 chars):**

> "If we ship HumanCode publicly, we need real examples, not marketing copy, because the 76% compression number is a real thing but the Donna profile is what actually makes people believe the notation carries meaning."

**HumanCode (96 chars, 55% tighter):**

```
IF(Ship_Publicly) -> real_examples_NOT_marketing
76%_compression = real; DonnaProfile = the_proof
```

---

## The Ten — David's canonical practice set

Full version: [`Canonical-Examples.md`](./Canonical-Examples.md). Summary here for quick reference:

| # | Source | HumanCode | Move |
|---|--------|-----------|------|
| 1 | A good night's sleep equals a better mood the next day. | `1GoodSleep = BetterMood_ON_NextDay` | `=` + `_ON_` time window |
| 2 | Coffee plus a short walk wakes me up faster than either alone. | `Coffee + ShortWalk -> ForME(=FasterWakeDuration_THAN_EitherAlone)` | `+` · `->` · `_THAN_` |
| 3 | The project without Tom feels ten kilos lighter. | `ImpactTOFeelings(Project_WithoutTom) = 10kg_Lighter` | Parenthetical context; unit-suffixed literal |
| 4 | Five clients at £2k each is £10k a month. | `Math: 5Clients @ £2kEach = £10k/m` | Intent label; `@` rate; `/m` period |
| 5 | Split the revenue evenly between the three of us. | `Proposal/Instruction: Split_Revenue(Evenly_x3)` | Dual label; `x3` multiplicity |
| 6 | Every compound hour of practice makes you exponentially better. | `Every_Compound_hr(Practiced) _MAKES: Better(You)^2` | Verb-as-label; `^2` colloquial exponential |
| 7 | If it rains before nine, the job gets rescheduled. | `IF(Rain=true BEFORE 9am, Reschedule(Job))` | Canonical conditional |
| 8 | Her patience with the kids is greater than mine. | `HerPatience(withKids) > Mine` | `>` · parenthetical scope |
| 9 | All the morning tasks combined take about two hours. | `TasksTotalDuration(morning) = 2hrs` | Aggregated subject; scope in parens |
| 10 | He hasn't slept, therefore he's grumpy. | `HeHas:SleepDebt. Expect:Grumpy` | Intent labels as sentences; `.` as separator |

---

## What HumanCode is NOT

These are AI artefacts from when the notation was over-formalised by an LLM. They are not HumanCode.

- **No empty parentheses** — `Dissolve()` is wrong. Write `Status = Dissolving(Apr_2026)`.
- **No method calls** — `EstablishSafety(via_competence)` is wrong. Write `Donna = Receptionist(fierce, competent)`.
- **No function signatures** — this isn't code. Parentheses hold context hints only.
- **No rigid one-concept-per-line padding** — chain related ideas with semicolons when they belong together.
- **No container words** — never use Block, Node, Module, Component, Segment, SectionBlock, StrategicLogicBlock. Label the concept, not the container.
- **No over-compression past readability** — if a reader has to translate the symbols back into words before understanding, you've gone too far.

### Anti-pattern table (real error, logged 2026-04-24)

Logged from a session where an AI assistant suggested "cuts" that violated the operating principle:

| Wrong (AI overreach) | Right (David's dialect) |
|---|---|
| `Sleep(good) → Mood(+, nextDay)` | `1GoodSleep = BetterMood_ON_NextDay` |
| `Project(−Andy) ≈ 10kg_lighter` | `ImpactTOFeelings(Project_WithoutTom) = 10kg_Lighter` |
| `Revenue ÷ 3` | `Proposal/Instruction: Split_Revenue(Evenly_x3)` |
| `Σ(am.tasks) ≈ 2hr` | `TasksTotalDuration(morning) = 2hrs` |
| `−Sleep ∴ Grumpy` | `HeHas:SleepDebt. Expect:Grumpy` |

The wrong column is tighter. It's also unreadable to the target user and un-typable on a standard keyboard. That disqualifies it.

---

## Companion file format (.hc.md)

When AI generates HumanCode for a markdown file, output it as `filename.hc.md` in the same folder.

**Header:**

```
SOURCE = filename.md
ENCODED = YYYY-MM-DD
PURPOSE = one-line summary
```

**Body:** Group by blank lines. Use intent labels to organise. For short files (<30 output lines), skip section headers — let labels and blank lines do the work. For longer docs, section headers are fine.

**Target:** <30% of source line count. Scannable in 10 seconds. Emotional charge preserved.

See the [`examples/`](./examples/) folder for three representative `.hc.md` files: a session report companion, a voice/identity profile, and a system architecture spec.

---

## Document Code Classifier (optional extension)

A classifier that reads a doc body and produces a structured code.

Format: `document_code = Role_Access_OrgUnit_DocType` (e.g. `2_1_Delivery_BookingSquad_SOP`)

```
Role(0-3,9): 0=Founder/doctrine, 1=Leadership, 2=Builders, 3=Training, 9=unclear
Access(0-3,9): 0=Public, 1=Internal, 2=Restricted, 3=Confidential, 9=unclear
OrgUnit: Delivery_*, Growth_*, Comms_*, Money_*, Platform_*, People_*, Org_CrossBase
DocType: SOP, Spec, Schematic, Schema, Policy, Script, Report, Guide, Template, Checklist, Index, Notes, Doctrine

Safety: IF(confidence < 0.65) -> 9_9_Org_CrossBase_Notes + needs_review
```

---

## Origin Story

HumanCode wasn't designed. It emerged from how David Caldicott naturally compresses thought when writing fast — assignments, intent labels, semicolon chains, parenthetical context. In late 2025, an LLM formalised it into a teachable spec (an Instruction Set v1.0, agent voice profiles, FAQ encodings). The formalisation was useful but drifted from the source — adding code-like patterns (empty parens, method calls) that weren't part of David's original notation.

This reference recalibrates to the source dialect. The key insight: a human's natural shorthand, when structured just enough, becomes an extremely efficient format for AI context loading — achieving 70–80% compression while remaining readable to anyone willing to slow down and parse it.

**Timeline:**

```
2018     Character-based role-play methodology for running a business (pre-AI; proto-HumanCode thinking)
2025-06  Instruction Set v1.0 formalised by an LLM
2025-12  Voice profiles, full profile, FAQ encodings created
2026-01  Document classifier, agent prompts in "Ultra-Lean HumanCode"
2026-04  Recalibrated to David's actual dialect
2026-04  Operating principle locked: average human, types quickly, no translation
2026-04  Public release + `.hc.md` convention adopted
```

---

## Further reading

- [`Canonical-Examples.md`](./Canonical-Examples.md) — twenty worked translations, the spec-in-practice
- [`SKILL.md`](./SKILL.md) — deployable Claude skill
- [`examples/`](./examples/) — representative `.hc.md` files
