---
name: superpowers-mm:executing-plans
description: >
  Use when you have an approved plan to execute — either from the writing-plans skill
  or a plan document your human partner provides. Triggers on "execute the plan",
  "follow the plan", "work through these tasks", "start executing", "run through the
  steps", or when a plan exists and the user signals readiness to begin. Also triggers
  when resuming execution of a partially completed plan. Adapted from upstream
  superpowers:executing-plans.
---

# Executing Plans

Load a plan, review it critically, execute tasks with verification at each step, and report when complete. This skill bridges the gap between planning and delivery.

## The Process

### Step 1: Load and Review Plan

1. Read the plan (file or approved design from brainstorming)
2. Review critically — identify any questions, concerns, or gaps
3. If concerns: raise them with your human partner BEFORE starting work
4. If no concerns: create a task list and proceed

**Critical review means:**
- Are any steps unclear or ambiguous?
- Are dependencies correctly ordered?
- Are there missing inputs or context?
- Does the scope still match what was approved?

Don't force through a flawed plan. Stop and ask.

### Step 2: Execute Tasks

For each task in the plan:

1. Mark as in_progress
2. Follow each step exactly as specified (the plan has bite-sized steps for a reason)
3. Invoke any skills the plan references (brainstorming for sub-problems, verification for deliverables)
4. Run verifications as specified in the plan
5. Mark as completed only after verification passes

**Between tasks:** Check if anything learned in the current task affects upcoming tasks. If so, flag it rather than silently adjusting.

### Step 3: Human Checkpoints

For complex plans (5+ tasks), check in with your human partner at natural breakpoints:

- After completing a major deliverable
- Before starting a section that requires different context or direction
- When something unexpected comes up
- At the halfway mark

Don't wait until the end to surface issues.

### Step 4: Completion

After all tasks are complete and verified:
- Run a final verification pass on the complete deliverable (invoke verification-before-completion)
- Present the work with evidence of verification
- Note any deviations from the original plan and why

## When to Stop and Ask for Help

**STOP executing immediately when:**
- Hit a blocker (missing input, dependency not met, instruction unclear)
- Plan has a gap that prevents the next step
- You don't understand what a step is asking
- Verification fails repeatedly on the same step
- You discover the plan's assumptions were wrong

**Ask for clarification rather than guessing.** A 2-minute conversation prevents a 20-minute redo.

## Red Flags (Rationalization Prevention)

| You might think... | But actually... |
|---|---|
| "I'll interpret this loosely, I know what they meant" | Plans exist so you DON'T interpret. Follow them. |
| "I'll skip this verification, I'm confident" | Confidence without evidence. Run the check. |
| "This step seems unnecessary, I'll skip it" | The plan was approved for a reason. Flag your concern, don't silently skip. |
| "I'll batch the verifications at the end" | Per-task verification catches errors early. Batching creates compounding problems. |
| "I'll adjust the plan as I go" | Adjustments need approval. Flag the change, get agreement, then proceed. |

## Integration with Other Skills

- **writing-plans** creates the plan this skill executes
- **verification-before-completion** is invoked per-task and at final completion
- **two-stage-review** applies to each deliverable within the plan
- **parallel-work** can be used when the plan contains independent tasks
- **systematic-problem-solving** applies when a task hits an unexpected problem
