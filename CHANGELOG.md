# Changelog

Narrative history of significant changes to the Superpowers MM Plugin. Each entry describes what changed and why — not a per-commit log.

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
