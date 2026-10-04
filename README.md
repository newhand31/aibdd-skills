# aibdd-skills

Acceptance-driven development skills for [Claude Code](https://claude.com/claude-code), installed as a plugin instead of copied into every project.

> **Status: 0.1.0, early access.** One skill is published here. It exists to prove the install path works before the rest of the library moves in. See [Roadmap](#roadmap).

## Why this repo exists

The skills in this library grew up inside a project scaffold, and that scaffold got cloned. Three copies later, every one of the 92 shared skills had drifted apart — a guardrail added to one copy never reached the other two, and all three kept being loaded as if they were authoritative.

Copying is not versioning. A plugin is: one source of truth, installed by name, updated in one place.

## Install

```
/plugin marketplace add newhand31/aibdd-skills
/plugin install aibdd-skills@newhand31-aibdd
```

## What's here

| Skill | What it does |
|---|---|
| `aibdd-discovery` | Entry point for spec discovery. Coordinates activity, feature, API and ERM views in two passes (Strategic / Tactical), keeping all four consistent no matter which one you enter from. |

Skill content is written in Traditional Chinese; skill names, frontmatter and file layout are English.

## Roadmap

The library being consolidated here is 93 skills across three drifted copies. Consolidation collapses them rather than moving them verbatim: 56 of the 93 are stack-bound, and 42 of those are the same 14 steps written out three times (.NET / Java / Python). Those become 14 skills with per-stack variant references, which is why the target is roughly 65 skills, not 93.

- [x] Plugin skeleton + install path verified against `claude plugin validate --strict`
- [ ] Collapse the 14 × 3 stack triples into 14 skills + `references/variants/<stack>.md`
- [ ] Move the 37 stack-agnostic skills
- [ ] Switch the source projects over to installing this plugin

## Not affiliated with AIxBDD

This library is an independent implementation of acceptance-driven development. It is not derived from, and shares no code with, [Waterball-Software-Academy/aixbdd](https://github.com/Waterball-Software-Academy/aixbdd) — a separate Apache-2.0 project with a similar goal and a different decomposition. The two share four skill names and nothing else; this one's first commit predates that repository.

## License

MIT — see [LICENSE](LICENSE).
