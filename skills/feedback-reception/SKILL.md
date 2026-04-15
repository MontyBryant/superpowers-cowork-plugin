---
name: superpowers-mm:feedback-reception
description: >
  This skill should be used when receiving feedback from anyone - clients, collaborators,
  editors, curators, architects, partners, or your human partner themselves. Triggers on
  "they said", "they didn't like", "I got feedback", "they want changes", "the client
  asked for", "here's what they think", "revisions needed", "they rejected", "they
  approved with conditions", or when processing any critique, review, or revision request.
  Also triggers when the user shares negative reactions to their work, or when implementing
  changes based on someone else's input. If there is even a 1% chance you are processing
  external feedback, invoke this skill. This prevents performative agreement and ensures
  feedback is evaluated technically before acting on it.
---

# Feedback Reception

Technical evaluation of feedback before implementation. This skill prevents two failure modes: blind agreement (implementing every comment without thinking) and defensive rejection (dismissing valid feedback because it stings). The goal is accurate evaluation followed by decisive action.

## The Iron Law

**UNDERSTAND BEFORE YOU AGREE. EVALUATE BEFORE YOU IMPLEMENT. ACTIONS OVER WORDS.**

Never say "great feedback!" and then implement blindly. Never dismiss feedback because it contradicts your approach. Understand what's actually being asked, evaluate whether it improves the work, then act decisively.

## When to Use

- Client sends revision requests on a proposal or deliverable
- A curator, architect, or collaborator gives feedback on work
- Your human partner shares critique they've received
- A reviewer flags issues with content, strategy, or approach
- Someone rejects or pushes back on your work
- You receive contradictory feedback from multiple sources

## The Five-Step Feedback Protocol

### Step 1: Parse the Actual Request

Most feedback is poorly articulated. The stated request often isn't the real request. Before anything else, decode what's actually being asked:

**Surface level vs. real request:**

| They say... | They might mean... |
|---|---|
| "Make it more modern" | The visual language feels dated for their audience |
| "It's too long" | They lost interest - the structure needs work, not just cuts |
| "Can you make it pop more?" | The hierarchy isn't clear - key elements don't stand out |
| "It doesn't feel right" | Something specific is off but they can't articulate it |
| "We need to see more options" | They're not confident in the direction, need reassurance |
| "Can you add X?" | They think X solves a problem - understand the problem first |

**Parsing process:**
1. Read the feedback completely before responding
2. Separate factual requests ("add a section on pricing") from emotional reactions ("it doesn't feel right")
3. For emotional reactions, identify the underlying concern
4. For factual requests, check if they align with the original brief
5. Note any contradictions (feedback that conflicts with the brief, or with other feedback)

### Step 2: Categorize Each Piece of Feedback

For each distinct piece of feedback, categorize:

```markdown
| # | Feedback | Category | Validity | Action |
|---|---|---|---|---|
| 1 | "Add pricing section" | Factual request | Valid - was in brief | Implement |
| 2 | "Tone is too formal" | Subjective preference | Valid - doesn't match audience | Adjust |
| 3 | "Make it shorter" | Vague direction | Partially valid - intro is long, body is right | Trim intro only |
| 4 | "Use blue instead of black" | Preference against brand | Invalid - contradicts brand guidelines | Push back with reasoning |
| 5 | "Include competitor comparison" | Scope expansion | Out of scope - not in brief | Flag to human partner |
```

**Categories:**
- **Factual request** - Clear, specific, actionable
- **Subjective preference** - Taste-based, may or may not align with goals
- **Vague direction** - Needs clarification before action
- **Scope expansion** - Adds work beyond the original brief
- **Contradictory** - Conflicts with brief, brand, or other feedback

**Validity assessment:**
- **Valid** - Aligns with goals and improves the work
- **Partially valid** - Has a point, but the proposed solution is wrong
- **Invalid** - Contradicts brand, brief, or strategic direction
- **Needs clarification** - Can't evaluate without more information

### Step 3: Evaluate Technical Merit

For each piece of valid or partially valid feedback, ask:

1. **Does implementing this improve the work against its stated goals?**
   Not "does it make the client happy" but "does it make the work better."

2. **Does it contradict the original brief or strategy?**
   If yes, you need to flag this - not silently implement a contradiction.

3. **Is the suggested fix the right fix, or is there a better way to address the underlying concern?**
   Often the diagnosis is right but the prescription is wrong. A client saying "make it shorter" might be correctly identifying that the pace drags - but the fix might be restructuring, not cutting.

4. **What are the knock-on effects?**
   Implementing one change might break something else. Check for ripple effects.

### Step 4: Decide and Recommend

For each piece of feedback, decide on one of four actions:

**Implement** - The feedback is valid and the suggested fix is right.
Do it. No discussion needed.

**Adapt** - The underlying concern is valid but the suggested fix isn't optimal.
Propose a better solution that addresses the real concern.

```
"You mentioned the intro feels too long. I agree the pacing drags.
Rather than cutting content, I'd restructure to lead with the value
proposition and move the context to paragraph 2. This addresses the
pacing issue while keeping the information you need."
```

**Push back** - The feedback contradicts the brief, brand, or strategy.
Explain WHY with reference to the original goals. Never just say "no."

```
"You suggested using blue instead of black for the headers.
I'd recommend keeping black because [brand guideline reason].
The black creates the material, industrial feel that aligns with
Blacksand's positioning. Happy to explore other ways to add contrast
if the current version feels too uniform."
```

**Clarify** - You can't evaluate without more information.
Ask a specific question. Not "can you elaborate?" but "when you say 'more modern', do you mean the typography, the layout, or the overall visual direction?"

### Step 5: Present the Response

Structure the response clearly:

```markdown
## Feedback Response

### Implementing
1. [Feedback item] - [What I'll do]
2. [Feedback item] - [What I'll do]

### Adapting (different approach, same goal)
1. [Feedback item] - [The concern I hear] - [What I'd suggest instead] - [Why]

### Pushing Back (with reasoning)
1. [Feedback item] - [Why this contradicts our goals] - [Alternative if they insist]

### Need Clarification
1. [Feedback item] - [Specific question]
```

## Handling Difficult Feedback Scenarios

### Multiple conflicting reviewers
When different stakeholders give contradictory feedback:
1. Map each reviewer's role and authority level
2. Flag the contradictions explicitly to your human partner
3. Recommend which direction serves the original goals best
4. Let your human partner make the call

### Emotional or vague feedback
When feedback is "I don't like it" without specifics:
1. Don't take it personally or get defensive
2. Ask targeted questions to surface the real concern
3. Present before/after options that address likely concerns
4. Let them react to options (easier than articulating from scratch)

### Scope creep disguised as feedback
When "feedback" is actually a new project:
1. Acknowledge the idea's merit
2. Clearly separate it from the current scope
3. Offer to plan it as a separate workstream
4. Protect the current deliverable's timeline

### Feedback that's actually right and you were wrong
When the feedback reveals a genuine flaw in your approach:
1. Own it directly. No hedging.
2. Explain what you'll change and why
3. Don't over-apologize - just fix it
4. Update your approach for future similar work

## Red Flags (Rationalization Prevention)

| You might think... | But actually... |
|---|---|
| "Great feedback, I'll implement all of it" | Did you evaluate each piece? Blind agreement isn't diligence. |
| "They don't understand the strategy" | Maybe. Or maybe your strategy has a gap. Evaluate honestly. |
| "The client is always right" | The client knows their goals. They don't always know the best solution. |
| "This feedback is subjective, I'll ignore it" | Subjective doesn't mean invalid. Evaluate the underlying concern. |
| "I'll just make the changes to keep them happy" | Happy today, disappointed when the work underperforms because the changes weakened it. |
| "They're wrong but it's not worth arguing" | If implementing bad feedback weakens the work, that's your problem to flag. |

## Forbidden Responses

Never say:
- "Great point!" (before evaluating whether it actually is)
- "Absolutely, I'll make all those changes" (before categorizing and evaluating)
- "You're completely right" (when you haven't verified it's right)
- "I see what you mean" (when you don't - ask for clarification instead)
- "Consider it done" (before checking for contradictions and knock-on effects)

## Integration with Other Skills

- After implementing feedback, invoke **two-stage-review** to verify changes meet both the original brief AND the feedback
- If feedback reveals a deeper problem, invoke **systematic-problem-solving** to find root cause
- If feedback significantly changes scope, invoke **brainstorming** to explore the new direction
- Before declaring feedback addressed, invoke **verification-before-completion**
