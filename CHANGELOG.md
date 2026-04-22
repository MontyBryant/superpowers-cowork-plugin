# Changelog

Narrative history of significant changes to the Superpowers MM Plugin. Each entry describes what changed and why — not a per-commit log.

---

## 2026-04-22 — v0.5.0: AGENTS.md canon and Codex install support

Shifted the repo to the same compatibility-layer model now used across the plugin portfolio. `AGENTS.md` is now the canonical repo instruction file, `CLAUDE.md` is a thin wrapper, and the one runtime reference used by the meta-skill now resolves through a portable root variable instead of assuming a Claude-only plugin host.

Added Codex install/update scripts, fixed installation naming drift in the docs, and aligned plugin metadata so the repo is clearly positioned as a host-agnostic methodology package with Claude packaging compatibility. See Decision 006.

## 2026-04-21 — v0.4.0: Rename to superpowers-knowledge, coexistence with official Superpowers

Renamed the plugin from `superpowers-cowork` to `superpowers-knowledge` — the old name implied Cowork-specificity, but the plugin runs in any host. The new name signals the knowledge-work domain that makes it complementary to (not competing with) the official Superpowers plugin.

Added a Coexistence section to CLAUDE.md and README explaining how the plugin works alongside Jesse Vincent's Superpowers. The design: 7 shared methodology skills (brainstorming, writing-plans, etc.) are domain-scoped via their descriptions so the agent routes by context — code tasks go to upstream, knowledge tasks to this plugin. 3 original skills (systematic-problem-solving, two-stage-review, feedback-reception) have no upstream equivalent and add unique value in any configuration.

Updated all 10 skill SKILL.md descriptions to include explicit domain-scoping language. The 7 shared skills now say "for non-code knowledge work" and reference the upstream coexistence pattern. The 3 originals now explicitly note they have no upstream equivalent.

Also renamed README from "Superpowers for Cowork" to "Superpowers for Knowledge Work". See Decision 005.

---

## 2026-04-21 — v0.3.3: Authorship attribution update

Corrected the authorship record across README.md, CLAUDE.md, and plugin.json to properly reflect the fork's lineage. Rollo Bryant is credited as the original fork author (v0.1.0), having adapted Jesse Vincent's Superpowers framework for knowledge work. Monty Bryant is listed as the current maintainer (v0.2.0 onwards). The previous README listed only Rollo under "Author", which omitted the handoff entirely.

---

## 2026-04-21 — v0.3.2: Dual-distribution packaging

Added `marketplace.json` for Claude Code CLI installation via `claude plugins install`. Added Distribution section to CLAUDE.md and Installation section to README.md covering Claude Code, Cowork, and Cursor install paths. The plugin was previously documented as Claude Code-only; it now explicitly supports both hosts. See Decision 004.

---

## 2026-04-21 — v0.3.1

Added `skills/using-superpowers/references/upstream-context.md` with a condensed version of the fork rationale, skill mapping, adoption criteria, and new-skill checklist from UPSTREAM.md. Added a one-line pointer in the using-superpowers meta-skill so the agent can answer origin questions and guide new skill creation without needing the non-loaded repo docs. Follows the same references pattern established in agentic-scaffold Decision 008. See Decision 003.

## 2026-04-15

Renamed the plugin repo from `superpowers-plugin` to `superpowers-MM-plugin` to make its identity as a montymerlinHQ-specific fork clearer. Added agentic scaffold (CLAUDE.md, CHANGELOG.md, DECISIONS.md, ROADMAP.md) to bring the repo up to agentic best practices.

Also added a ROADMAP item to explore workspace-specific customisation of the MM skills — the current skills are adapted for generic knowledge work but don't reference montymerlinHQ-specific structures (SOUL.md, STYLE.md, 6Rs pipeline, Ars Contexta, etc.). That's a future improvement tracked in ROADMAP.md.

---

## 2026-04-08 — v0.2.0

Synced with upstream Superpowers v5.0.7. Ported the CSO methodology, bulletproofing framework, and skill-type testing patterns into `writing-skills`. Added scope-decomposition and spec-saving steps to `brainstorming`. Tightened rationalization prevention in `verification-before-completion`. Added two new skills:

- **parallel-work** — adapted from upstream `dispatching-parallel-agents` for knowledge-work parallelization
- **executing-plans** — adapted from upstream with git/branch references removed

---

## 2026-04-03 — v0.1.0

Initial release. Ten skills adapted from Superpowers v5.0.x by Rollo Bryant. Core methodology (Iron Laws, verification gates, rationalization prevention) is shared with upstream; domain-specific content rewritten for creative, strategic, and business workflows rather than software development.
