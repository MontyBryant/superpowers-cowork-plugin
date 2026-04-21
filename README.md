# Superpowers for Cowork

Structured workflow discipline for creative, business, and strategic work. Adapted from Jesse Vincent's [Superpowers](https://github.com/obra/superpowers) framework for non-code knowledge work.

## What It Does

Stops Claude from winging it. Enforces a disciplined pipeline - brainstorm, plan, execute, review, verify - with hard gates at each stage. Every deliverable gets explored before execution, planned before work begins, reviewed against its brief, and verified with evidence before being called "done."

## The Three Principles

1. **The 1% Rule** - If there's even a 1% chance a skill applies, invoke it. No rationalizing.
2. **Iron Laws** - Non-negotiable rules per skill that cannot be overridden by convenience or time pressure.
3. **Evidence Over Claims** - Verification is an action, not a feeling. "Should be fine" is banned.

## Skills

| Skill | Purpose | Iron Law |
|---|---|---|
| **using-superpowers** | Meta-skill backbone. Governs all other skills. | The 1% Rule is mandatory. |
| **brainstorming** | Socratic exploration before any creative/strategic work | No execution without approved design |
| **writing-plans** | Break work into bite-sized tasks with zero ambiguity | No placeholders. No "figure it out later." |
| **verification-before-completion** | Evidence gate before any "done" claim | No completion claims without fresh evidence |
| **systematic-problem-solving** | 4-phase root cause analysis for any stuck situation | No fixes without root cause investigation |
| **two-stage-review** | Spec compliance first, quality second | Compliance before quality. Always. |
| **feedback-reception** | Technical evaluation of external feedback | Understand before agreeing. Evaluate before implementing. |
| **writing-skills** | Create new skills using hypothesis-driven methodology | Test without skill first. Then write. |
| **parallel-work** | Dispatch independent tasks to concurrent agents | One agent per independent domain. |
| **executing-plans** | Execute approved plans with verification checkpoints | Follow the plan. Stop when blocked. |

## Workflow

```
1. Receive task
2. 1% Check: which skills apply?
3. Brainstorm: explore approaches, get approval
4. Plan: break into tasks, get approval
5. Execute: work through tasks
   -> Review each task (spec, then quality)
   -> Verify each task (evidence gate)
6. Verify whole deliverable
7. Handoff with evidence
```

## Installation

### Claude Code CLI

```bash
claude plugins install github.com/montymerlin/superpowers-MM-plugin
```

### Claude Desktop (Cowork)

Install the `.plugin` file by dragging it into a Cowork chat, or install from the plugin marketplace.

### Cursor / Other MCP Hosts

Clone the repository and configure skills as MCP tool calls per your host's plugin documentation.

## Upstream Tracking

This plugin is adapted from [Superpowers](https://github.com/obra/superpowers) v5.0.7 by Jesse Vincent. It selectively adopts upstream improvements that apply to knowledge work while maintaining domain-specific adaptations. See [UPSTREAM.md](UPSTREAM.md) for the full sync history, skill mapping, and review process.

## Authorship & Lineage

**Original fork:** [Rollo Bryant](https://rollostudio.com) — created v0.1.0, adapting Jesse Vincent's [Superpowers](https://github.com/obra/superpowers) framework for creative, business, and strategic knowledge work.

**Current maintainer:** [Monty Bryant](https://github.com/montymerlin) — v0.2.0 onwards, syncing with upstream and extending for montymerlinHQ workflows.
