# Roadmap

Ideas, directions, and planned improvements for the Superpowers for Knowledge Work plugin.

Items move to the **Decided** section once evaluated and committed to. Completed items are noted inline.

---

## Parking Lot

### Workspace-Specific Skill Customisation

**Idea:** Create a montymerlinHQ-tailored layer on top of the core skills — adding workspace-specific guidance that the current generic skills don't provide.

**Context:** Analysis of the MM skills vs. upstream (April 2026) found that the MM skills are not meaningfully customised to the montymerlinHQ workspace. They're adapted for generic knowledge work, but don't reference the workspace's actual structures: SOUL.md, STYLE.md, journal processing, the 6Rs pipeline (Record, Reduce, Reflect, Reweave, Verify, Rethink), Ars Contexta, OPAL entity extraction, or the three-space knowledge model (self / knowledge garden / ops).

**What this could look like:**
- `brainstorming` — when brainstorming inside montymerlinHQ, check SOUL.md for values alignment and STYLE.md for voice constraints before proposing approaches
- `writing-plans` — for knowledge-garden tasks, plans should reference the 6Rs pipeline stages; for ops tasks, reference inbox/process flow
- `systematic-problem-solving` — include the montymerlinHQ knowledge structures as diagnostic tools (e.g., has this been captured in the right layer?)
- `two-stage-review` — spec compliance should check against SOUL.md/STYLE.md for identity-aligned work
- Possibly a new `workspace-context` skill that loads relevant context (SOUL, STYLE, USER) before any significant task

**Open question:** Should this be a separate plugin that extends the core skills, or should the core skills be made more context-aware via configuration?

**Raised:** 2026-04-15

---

## Decided

- **Bundle upstream context as on-demand reference** — → Decision 003. `status: decided`
