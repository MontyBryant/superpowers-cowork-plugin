# Upstream Tracking

This plugin is an adaptation of [Superpowers](https://github.com/obra/superpowers) by Jesse Vincent, adapted for non-code knowledge work (creative, strategic, business workflows) by Rollo Bryant.

## Relationship to Upstream

This is a **deliberate fork**, not a mirror. The core methodology (Iron Laws, verification gates, rationalization prevention) is shared, but the domain-specific content differs significantly:

- Upstream targets software development (TDD, debugging, code review, git workflows)
- This plugin targets knowledge work (proposals, campaigns, research, strategy, creative briefs)

We selectively adopt upstream improvements that apply to both domains, while maintaining our own domain-specific skills.

## Sync Status

| Date | Upstream Version | Plugin Version | What Changed |
|------|-----------------|----------------|--------------|
| 2026-04-03 | ~v5.0.x | v0.1.0 | Initial adaptation by Rollo Bryant |
| 2026-04-08 | v5.0.7 | v0.2.0 | Ported CSO methodology, bulletproofing framework, skill-type testing patterns to writing-skills. Added scope-decomposition and spec-saving to brainstorming. Tightened rationalization prevention in verification-before-completion. Added rigid/flexible skill typing to using-superpowers. New skills: parallel-work (from dispatching-parallel-agents), executing-plans. |

## Skill Mapping

How our skills map to upstream:

| This Plugin | Upstream Equivalent | Relationship |
|---|---|---|
| brainstorming | brainstorming | Adapted (creative/business domain) |
| writing-plans | writing-plans | Adapted (non-code deliverables) |
| executing-plans | executing-plans | Adapted (removed git/branch references) |
| verification-before-completion | verification-before-completion | Adapted (business verification criteria) |
| using-superpowers | using-superpowers | Adapted (knowledge-work skill list) |
| writing-skills | writing-skills | Adapted (non-code pressure scenarios) |
| systematic-problem-solving | systematic-debugging | Significantly adapted (business problems, not code bugs) |
| two-stage-review | — (part of subagent-driven-development) | Original (extracted review pattern into standalone skill) |
| feedback-reception | receiving-code-review | Significantly adapted (client/stakeholder feedback, not code review) |
| parallel-work | dispatching-parallel-agents | Adapted (knowledge-work parallelization) |

### Upstream Skills NOT Adopted (and why)

| Upstream Skill | Why Not Adopted |
|---|---|
| test-driven-development | Code-specific. The underlying principle (test before implement) is embedded in writing-skills and verification-before-completion. |
| systematic-debugging | Replaced by systematic-problem-solving, which applies the same methodology to business/operational problems. |
| requesting-code-review | Code-specific. The review pattern is captured in two-stage-review. |
| receiving-code-review | Replaced by feedback-reception, adapted for client/stakeholder feedback rather than code review. |
| using-git-worktrees | Git-specific. No knowledge-work equivalent needed. |
| finishing-a-development-branch | Git-specific. No knowledge-work equivalent needed. |
| subagent-driven-development | The two-stage review pattern was extracted into two-stage-review. The subagent dispatch pattern was adapted into parallel-work. |

## Review Process

### When to Review

- **Watch releases:** Star/watch https://github.com/obra/superpowers on GitHub. When a new version drops, review the changelog.
- **Quarterly check:** Every ~3 months, diff the shared skills against upstream to see if methodology has evolved.
- **After major upstream releases:** If upstream jumps a major version (e.g., v5 → v6), do a thorough review.

### How to Review

1. Clone or pull the latest upstream:
   ```bash
   cd /tmp && git clone https://github.com/obra/superpowers.git superpowers-upstream
   ```

2. Check the version:
   ```bash
   cat superpowers-upstream/.claude-plugin/plugin.json | grep version
   ```

3. Compare shared skills (focus on methodology changes, not code-specific content):
   - `brainstorming/SKILL.md`
   - `writing-plans/SKILL.md`
   - `verification-before-completion/SKILL.md`
   - `using-superpowers/SKILL.md`
   - `writing-skills/SKILL.md`
   - `executing-plans/SKILL.md`

4. Check for new skills that might have non-code applications:
   ```bash
   ls superpowers-upstream/skills/
   ```

5. Review any new upstream skills and ask:
   - Does the underlying pattern apply to knowledge work?
   - Would adapting this skill improve our workflow?
   - Can we extract a principle without needing the code-specific implementation?

### What to Adopt

**Always adopt:**
- Improvements to rationalization prevention (Red Flags, Forbidden Responses)
- New insights about skill triggering (CSO improvements)
- Tighter verification methodology
- Better pressure-scenario testing approaches

**Selectively adopt:**
- New skills, if the underlying pattern applies beyond code
- Structural changes to shared skills (evaluate if the change improves our version)
- New Iron Laws or discipline patterns

**Don't adopt:**
- Code-specific tooling (TDD cycles, git workflows, CI/CD patterns)
- Language-specific examples
- Platform-specific references (Claude Code CLI flags, Codex conventions)

### After Updating

1. Update the Sync Status table above
2. Bump the plugin version in `.claude-plugin/plugin.json`
3. Update the README if skills were added or removed
4. Re-package the `.plugin` file
5. Commit and push to https://github.com/montymerlin/superpowers-cowork
