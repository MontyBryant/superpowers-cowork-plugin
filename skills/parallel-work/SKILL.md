---
name: parallel-work
description: Use for non-code knowledge work when facing 2+ independent tasks, deliverables, or investigations
  that can be worked on without shared dependencies or sequential constraints. Triggers on "these are
  independent", "do these in parallel", "multiple deliverables", "batch these", "work on all of these",
  or when a plan contains tasks that don't depend on each other. Also applies when troubleshooting multiple
  unrelated problems simultaneously.
---

# Parallel Work

Dispatch independent tasks to separate agents working concurrently. Instead of working through tasks sequentially, identify which ones are truly independent and run them in parallel — completing in the time of one instead of the time of many.

**Core principle:** Dispatch one agent per independent problem domain. Let them work concurrently. Review and integrate when they return.

## When to Use

```
Multiple tasks or deliverables?
  ├── yes → Are they independent (no shared inputs or dependencies)?
  │          ├── yes → Can agents work without interfering?
  │          │          ├── yes → PARALLEL DISPATCH
  │          │          └── no (shared resources) → Sequential agents
  │          └── no (related) → Single agent handles all
  └── no → Normal single-task execution
```

**Use when:**
- 3+ deliverables that don't depend on each other
- Multiple research threads across different domains
- Several independent problems to diagnose simultaneously
- Batch content creation where pieces don't reference each other
- Parallel audit or review of unrelated items

**Don't use when:**
- Tasks are related (output of one feeds into another)
- Need to maintain a consistent voice/thread across deliverables
- Tasks would reference the same evolving document
- You don't yet understand the scope (investigate first, parallelize later)

## The Pattern

### 1. Identify Independent Domains

Group tasks by what they touch. Each domain should be self-contained:
- Research on Topic A doesn't affect Research on Topic B
- Proposal Section 1 doesn't depend on Section 3
- Problem in Process X is unrelated to Problem in Process Y

### 2. Create Focused Agent Tasks

Each agent gets:
- **Specific scope:** One deliverable or investigation
- **Clear goal:** What "done" looks like
- **All context needed:** Don't assume the agent has your conversation history
- **Constraints:** What NOT to touch or change
- **Expected output:** What to return (summary, file, findings)

**Good agent prompt:**
```markdown
Research the current landscape of ecological credit registries in Southeast Asia.

Context: We're writing a market analysis for Bridging Worlds. The Southeast
Asia section is one of four regional sections being researched in parallel.

Scope: Southeast Asia only (Thailand, Vietnam, Indonesia, Philippines,
Malaysia, Singapore, Cambodia, Myanmar, Laos).

Deliverable: A markdown file with:
- Active registries and their focus areas
- Volume of credits issued (last 12 months if available)
- Key projects and methodologies
- Emerging trends

Save to: research/bridging-worlds/references/2026-04-08_SEA-Credit-Registries.md

Do NOT cover other regions - those are being researched separately.
```

**Bad agent prompt:**
"Research ecological credits" — too broad, no constraints, no output format.

### 3. Dispatch in Parallel

Launch all independent agents simultaneously. Don't wait for one to finish before starting the next — that defeats the purpose.

### 4. Review and Integrate

When agents return:
1. **Read each result** — understand what was produced
2. **Check for conflicts** — did agents make contradictory assumptions?
3. **Verify quality** — run two-stage-review on each deliverable
4. **Integrate** — combine results, ensure consistency across the whole
5. **Fill gaps** — parallel work sometimes reveals gaps between domains

## Common Mistakes

| Mistake | Fix |
|---|---|
| Scope too broad ("handle everything") | One clear deliverable per agent |
| Missing context (agent doesn't know the project) | Include all necessary background in the prompt |
| No output format specified | Tell the agent exactly what to return |
| Dispatching related tasks in parallel | If Task B depends on Task A's output, run them sequentially |
| Skipping the integration step | Always review the combined output for consistency |

## Red Flags (Rationalization Prevention)

| You might think... | But actually... |
|---|---|
| "I'll just do these one at a time, it's easier" | Sequential work on independent tasks wastes time. Parallelize. |
| "These might be related" | If you can't name the specific dependency, they're independent. |
| "I'll parallelize later" | If tasks are independent NOW, dispatch NOW. |
| "One big agent can handle all of this" | Focused agents with narrow scope produce better results than one agent juggling everything. |

## Integration with Other Skills

- After **writing-plans**: scan the plan for independent tasks — candidates for parallel dispatch
- Each parallel agent should invoke **verification-before-completion** before returning
- After integration, run **two-stage-review** on the combined deliverable
