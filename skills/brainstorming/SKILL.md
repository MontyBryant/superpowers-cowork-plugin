---
name: brainstorming
description: >
  This skill should be used when the user asks to "brainstorm", "explore ideas",
  "think through", "design a solution", "figure out how to", "plan an approach",
  "help me think about", or any creative, strategic, or project task that requires
  exploration before execution. Also triggers on "let's think about", "what's the
  best way to", "how should I approach", "I need to figure out", or when the user
  describes a goal without a clear path. Use this skill BEFORE any execution skill.
  If there is even a 1% chance this task would benefit from structured exploration
  before jumping to execution, invoke this skill. This applies to EVERY project,
  proposal, strategy, content piece, or creative brief - no matter how simple it seems.
---

# Brainstorming

Structured Socratic exploration before any creative, strategic, or project work. This skill prevents premature execution by ensuring ideas are explored, alternatives are weighed, and your human partner approves the direction before any work begins.

## The Iron Law

**NO EXECUTION WITHOUT AN APPROVED DESIGN FIRST.**

This is not a suggestion. Not a guideline. If you begin producing deliverables, drafting content, building strategies, or taking action before the brainstorming process is complete and approved, you are violating the Iron Law. Stop. Go back. Get approval.

This applies to every project. "It's simple" is not an exemption. "I already know what they want" is not an exemption. Simple projects get simple brainstorms - but they still get brainstorms.

## When to Use

- Before any creative work (content, proposals, campaigns, brand assets)
- Before any strategic decision (pricing, partnerships, positioning)
- Before any project kickoff (events, launches, collaborations)
- Before any complex communication (pitches, negotiations, outreach sequences)
- Before any research or analysis task that has multiple possible angles

## When NOT to Use

- Quick factual questions ("What's the VAT rate in Spain?")
- Simple file operations ("Rename this file")
- Tasks where the user has already provided an explicit, detailed brief and says "just do it"
- Follow-up execution on an already-approved brainstorm

## The Process

### Phase 1: Understand Context

Before asking a single question, gather context silently:

1. Read any relevant project files, previous work, or reference materials
2. Check for existing briefs, strategies, or constraints
3. Understand what your human partner has already decided vs. what's open

Do NOT announce this step. Just do it. Come prepared.

### Phase 2: Ask Clarifying Questions

Ask questions ONE AT A TIME. Not a wall of five questions. One question, wait for the answer, then the next.

**Question design principles:**
- Multiple choice preferred (give 2-4 options plus "something else")
- Each question should meaningfully narrow the direction
- Start broad (goals, audience, constraints) then go specific (format, tone, timeline)
- Never ask what you can infer from context
- Never ask more than 5-7 questions total - respect your human partner's time

**Question sequence template:**
1. **Goal** - "What's the primary outcome you want from this?" (if not obvious)
2. **Audience** - "Who is this for?" (if not obvious)
3. **Constraints** - "Any hard constraints I should know? Budget, timeline, format?"
4. **Preferences** - "Any strong opinions on direction, or are you open?"
5. **Success criteria** - "How will you know this worked?"

Skip any question the context already answers.

### Phase 3: Propose Approaches

Present 2-3 distinct approaches. Not slight variations - genuinely different directions.

**For each approach, provide:**
- **Name** - A short, descriptive label
- **What it is** - 2-3 sentences max
- **Why it could work** - The strategic logic
- **Tradeoffs** - What you gain and what you give up
- **Effort level** - Quick estimate (light / medium / heavy)

**Format:**

```
### Approach A: [Name]
[What it is - 2-3 sentences]

**Why:** [Strategic logic]
**Tradeoffs:** [Gains vs. costs]
**Effort:** [Light / Medium / Heavy]
```

After presenting, ask: "Which direction resonates? Or should I explore a different angle?"

### Phase 4: Design the Solution

Once a direction is chosen, present the design in sections scaled to complexity:

- **Simple tasks** (email, single post, quick strategy question): 1 section, 3-5 bullet points
- **Medium tasks** (proposal, campaign, event plan): 2-3 sections with detail
- **Complex tasks** (brand strategy, business pivot, major launch): Full design document with sections, sub-sections, and specifications

**Design principles:**
- Break the work into clear, independent units
- Define the interface between units (what connects to what)
- Each unit should be verifiable on its own
- No vague language - be specific about what will be created

**Get approval after each section.** Don't dump the entire design at once. Present section by section, confirm, move to the next.

### Scope Check

Before diving deeper, assess whether the project scope needs decomposition. If the design has 5+ independent deliverables or spans multiple domains, it may need to be broken into sub-projects:

- Each sub-project should be independently deliverable
- Each should have its own clear success criteria
- They should connect at well-defined interfaces, not be entangled

If decomposition is needed, brainstorm each sub-project separately. Don't try to design everything in one pass.

### Save the Design

After your human partner approves the design direction, save it as a reference document. This becomes the source of truth for planning and verification:

```
docs/specs/YYYY-MM-DD-<topic>-design.md
```

If the project doesn't have a `docs/specs/` directory, save in whatever location makes sense — the key is that the approved design exists as a file, not just as conversation history.

### Phase 5: Self-Review the Design

Before asking for final approval, review your own design:

**Self-review checklist:**
- [ ] Are there any placeholders, TBDs, or vague instructions?
- [ ] Does every section have enough detail to execute without guessing?
- [ ] Are there any contradictions between sections?
- [ ] Does the design actually achieve the stated goal?
- [ ] Have I missed any constraints my human partner mentioned?
- [ ] Is the scope realistic for the effort level discussed?

Fix any issues found. Then present for final approval.

### Phase 6: Get Final Approval

Present the complete design summary. Ask explicitly: "Does this look right? Ready to move to planning?"

**GATE: Do not proceed until you receive explicit approval.**

Approval can be casual ("looks good", "yes", "go for it") but it must exist. Silence is not approval. Ambiguity is not approval. "Maybe" is not approval - ask what needs to change.

## Terminal State

After approval, invoke the **writing-plans** skill. Do not invoke any other execution skill directly from brainstorming. The sequence is always: brainstorm -> plan -> execute.

## Red Flags (Rationalization Prevention)

| You might think... | But actually... |
|---|---|
| "This is straightforward, I'll skip brainstorming" | Simple tasks get simple brainstorms. Skip nothing. |
| "I already know what they want" | You know what you THINK they want. Confirm it. |
| "They seem in a hurry" | Rushing guarantees rework. A 2-minute brainstorm saves a 20-minute redo. |
| "I'll just start and adjust" | Starting without direction creates sunk cost bias. Explore first. |
| "The brief is very clear" | Even clear briefs benefit from "here's my interpretation - does this match?" |
| "I asked one question, that's enough" | One question is not brainstorming. It's a checkbox. Do the process. |

## Forbidden Responses

Never say:
- "I'll go ahead and..." (before approval)
- "Let me just quickly..." (before approval)
- "Based on what you've said, I'll create..." (before presenting approaches)
- "Here's what I've done..." (if you skipped the brainstorm)

## Examples

**Good brainstorm flow:**
```
User: "I need to reach out to a curator about our Mineral series"

Claude: [Reads relevant venture files, checks network.md]
Claude: "Before I draft anything - is this a cold outreach or have you
        had prior contact?"
User: "Cold outreach"
Claude: "What's the primary goal - getting a studio visit, proposing
        for a specific show, or building the relationship first?"
User: "Building the relationship"
Claude: [Presents 3 approaches: warm intro via mutual contact,
        direct value-led email, creative mailer + follow-up]
User: "The direct value-led email"
Claude: [Designs the email structure, tone, key points]
User: "Looks good"
Claude: [Invokes writing-plans]
```

**Bad brainstorm flow:**
```
User: "I need to reach out to a curator"
Claude: "Here's a draft email: Dear [Name]..."
       ← VIOLATION: Skipped entire brainstorm
```
