# CLAUDE.md

The Calcination operation — Stage 1 of the Magnum Opus. Burn project bloat to reveal essence.

> "That which does not serve the Work must burn."
>
> Element: Fire 🜂 · Stage: Nigredo · Operation: destruction in service of essence

**What this is**: a destructive operation. It does not add features. It does not refactor for elegance. It identifies what doesn't belong and burns it — anchored to a declared intent.

**Tradeoff**: bias toward removing over preserving. The constructive counter-operation is [`coagulate`](https://github.com/HermeticOrmus/magnum-opus-skills); use them as a pair.

## Position in the Magnum Opus

| # | Stage | Element | Operation |
|---|---|---|---|
| **1** | **Calcination 🜂** | **Fire** | **Burn what doesn't serve** |
| 2 | Dissolution 🜄 | Water | Let understanding flow |
| 3 | Separation 🜁 | Air | Gold from dross |
| 4 | Conjunction ☌ | Sacred marriage | Unite opposites |
| 5 | Fermentation 🜅 | Decay + rebirth | Trial by failure |
| 6 | Distillation ⊚ | Vapor | Refine to wisdom |
| 7 | Coagulation 🜍 | Crystallization | Shape the final form |

Calcination is the opening operation. Standalone: yes. Companion: full pipeline in [`magnum-opus-skills`](https://github.com/HermeticOrmus/magnum-opus-skills).

## Hard rules — never violate

1. **No deletion without intent.** Before removing anything, the three-layer intent must be declared (see below). Without intent, removal is reckless.
2. **Reversible by construction.** Every deletion is via git, with a clear commit per item. Auto-revert on failed verify.
3. **Verify after every step.** Tests pass + build succeeds before moving to next item.
4. **No batch removal.** Item by item. Batches conceal the item that broke the verify.
5. **The agent does not decide what burns.** The user declares intent. The agent surfaces candidates; the user approves each one.

## The three-layer intent

Before burning anything, declare:

1. **Business intent** — what is this project for, in business terms? "Ship the v3 API by Q3" or "Maintain the legacy reporting service until 2027 migration."
2. **Architectural intent** — what shape should the codebase take? "Microservice with strict layered architecture" or "Monolith with explicit module boundaries."
3. **Stylistic intent** — what should the code feel like? "Concise functional style" or "Defensive OO with extensive guards."

The three intents collectively define what serves and what doesn't. Without them, "bloat" is opinion.

## What gets burned

Four categories, identified by parallel scan:

### 1. Code rot

- Functions / classes / modules that are unreferenced (verified via static analysis + grep)
- Dead branches (unreachable code, perpetually-false conditionals)
- Commented-out code (> 3 months old, no tracking ticket)
- TODO markers > 6 months old with no follow-up
- Files in `_old/`, `legacy/`, `deprecated/` directories with no callers

### 2. Structural bloat

- Modules whose stated purpose has changed but whose name hasn't
- Inheritance hierarchies > 3 levels deep with no functional reason
- "Utility" modules that became dumping grounds
- Abstraction layers introduced for hypothetical flexibility that never materialized
- Configuration that's never been overridden from defaults

### 3. Dependency bloat

- Packages imported once, in a single file
- Packages that overlap (left-pad and string-utils)
- Dev dependencies that don't run in CI
- Frozen-version dependencies with security vulnerabilities
- Transitive dependencies bloating the lockfile

### 4. Documentation + test bloat

- Documentation describing features that don't exist
- Tests that test the test framework, not the code
- Tests that never fail
- Documentation organized by file structure rather than by user need
- README sections that haven't been updated since v0.1

## The procedure

1. **Declare three-layer intent** (Business + Architectural + Stylistic)
2. **Dispatch four parallel scans** (code rot, structural, dependency, docs+tests)
3. **Produce tiered CALCINATION-PLAN.md** with items sorted by impact / risk
4. **Execute item by item**:
   a. Show item + reason
   b. User approves
   c. Make the change
   d. Run verify (tests + build)
   e. If verify fails: auto-revert + flag
   f. If verify passes: commit with `chore(calcinate): <item>`
5. **Final report**: what was removed, what was preserved + why, what was deferred

## When to use

- A project that "has gotten fat" — accumulated 6+ months of features without prune
- Before a major refactor (calcinate first so the refactor is on the essence, not the bloat)
- Before handoff (the next maintainer shouldn't inherit the dead code)
- Onboarding (do calcinate together with the new hire so they see what doesn't belong)
- Post-acquisition (the acquired codebase has different intent; calcinate to align)

## When NOT to use

- During active feature work (calcinate is a meta-operation; don't mix with feature shipping)
- On code you don't understand (research first; never burn what you can't justify)
- On code under regulatory scrutiny (you need an audit trail beyond git for some industries)
- On someone else's project without their three-layer intent (you're guessing)

## Anti-patterns

- **Calcinate without intent** — random deletion of what looks ugly. Produces drift, not essence.
- **Calcinate everything at once** — batch removal that conceals failures.
- **Calcinate during feature work** — mixed signals; PR review becomes confused.
- **Calcinate aesthetically** — removing what looks bad rather than what doesn't serve.
- **Calcinate without coagulate** — pure destruction without the constructive partner produces a void, not a clean structure.

---

**License**: MIT. The Magnum Opus framework is rooted in Hermetic tradition (public domain); the application to software engineering is yours.
