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

The library being consolidated here is 92 skills, in three copies that had drifted apart. 59 are stack-bound, and 51 of those form a 13-step × 4-suite matrix: .NET e2e, Java e2e, Python e2e, Python unit.

Measuring that matrix before moving it changed the plan. Across suites, the same step shares very little text — character similarity runs 0.13 to 0.78, against 0.91–0.96 for one skill compared between two drifted copies and 0.13 for two unrelated skills. Only `control-flow` is close enough to merge (0.94–0.98 across the three non-.NET suites). So these are not one step written four times; they are four documents that happen to share a name, and hiding them behind a single skill would add indirection without removing content.

Consolidation therefore moves what is genuinely shared and leaves the rest as separate skills.

- [x] Plugin skeleton, and the install path verified end to end — `marketplace add` → `install` → the skill reaching a live session's skill index
- [ ] Move the 33 stack-agnostic skills
- [ ] Ship the .NET e2e path, which is the one the orchestrating skills (`bdd-cycle`, `mvp-run`, `mvp-acceptance-tests`) actually delegate to. The Java and Python suites have no inbound references and nothing selects a stack at runtime, so their scope is still open
- [ ] Switch the source projects over to installing this plugin

## Not affiliated with AIxBDD

This library is an independent implementation of acceptance-driven development. It is not derived from, and shares no code with, [Waterball-Software-Academy/aixbdd](https://github.com/Waterball-Software-Academy/aixbdd) — a separate Apache-2.0 project with a similar goal and a different decomposition. The two share four skill names and nothing else; this one's first commit predates that repository.

## License

MIT — see [LICENSE](LICENSE).
