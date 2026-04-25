# HumanCode

**A shorthand for thinking — that AI can read at a fraction of the token cost.**

HumanCode is a natural notation for compressing complex thought into scannable, AI-parseable fragments. It isn't a programming language. It isn't pseudocode. It's closer to the way a carpenter writes a measurement on a wall before they cut: short, declarative, lossless in the direction that matters.

Created by [David Caldicott](https://medium.com/@davidcaldicott). Used on real work for two years. Open-sourcing now because explaining it one conversation at a time is slower than publishing the reference.

---

## The operating principle

> An average human with no maths or programming background should be able to type it quickly and read it without translation. Readability without mental decoding is the ceiling. There is no "more correct" compressed form beyond that.

Every symbol, pattern, or compression must pass four tests:

1. **Typable quickly** on a standard keyboard
2. **Readable without mental translation**
3. **No maths or programming background** required
4. **No "more correct" form** — once it passes 1–3, it's done

Symbols that pass: `=` · `+` · `-` · `>` · `<` · `->` · `^` · `@` · `/` · `:` · `()` · `;` · `_` · `[]` · `.`

Symbols that fail: `∴` · `Σ` · `≈` · `∫` · `→` (use `->`) · `−` (use `-`) · `≥` · `≤` · `^n` with abstract `n`. If it needs a character map to type, it fails the principle.

---

## Why this exists

The bottleneck in working with AI is not the model anymore. The models are smart enough. The point of failure is upstream of the model, in the conversational English we keep trying to push through it. Ambiguity. Cultural assumptions. Structural fluff. Soft verbs like *feels* and *seems* that hide three decisions inside a single word. The fidelity of what you meant drops the second you hit send, and the model can only work with what arrives.

HumanCode changes the shape of what you send. Nouns you reuse get stuck together in PascalCase (`GoodSleep`, not "a good night's sleep"). Colons declare what a line IS (`Math:`, `Proposal:`, `Instruction:`). Arrows (`->`) mark sequence. Units stay attached to numbers (`£2k`, `10kg_Lighter`, `/m` for per month). Parentheses hold context hints in natural English, never method calls. You do the parsing work in advance and tell the system — and yourself — what the line is doing before either of you has to interpret it.

What falls out of that practice is not just cheaper tokens. It's clearer thinking, by force. *I feel like we should maybe lean in to this* becomes either a HumanCode line or it becomes nothing, because there's no structure underneath it. That's diagnostic, not pejorative. Finding the boundary of your own thinking is the most useful thing you can do before asking an AI to help with it.

---

## Two ways to use it

HumanCode runs in two modes. Both share the same notation.

**Background mode (AI ↔ AI).** Let an assistant generate `.hc.md` companion files alongside your long-form markdown notes. Humans can peek if curious. Used for session report companions, knowledge base compressions, voice/identity profiles, and system specs. The companion file pattern uses a stacked extension: `filename.md` alongside `filename.hc.md`, so every markdown tool renders both without special handling.

**Active mode (human writing).** Write HumanCode yourself as a thinking tool. Compress prompts (fit more context; cheaper; faster). Clarify your own thinking (force the bones of a thought to surface). Take scannable notes that reread in ten seconds. Both modes share the same grammar — AI output in HumanCode reads the same as handwritten HumanCode.

---

## One worked example

Source prose:

> A good night's sleep equals a better mood the next day.

HumanCode:

```
1GoodSleep = BetterMood_ON_NextDay
```

One compressed line, and three decisions surface that the English version hid. `Good` is a value judgement, and it's kept. `Better` is comparative, and it now has to mean something specific — better than what? Baseline. `_ON_NextDay` is a temporal modifier, explicit. The line commits. The paragraph didn't.

For nine more translations at that grain, plus the extended dialect moves (intent labels, chained conditionals, inequality-with-condition, role-chain parallelism), see [`Canonical-Examples.md`](./Canonical-Examples.md).

---

## Files in this repo

| File | Purpose |
|------|---------|
| [`README.md`](./README.md) | You are here |
| [`REFERENCE.md`](./REFERENCE.md) | Master reference — symbol set, dialect, companion-file format, origin |
| [`SKILL.md`](./SKILL.md) | Deployable Claude skill — drop into `.claude/skills/humancode/` and invoke |
| [`Canonical-Examples.md`](./Canonical-Examples.md) | Twenty worked translations by the creator — the spec-in-practice |
| [`examples/`](./examples/) | Representative `.hc.md` files: session report companion, voice profile, system spec |
| [`LICENSE`](./LICENSE) | MIT |

---

## Try this

Take something you can't quite describe — your current project, the thing your team keeps arguing about, the weird side hustle, the method you've never written down. Write it in HumanCode. Don't aim for short. Aim for honest. PascalCase the nouns you reuse. Colons for what kind of line you're writing. Arrows for sequence. Units attached to numbers.

If you can do it, you understand what you're doing.

If you can't, you've found the exact place where your thinking stops being clear. That isn't a failure. That's a diagnosis. That's where the work begins.

---

## Use, break, fork

MIT licence. No attribution obligation, but a mention is welcome if you build on it. Issues and pull requests open. Tell me what doesn't work for you.

— [David Caldicott](https://medium.com/@davidcaldicott) · Norwich, 2026
