# Decisions

Architectural decisions for the Superpowers MM Plugin. Log significant choices here *before* implementing, using the format below.

---

## Decision 001 — Deliberate fork over mirror (2026-04-03)

**Context:** Superpowers upstream targets software development workflows. The montymerlinHQ use case is primarily creative, strategic, and business knowledge work — proposals, campaigns, research, strategy documents — where code-specific skills (TDD, git workflows, debugging) don't apply.

**Decision:** Maintain a deliberate fork, selectively adopting upstream methodology improvements while replacing code-specific content with knowledge-work equivalents.

**Consequences:** We stay current on methodology (Iron Laws, verification patterns, rationalization prevention) while keeping domain-specific content relevant. The cost is ongoing maintenance overhead from tracking upstream.

**Alternatives Considered:**
- *Mirror upstream exactly* — rejected. Too many code-specific skills that would confuse or not trigger in a knowledge-work context.
- *Wrapper plugin that extends upstream* — rejected. Skill precedence rules make this complex; cleaner to own the full skill set.

---

## Decision 002 — Adopted agentic scaffold (2026-04-15)

**Context:** The plugin repo lacked CLAUDE.md, CHANGELOG.md, and DECISIONS.md, making it harder for Claude Code to understand conventions and for the history to be legible.

**Decision:** Add the standard agentic scaffold (CLAUDE.md, CHANGELOG.md, DECISIONS.md) alongside the existing README.md and ROADMAP.md.

**Consequences:** The repo is now a first-class agentic workspace. Claude Code has explicit instructions for skill authoring, versioning, and upstream sync.

**Alternatives Considered:**
- *Leave as-is* — rejected. Without CLAUDE.md, conventions have to be re-explained each session.

---

## Decision 003 — Bundle upstream context as on-demand reference (2026-04-21)

**Context:** Cowork loads skill SKILL.md files but doesn't auto-load the plugin's CLAUDE.md, README.md, or UPSTREAM.md. The skills are self-contained methodology docs and work well at runtime — except when a user asks about the plugin's origins ("how does this relate to the real Superpowers?"), wants to add a new skill (needs to check upstream first), or questions the fork rationale. That context lives only in UPSTREAM.md and CLAUDE.md, which are invisible during Cowork invocation.

**Decision:** Add `skills/using-superpowers/references/upstream-context.md` with a condensed version of the skill mapping, fork rationale, adoption criteria, and new-skill checklist. Add a one-line pointer in `using-superpowers/SKILL.md` directing the agent to load it when relevant.

**Consequences:**
- The meta-skill can now answer origin questions and guide new skill creation without external docs
- Follows the same pattern established in agentic-scaffold Decision 008 (references for *why*, SKILL.md for *what*)
- Minor maintenance: upstream-context.md must be updated when UPSTREAM.md Sync Status table changes
- Patch bump (0.3.0 → 0.3.1) — no new skills, just a reference addition

**Alternatives Considered:**
- *Inline upstream context in using-superpowers SKILL.md* — rejected. Adds ~60 lines to a skill that's already the longest in the plugin, and the context is rarely needed
- *Leave as-is* — viable, since the gap is minor. But the cost of adding it is low and the pattern is already established

---

## Decision 004 — Dual-distribution packaging with marketplace.json (2026-04-21)

**Context:** The plugin was positioned as a "Claude Code plugin" in documentation, with no explicit Cowork install path or marketplace.json for `claude plugins install`. As the plugin portfolio standardised on dual-distribution (Claude Code CLI + Cowork desktop), this plugin was the only one without a marketplace listing or installation instructions for both hosts.

**Decision:** Add `.claude-plugin/marketplace.json`, add a Distribution section to CLAUDE.md, and add installation instructions (Claude Code CLI, Cowork, Cursor) to README.md. Follow the pattern established by mdpowers and git-plugin.

**Consequences:**
- Users can install via `claude plugins install github.com/montymerlin/superpowers-MM-plugin`
- Cowork users can install via `.plugin` zip or marketplace
- Documentation no longer positions the plugin as single-host
- marketplace.json version must stay in sync with plugin.json on each release

**Alternatives Considered:**
- *Claude Code only* — rejected. The skills are pure markdown with no host-specific code; there's no reason to limit distribution
- *Cowork only* — rejected. Claude Code is the primary development environment where the plugin is also heavily used
