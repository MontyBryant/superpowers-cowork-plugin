---
name: superpowers-mm:systematic-problem-solving
description: >
  This skill should be used when the user has a problem, challenge, or issue that
  needs diagnosing - business problems, underperformance, operational bottlenecks,
  strategic questions, relationship issues, brand positioning challenges, or anything
  that isn't working as expected. Triggers on "why isn't this working", "what's going
  wrong with", "help me figure out", "diagnose this", "troubleshoot", "I'm stuck",
  "this isn't performing", "what should I do about", "how do I fix", or any situation
  where something is broken, stuck, or underperforming. Use ESPECIALLY when under
  time pressure, when "just one quick fix" seems obvious, when multiple attempts have
  already failed, or when the root cause is unclear. If there is even a 1% chance the
  user is dealing with a problem rather than a creation task, invoke this skill.
---

# Systematic Problem-Solving

Four-phase root cause analysis adapted from systematic debugging methodology. This skill prevents symptom-chasing by requiring thorough investigation before any fixes are proposed. It works for business problems, creative blocks, operational issues, relationship challenges, and strategic questions.

## The Iron Law

**NO FIXES WITHOUT ROOT CAUSE INVESTIGATION FIRST.**

Complete ALL FOUR PHASES before proposing solutions. Not after Phase 1. Not after you think you've spotted the issue. All four phases.

"I think I see the problem" is not root cause identification.
"The obvious fix is..." means you haven't investigated enough.
"Let's just try..." is symptom-chasing, not problem-solving.

## When to Use

- Revenue is down or stagnant and you don't know why
- A campaign, launch, or outreach isn't getting results
- A relationship or collaboration is stuck or deteriorating
- Operations are inefficient or bottlenecked
- A strategy isn't producing expected outcomes
- You've tried multiple fixes and nothing is working
- Time pressure is making you want to skip investigation

**Use ESPECIALLY when:**
- The fix seems "obvious" (obvious fixes are often wrong)
- You're under pressure to act fast (rushing guarantees rework)
- Multiple fixes have already been tried (the real cause hasn't been found)
- The problem keeps recurring (symptom fixes don't last)

## Phase 1: Root Cause Investigation

### Read the signals carefully

Don't skip past symptoms or dismiss them. Every signal matters:
- What exactly is happening? (Not what you assume is happening)
- When did it start? What changed around that time?
- Is it consistent or intermittent?
- What have you already tried? What were the results?

### Reproduce the problem

Can you observe the problem directly? Get specific:
- What are the exact numbers? (Not "sales are down" but "sales dropped 23% month-over-month in March")
- What are the exact symptoms? (Not "outreach isn't working" but "sent 15 emails, 2 opens, 0 replies")
- Is this happening everywhere or in specific areas?

If you can't observe the problem directly, gather more data. Don't guess.

### Check recent changes

What changed that could cause this?
- New competitors, market shifts, seasonal patterns
- Changes to your process, team, tools, or approach
- Changes in the audience, platform, or channel
- External factors (economy, regulations, trends)

### Trace the data flow

For problems that cross multiple systems or touchpoints, trace the path:

```
For EACH stage in the process:
  - What enters this stage? (inputs)
  - What happens here? (transformation)
  - What exits this stage? (outputs)
  - Is the output what you'd expect?

Find WHERE the breakdown occurs.
THEN investigate that specific stage.
```

**Example - "Our proposals aren't converting":**
```
Lead source -> Initial contact -> Discovery call -> Proposal sent -> Follow-up -> Close

Stage check:
- Lead source: Getting 10 qualified leads/month [OK]
- Initial contact: 8 of 10 respond [OK]
- Discovery call: 6 of 8 agree to call [OK]
- Proposal sent: 6 proposals sent [OK]
- Follow-up: 2 of 6 engage after proposal [BREAKDOWN HERE]
- Close: 1 of 2 closes [OK]

The problem isn't "proposals don't convert" - it's
"something happens between sending the proposal and follow-up
that loses 4 of 6 prospects."
```

## Phase 2: Pattern Analysis

### Find working examples

Look for similar situations that ARE working:
- Which outreach emails DO get replies? What's different about them?
- Which products DO sell well? What do they have that others don't?
- Which relationships ARE progressing? What's different about those?
- What worked in the past that isn't working now?

### Compare against references

If you have benchmarks, best practices, or past performance data, compare:
- What does "good" look like in this domain?
- Where does current performance diverge from the benchmark?
- What do the successful examples have in common?

### Identify every difference

Between working and broken, list EVERY difference. Not just the obvious ones:
- Timing, format, channel, audience, tone, length
- Context, relationship stage, market conditions
- Who's involved, what tools are used, what process is followed

Small differences often matter most.

### Map dependencies

What does the broken thing depend on?
- Other people, systems, or processes?
- External factors you don't control?
- Assumptions that might be wrong?

## Phase 3: Hypothesis and Testing

### Form a single hypothesis

"I think [X] is the root cause because [Y evidence from Phases 1-2]."

Not "it could be A or B or C." Pick one. The one with the most evidence. Be specific:

- **Bad:** "I think the marketing isn't working"
- **Good:** "I think the proposal follow-up timing is the issue - we're waiting 7 days, and the evidence shows prospects go cold after 3 days based on email open data"

### Design a test

How can you prove or disprove this hypothesis?

- What would you observe if the hypothesis is correct?
- What would you observe if it's wrong?
- What's the smallest, fastest test you can run?

**Test design principles:**
- Test one variable at a time
- Define success criteria BEFORE running the test
- Set a time limit for the test
- Plan what you'll do if the test confirms OR denies the hypothesis

### Run the test

Execute the test. Collect evidence. Don't interpret results through confirmation bias - look for what actually happened, not what you wanted to happen.

### If proven: Move to Phase 4
### If disproven: Form a new hypothesis from the evidence. Repeat Phase 3.

## Phase 4: Fix at Source

### Fix the root cause, not the symptom

| Symptom Fix (BAD) | Root Cause Fix (GOOD) |
|---|---|
| Send more emails to compensate for low response rate | Fix the email content/targeting that causes low response |
| Discount prices because proposals don't close | Fix the proposal timing/content that loses prospects |
| Post more content because engagement is low | Fix the content strategy that creates low-engagement posts |
| Hire more people because the team is overwhelmed | Fix the process that creates unnecessary work |

### Implement with defense in depth

1. **Fix the source** - Address the actual root cause
2. **Add a guard** - Put a check at the symptom point too (catches future issues)
3. **Add monitoring** - How will you know if the problem returns?

### Verify the fix

After implementing:
- Does the original symptom still occur?
- Has the metric improved?
- Are there any new problems introduced by the fix?
- Set a check-in date to confirm the fix holds

## Output Format

Present findings in this structure:

```markdown
## Problem Analysis: [Problem Name]

### Symptoms Observed
[What's actually happening - with specific data]

### Root Cause
[What investigation revealed - with evidence chain]

### Recommended Fix
[Action to take at the source]

### Guard Rails
[How to prevent recurrence]

### Verification Plan
[How we'll know the fix worked]

### Timeline
[When to check results]
```

## Red Flags (Rationalization Prevention)

| You might think... | But actually... |
|---|---|
| "Just one quick fix" | Quick fixes are symptom patches. Find root cause first. |
| "This seems simple" | Simple problems have root causes too. Investigate. |
| "I'm in a hurry" | Rushing guarantees rework. 10 minutes of investigation saves days. |
| "I've seen this before" | Maybe. But verify - same symptoms can have different causes. |
| "Let's just try something" | Trying without hypothesizing is random. Hypothesize first. |
| "The user wants action, not analysis" | The user wants the problem SOLVED, which requires understanding it. |
| "We can always undo it" | Some fixes create new dependencies. Understand before acting. |

## Forbidden Responses

Never say:
- "Let's just try X and see what happens" (without a hypothesis)
- "The obvious solution is..." (obvious to whom? based on what evidence?)
- "I think the problem is X" (before completing investigation)
- "Here are 5 things that might help" (scattershot is not systematic)
- "Have you tried..." (before understanding the problem yourself)
