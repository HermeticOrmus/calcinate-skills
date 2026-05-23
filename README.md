# Calcinate Skills

> A single `CLAUDE.md` for the Calcination operation — Stage 1 of the seven-stage Magnum Opus. Burn project bloat to reveal essence.

> *"That which does not serve the Work must burn."*

## What is Calcination?

The destructive operation. It does not add features. It does not refactor for elegance. It identifies what doesn't belong and burns it — anchored to a declared intent.

Element: Fire 🜂 · Stage: Nigredo · Companion: [`coagulate`](https://github.com/HermeticOrmus/magnum-opus-skills) (the constructive counter)

## Position in the seven-stage cycle

```
1. Calcination 🜂 — Burn what doesn't serve         ← YOU ARE HERE
2. Dissolution 🜄 — Let understanding flow
3. Separation 🜁 — Gold from dross
4. Conjunction ☌ — Unite opposites
5. Fermentation 🜅 — Rebirth through trial
6. Distillation ⊚ — Refine to wisdom
7. Coagulation 🜍 — Crystallize into form
```

Calcination is the opening move. It works standalone (a project that has gotten fat) or as the gateway to the full Magnum Opus pipeline (see [`magnum-opus-skills`](https://github.com/HermeticOrmus/magnum-opus-skills)).

## Hard rules

- No deletion without three-layer intent (Business + Architectural + Stylistic)
- Reversible by construction (git per item)
- Verify after every step (tests + build pass)
- No batch removal (item by item)
- Agent surfaces, user approves

Full content: [`CLAUDE.md`](CLAUDE.md).

## What gets burned

Four parallel scans:

1. **Code rot** — unreferenced functions, dead branches, stale TODOs
2. **Structural bloat** — abstractions that didn't materialize, dumping grounds
3. **Dependency bloat** — single-use packages, overlapping libs, security debt
4. **Documentation + test bloat** — docs for features that don't exist, tests of the framework

## Install

```bash
curl -o CLAUDE.md https://raw.githubusercontent.com/HermeticOrmus/calcinate-skills/main/CLAUDE.md
```

Or as a [Claude Code skill](skills/calcinate/) or [Cursor rule](.cursor/rules/calcinate.mdc).

## When to use

- A project that has gotten fat (6+ months of accretion)
- Before a major refactor (calcinate first; refactor on essence)
- Before handoff (next maintainer shouldn't inherit dead code)
- Onboarding (do it with new hires; they see what doesn't belong)
- Post-acquisition (align acquired codebase to new intent)

## When NOT to use

- During active feature work
- On code you don't understand
- On regulated code (audit trails beyond git)
- On someone else's project without their three-layer intent

## See also

- [`magnum-opus-skills`](https://github.com/HermeticOrmus/magnum-opus-skills) — the full 7-stage cycle
- [`hermetic-laws-skills`](https://github.com/HermeticOrmus/hermetic-laws-skills) — the principle framing
- [`vibe-engineer-skills`](https://github.com/HermeticOrmus/vibe-engineer-skills) — directing AI codegen well

## License

MIT.
