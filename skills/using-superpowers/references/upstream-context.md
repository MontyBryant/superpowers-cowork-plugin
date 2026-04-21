# Upstream Context

This plugin is a **deliberate fork** of [Superpowers](https://github.com/obra/superpowers) by Jesse Vincent. Upstream targets software development; this fork targets creative, strategic, and business knowledge work.

Load this file when a user asks about the plugin's origins, wants to add a new skill, or asks how this relates to the "real" Superpowers.

## Fork Rationale

Core methodology is shared — Iron Laws, verification gates, rationalization prevention, the 1% Rule. Domain-specific content differs: upstream has TDD, git workflows, code debugging; this fork replaces those with proposal drafting, campaign strategy, research, creative briefs.

**Decision:** Maintain a deliberate fork, selectively adopting upstream methodology improvements while owning domain-specific content. (Decision 001 in DECISIONS.md.)

## Skill Mapping

| This Plugin | Upstream Equivalent | Relationship |
|---|---|---|
| brainstorming | brainstorming | Adapted (creative/business domain) |
| writing-plans | writing-plans | Adapted (non-code deliverables) |
| executing-plans | executing-plans | Adapted (removed git/branch references) |
| verification-before-completion | verification-before-completion | Adapted (business verification criteria) |
| using-superpowers | using-superpowers | Adapted (knowledge-work skill list) |
| writing-skills | writing-skills | Adapted (non-code pressure scenarios) |
| systematic-problem-solving | systematic-debugging | Significantly adapted (business problems, not code bugs) |
| two-stage-review | — (part of subagent-driven-development) | Original (extracted review pattern) |
| feedback-reception | receiving-code-review | Significantly adapted (client/stakeholder feedback) |
| parallel-work | dispatching-parallel-agents | Adapted (knowledge-work parallelization) |

## Upstream Skills NOT Adopted

| Upstream Skill | Why |
|---|---|
| test-driven-development | Code-specific. Principle embedded in writing-skills and verification. |
| systematic-debugging | Replaced by systematic-problem-solving. |
| requesting-code-review | Code-specific. Pattern captured in two-stage-review. |
| receiving-code-review | Replaced by feedback-reception. |
| using-git-worktrees | Git-specific. No knowledge-work equivalent. |
| finishing-a-development-branch | Git-specific. No knowledge-work equivalent. |
| subagent-driven-development | Review pattern → two-stage-review. Dispatch pattern → parallel-work. |

## Adding a New Skill

Before creating a new skill for this plugin:

1. Check if an upstream equivalent exists — adapt rather than invent when possible
2. Follow the `writing-skills` methodology (hypothesis-driven, test before writing)
3. Every skill needs: frontmatter (`name`, `description`), an Iron Law, When to Use, When NOT to Use, and the process
4. After adding, update plugin.json version (minor bump for new skills), CHANGELOG, and the Sync Status table in UPSTREAM.md

## What to Adopt from Upstream

**Always adopt:** Improvements to rationalization prevention, skill triggering (CSO), verification methodology, pressure-scenario testing.

**Selectively adopt:** New skills where the underlying pattern applies beyond code. Structural changes to shared skills.

**Don't adopt:** Code-specific tooling (TDD, git workflows, CI/CD), language-specific examples, platform-specific references.
