---
name: superpowers-mm:writing-plans
description: >
  This skill should be used when a brainstorming session has been approved and
  work needs to be broken into executable tasks, when the user asks to "make a
  plan", "break this down", "create an action plan", "what are the steps",
  "help me plan", "write a project plan", or "organize this into tasks". Also
  triggers when a project, campaign, proposal, or multi-step deliverable needs
  structured decomposition before execution. If there is even a 1% chance that
  breaking work into smaller tasks would improve the outcome, invoke this skill.
  Every multi-step task gets a plan. No exceptions.
---

# Writing Plans

Break approved designs into bite-sized, fully-specified tasks. Each task takes 2-5 minutes, has zero ambiguity, and includes verification steps. This skill prevents vague execution by demanding complete specifications before any work begins.

## The Iron Law

**NO EXECUTION WITHOUT A COMPLETE PLAN. NO PLACEHOLDERS. NO "FIGURE IT OUT LATER."**

Every task in the plan must be specific enough that someone with zero context could execute it. If a task says "add appropriate content" or "handle this part" - the plan is not done. Rewrite it.

## When to Use

- After brainstorming approval (mandatory next step)
- When a project has 3+ distinct deliverables or steps
- When coordinating work across multiple files, channels, or stakeholders
- When the user provides a complex brief that needs decomposition
- Before any execution that would take more than 5 minutes

## When NOT to Use

- Single-step tasks that are already fully specified
- When the user explicitly says "just do it, no plan needed"
- Quick fixes or minor edits to existing work

## The Process

### Step 1: Scope Check

Read the approved design (from brainstorming) or the user's brief. Ask:

- Does this cover multiple independent workstreams?
- Can parts be delivered and verified independently?

If yes, break into separate plans. Each plan should produce a complete, verifiable deliverable on its own. Don't create one mega-plan for unrelated workstreams.

### Step 2: Map the Deliverables

Before defining tasks, list every deliverable and its purpose:

```
| Deliverable | Purpose | Format | Audience |
|---|---|---|---|
| Curator email | Build relationship | Email draft (.md) | V&A curator |
| Follow-up sequence | Stay top of mind | 3-email sequence (.md) | Same |
| Portfolio PDF | Support the pitch | PDF attachment | Same |
```

This map drives the task breakdown. Every deliverable must appear in at least one task.

### Step 3: Write Bite-Sized Tasks

Each task takes 2-5 minutes and covers ONE action. Not "write and review the email." That's two tasks: "write the email" and "review the email against the brief."

**Task specification format:**

```markdown
### Task N: [Clear Action Name]

**Deliverable:** [What this task produces]
**Inputs needed:** [Files, context, references to load]
**Skills to invoke:** [Any superpowers skills that apply]

- [ ] **Step 1:** [Exact action]
  - Detail: [Specific enough to execute without guessing]
  - Expected output: [What "done" looks like]

- [ ] **Step 2:** [Exact action]
  - Detail: [Specific enough to execute without guessing]
  - Expected output: [What "done" looks like]

**Verification:** [How to confirm this task is complete and correct]
```

### Step 4: The No Placeholders Rule

Scan every task for these violations. If found, rewrite immediately:

**Never write:**
- "TBD", "TODO", "figure out later", "to be determined"
- "Add appropriate content" (appropriate HOW? specify)
- "Similar to Task N" (repeat the actual specification)
- "Handle the formatting" (what formatting, exactly?)
- "Research this further" (research WHAT, WHERE, and WHAT are you looking for?)
- "Include relevant details" (which details? list them)
- Vague verbs: "address", "handle", "deal with", "take care of"

**Always write:**
- Exact content specifications ("Write a 150-word opening paragraph that leads with the Mineral series' material innovation")
- Exact file references ("Load voice/voice_core.md and voice/voice_persuasion.md")
- Exact verification steps ("Read the email aloud - does it sound like a human wrote it?")
- Exact success criteria ("The proposal includes pricing for 3 tiers: commission, licensing, and consultation")

### Step 5: Sequencing and Dependencies

Order tasks logically. Mark dependencies explicitly:

```
Task 1: Research curator's recent exhibitions [no dependencies]
Task 2: Draft email opening [depends on Task 1]
Task 3: Write value proposition section [depends on Task 1]
Task 4: Assemble full email [depends on Tasks 2, 3]
Task 5: Review against brief [depends on Task 4]
```

Tasks without dependencies can run in parallel (if using subagents).

### Step 6: Plan Document Structure

Write the complete plan in this format:

```markdown
# [Project Name] - Execution Plan

> **Approved design:** [Link to or summary of the brainstorm output]

**Goal:** [One sentence]
**Deliverables:** [List]
**Estimated total time:** [Realistic estimate]

---

### Task 1: [Name]
[Full specification per Step 3 format]

### Task 2: [Name]
[Full specification per Step 3 format]

[... all tasks ...]

---

## Verification Checklist

- [ ] Every requirement from the approved design is covered by at least one task
- [ ] No task contains placeholders or vague instructions
- [ ] Every task has a verification step
- [ ] Dependencies are marked and sequencing is logical
- [ ] Total scope matches the effort level discussed in brainstorming
```

### Step 7: Self-Review

Before presenting the plan, run this checklist:

1. **Design coverage:** Can you point to a task implementing each requirement from the approved design?
2. **Placeholder scan:** Any "TBD", vague instructions, or missing specifications?
3. **Consistency check:** Do references between tasks match? (e.g., if Task 3 says "use the tone from Task 2", does Task 2 actually define a tone?)
4. **Verification completeness:** Does every task have a way to confirm it's done correctly?
5. **Scope check:** Is this plan realistic? Too ambitious? Too thin?

Fix any issues before presenting.

### Step 8: Present and Get Approval

Show the plan to your human partner. Ask: "Does this breakdown look right? Any tasks missing or unnecessary?"

**GATE: Do not begin execution until the plan is approved.**

### Step 9: Execution Handoff

After approval, begin executing tasks in order. For each task:

1. Mark it as in_progress
2. Load specified inputs
3. Invoke specified skills
4. Execute the steps
5. Run the verification
6. Mark as complete
7. Move to next task

If a task reveals something unexpected (new information, changed requirements, a blocker), STOP. Do not improvise. Flag it to your human partner and adjust the plan.

## Task Granularity Guide

| Project Type | Tasks | Granularity |
|---|---|---|
| Single email or post | 2-4 tasks | Research, draft, review |
| Proposal or pitch | 4-8 tasks | Research, structure, sections, review, polish |
| Campaign or launch | 8-15 tasks | Strategy, assets, copy, scheduling, review per channel |
| Major strategy | 5-10 tasks | Analysis, options, recommendation, implementation steps |

## Red Flags (Rationalization Prevention)

| You might think... | But actually... |
|---|---|
| "This is just one email, no plan needed" | Even one email has: research, draft, review. That's 3 tasks. Plan it. |
| "I'll figure out the details as I go" | That's how you end up redoing work. Specify now. |
| "The user seems impatient, I'll skip planning" | A 2-minute plan prevents a 15-minute redo. |
| "I know the format already" | Write it down anyway. Explicit beats implicit. |
| "This task is self-explanatory" | Self-explanatory to you, maybe. Specify the verification step at minimum. |

## Forbidden Responses

Never say:
- "I'll work through this step by step" (without writing an actual plan first)
- "Let me start with..." (before presenting the plan)
- "Here's what I've done so far..." (if you skipped planning)
- "I'll handle the rest similarly" (specify each task individually)
