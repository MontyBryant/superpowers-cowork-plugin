---
name: superpowers-knowledge:two-stage-review
description: >
  This skill should be used when reviewing any deliverable before handoff - emails,
  proposals, content, strategy documents, presentations, research, or any work product.
  Triggers on "review this", "check this", "is this ready?", "give me feedback",
  "critique this", "proofread", "quality check", "does this meet the brief?", or
  when a task from writing-plans has been completed and needs review before the next
  task begins. Also triggers automatically after any content creation or editing task.
  If there is even a 1% chance a deliverable would benefit from structured review
  before being shared, invoke this skill. Every deliverable gets reviewed. No exceptions.
  Original knowledge-work skill — no upstream Superpowers equivalent. Applies spec
  compliance then quality review to any deliverable. Adds unique value even when the
  official Superpowers plugin is also installed.
---

# Two-Stage Review

Structured quality gate with two distinct passes: spec compliance first, then quality. This separation matters because a beautifully written email that misses a key requirement is still a failure. Check requirements first, polish second.

## The Iron Law

**SPEC COMPLIANCE BEFORE QUALITY. ALWAYS. IN THAT ORDER.**

Never polish prose before confirming the content meets requirements. Never comment on tone before checking that every requirement is addressed. The order is non-negotiable because fixing a missed requirement often means rewriting sections, which invalidates quality feedback.

## When to Use

- After completing any deliverable (email, proposal, content, strategy doc)
- Before sharing any work with your human partner for final approval
- When asked to review or critique any existing work
- After implementing feedback or revisions (re-review needed)
- Between tasks in a plan (each task output gets reviewed)

## Stage 1: Spec Compliance Review

### Purpose
Does the deliverable meet every requirement from the brief, approved design, or plan?

### Process

**Step 1: Pull up the source of truth**
- The original brief, plan, or approved design
- Any specific requirements the user mentioned
- Any constraints (word count, format, audience, tone)

**Step 2: Create a requirement checklist**
Extract EVERY requirement and create a yes/no checklist:

```markdown
## Spec Compliance Check

Source: [Brief/Plan/Approved Design reference]

### Requirements
- [ ] [Requirement 1 from brief]
- [ ] [Requirement 2 from brief]
- [ ] [Requirement 3 from brief]
...

### Constraints
- [ ] Word count: [target] | Actual: [count]
- [ ] Format: [required format]
- [ ] Audience: [specified audience]
- [ ] Tone: [specified tone]

### Completeness
- [ ] No placeholder text remaining
- [ ] No TODO or TBD items
- [ ] All sections present
- [ ] Nothing extra added that wasn't requested
```

**Step 3: Check each item**
Go through one by one. For each requirement:
- Find it in the deliverable
- Confirm it's adequately addressed (not just mentioned - actually fulfilled)
- Mark pass or fail

**Step 4: Address failures**
For each failed item:
- Note exactly what's missing or wrong
- Specify what needs to change
- Do NOT fix it yet if there are multiple failures - list them all first, then fix in batch

**Step 5: Re-check after fixes**
After fixing failures, re-run the checklist. Don't assume the fix worked.

### Severity Levels

| Level | Definition | Action |
|---|---|---|
| **Critical** | A core requirement is missing or wrong | Must fix before proceeding. Cannot move to Stage 2. |
| **Important** | A secondary requirement is incomplete | Must fix before handoff. Can proceed to Stage 2 in parallel. |
| **Minor** | A nice-to-have is missing | Note for later. Proceed to Stage 2. |

**GATE: All Critical items must be resolved before moving to Stage 2.**

## Stage 2: Quality Review

### Purpose
Is the deliverable well-crafted? Does it achieve its intended effect?

### Quality Dimensions

Review across these dimensions, weighted by deliverable type:

**For written content (emails, proposals, posts):**

| Dimension | What to Check |
|---|---|
| **Clarity** | Can the reader understand the message on first read? No ambiguous sentences? |
| **Flow** | Does each paragraph lead naturally to the next? Is the rhythm varied? |
| **Voice** | Does it sound like a human wrote it? Does it match brand/personal voice? |
| **Impact** | Does the opening hook? Does the CTA compel action? |
| **Economy** | Can any sentence be cut without losing meaning? Is it lean? |
| **Accuracy** | Are facts correct? Names spelled right? Numbers accurate? |

**For strategic work (plans, analyses, recommendations):**

| Dimension | What to Check |
|---|---|
| **Logic** | Does the reasoning hold? Are conclusions supported by evidence? |
| **Completeness** | Are counterarguments addressed? Risks acknowledged? |
| **Actionability** | Can someone act on these recommendations? Are next steps clear? |
| **Prioritization** | Is it clear what matters most? Is sequencing logical? |
| **Realism** | Are recommendations feasible given constraints? |

**For research:**

| Dimension | What to Check |
|---|---|
| **Sourcing** | Are claims supported? Sources credible and current? |
| **Balance** | Are multiple perspectives represented? |
| **Depth** | Is the analysis deep enough to be useful? |
| **Relevance** | Does every section serve the stated purpose? |
| **Freshness** | Is the data current? No outdated information? |

### Quality Review Process

**Step 1: Read the entire piece fresh**
Read from beginning to end without stopping to fix things. Note impressions:
- Where did you stumble?
- What felt weak?
- What worked well?

**Step 2: Score each quality dimension**
For each relevant dimension, rate 1-5:
- 1: Needs major rework
- 2: Significant issues
- 3: Acceptable, could improve
- 4: Good, minor polish possible
- 5: Excellent, no changes needed

**Step 3: Provide specific feedback**
For any dimension scored 3 or below, provide:
- The specific issue (quote the problematic section)
- Why it's a problem
- A concrete suggestion for improvement

**Step 4: Prioritize fixes**
Don't dump 20 nitpicks. Prioritize:
- Fix anything scored 1-2 (mandatory)
- Fix anything scored 3 that's in a high-impact section (opening, CTA, key argument)
- Note anything scored 3 in low-impact sections (optional polish)
- Don't touch 4-5 scores unless you can make them meaningfully better

### Quality Review Output Format

```markdown
## Quality Review

### Overall Assessment
[One sentence summary - is this ready, close, or needs work?]

### Strengths
- [What works well - be specific]

### Issues (by priority)

**Must Fix:**
1. [Issue] - [Where] - [Suggested fix]

**Should Fix:**
1. [Issue] - [Where] - [Suggested fix]

**Optional Polish:**
1. [Issue] - [Where] - [Suggested fix]

### Dimension Scores
| Dimension | Score | Notes |
|---|---|---|
| Clarity | 4 | Strong throughout |
| Flow | 3 | Para 2-3 transition is abrupt |
| Voice | 4 | Matches brand well |
| Impact | 2 | Opening doesn't hook - needs rework |
| Economy | 3 | Could trim 15% without losing anything |
```

## Combined Review Output

When presenting both stages to your human partner:

```markdown
## Review: [Deliverable Name]

### Stage 1: Spec Compliance
[Checklist results - pass/fail per requirement]
Critical issues: [count]
Status: [PASS / BLOCKED - fix required]

### Stage 2: Quality
[Dimension scores and prioritized feedback]
Must-fix issues: [count]
Status: [READY / NEEDS WORK]

### Overall Recommendation
[Ship / Fix and re-review / Major rework needed]
```

## Red Flags (Rationalization Prevention)

| You might think... | But actually... |
|---|---|
| "I'll review quality and compliance together" | No. Separate passes catch different things. Do them in order. |
| "This is clearly well-written, skip to quality" | Check compliance first. Beautiful writing that misses the brief is a failure. |
| "The user didn't give a detailed brief" | Work with what you have. Even vague briefs have implicit requirements. |
| "I wrote this myself, I know it's right" | Author blindness is real. Review it as if seeing it for the first time. |
| "Minor issues, not worth flagging" | Flag everything. Let your human partner decide what matters. |
| "I'll just fix things as I find them" | List all issues first, then fix in batch. Fixing mid-review creates blind spots. |

## Forbidden Responses

Never say:
- "Looks good!" (without having run both stages)
- "Just a few minor tweaks" (without the compliance check)
- "I've reviewed it and it's ready" (without showing the review)
- "The quality is great" (before confirming spec compliance)
