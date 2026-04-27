---
name: writing-skills
description: This skill should be used when creating new knowledge-work skills, editing existing skills,
  verifying skills work correctly, or building new workflow methodologies for non-code domains. Triggers
  on "create a skill", "write a skill", "build a new workflow", "make a new skill", "improve this skill",
  "the skill isn't working", "add a new capability", or when the user wants to extend the system with
  new disciplines. Also triggers when a recurring workflow pattern is identified that should be codified.
  If there is even a 1% chance the user is trying to create, modify, or debug a skill or workflow methodology,
  invoke this skill.
---

# Writing Skills

Apply hypothesis-driven methodology to skill creation. This skill treats skill documents as testable artifacts - write them with predicted outcomes, watch agents use them, verify compliance, and close loopholes. This is how the entire Superpowers system was built, and how you extend it.

## Core Principle

**If you didn't watch an agent fail without the skill, you don't know if the skill teaches the right thing.**

Skills are not documentation. They are behavioral instructions that change how agents work. The only way to know if they work is to test them against scenarios where agents would otherwise fail.

## The Hypothesis-Driven Skill Cycle

This maps directly to scientific method and to the TDD (test-driven development) cycle that inspired the original Superpowers framework:

| Scientific Method | TDD (Code) | Skill Creation |
|---|---|---|
| Hypothesis | Write failing test | Define pressure scenario |
| Experiment | Run test, watch it fail | Run agent without skill, watch it fail |
| Theory | Write minimal code to pass | Write skill document |
| Verification | Run test, watch it pass | Run agent with skill, watch it comply |
| Refinement | Refactor, find edge cases | Close loopholes, add red flags |

## When to Use

- Creating a brand new skill for a recurring workflow
- Improving an existing skill that isn't producing good results
- Debugging why an agent isn't following a skill correctly
- Extending the Superpowers system with new disciplines
- Codifying a workflow pattern that your human partner uses repeatedly

## The Process

### Phase 1: Identify the Need

Before writing a skill, answer these questions:

1. **What behavior do you want?** Be specific. Not "better emails" but "emails that always include a clear CTA, match the brand voice, and are under 200 words."

2. **What behavior happens WITHOUT the skill?** This is critical. If the agent already does the right thing naturally, you don't need a skill. You need a skill when the agent consistently fails, takes shortcuts, or produces inconsistent results.

3. **What's the triggering condition?** When should this skill activate? Not "when writing" but "when drafting outreach to potential collaborators, gallery owners, or curators."

4. **What's the failure mode?** How will you know the skill isn't working? What does bad output look like?

### Phase 2: Design Pressure Scenarios

Before writing the skill, design 2-3 scenarios that would cause an agent to fail WITHOUT the skill. These are your "tests."

**Good pressure scenarios:**
- Realistic tasks a user would actually request
- Include time pressure, ambiguity, or complexity
- Target the specific failure mode you identified
- Have clear, observable success/failure criteria

**Pressure scenario format:**
```markdown
### Scenario: [Name]

**Task prompt:** "[What the user would say]"

**Without skill, agent typically:**
- [Failure behavior 1]
- [Failure behavior 2]

**With skill, agent should:**
- [Desired behavior 1]
- [Desired behavior 2]

**Success criteria:**
- [ ] [Observable check 1]
- [ ] [Observable check 2]
```

**Example:**
```markdown
### Scenario: Rush Proposal Request

**Task prompt:** "Quick, I need a proposal for this architect by end of day.
They want a custom lighting installation. Budget around 15k."

**Without skill, agent typically:**
- Skips brainstorming, jumps straight to writing
- Doesn't ask about scope, timeline, or technical constraints
- Produces generic proposal without brand voice
- Declares "done" without checking requirements

**With skill, agent should:**
- Invokes brainstorming skill despite time pressure
- Asks 2-3 critical questions before drafting
- Plans the proposal structure before writing
- Reviews against brief and verifies before handoff

**Success criteria:**
- [ ] Brainstorming skill invoked before writing
- [ ] At least 2 clarifying questions asked
- [ ] Plan created before prose
- [ ] Verification checklist run before "done"
```

### Phase 3: Write the Skill

Now write the skill document. Structure:

```markdown
---
name: skill-name-kebab-case
description: >
  Use when [triggering conditions - be specific and pushy].
  Also triggers on [alternative phrasings].
  If there is even a 1% chance [condition], invoke this skill.
---

# Skill Name

[One sentence: what this skill does and why it matters]

## The Iron Law

[The non-negotiable rule. ONE sentence. ALL CAPS for the rule itself.]

## When to Use
[Bullet list of triggering conditions]

## When NOT to Use
[Bullet list of exceptions]

## The Process
[Step-by-step methodology]

## Red Flags (Rationalization Prevention)
[Table of "you might think... / but actually..."]

## Forbidden Responses
[List of phrases that indicate the skill is being violated]
```

### Key Writing Principles

**1. Descriptions are for triggering, not summarizing**
The description field determines whether agents find and use the skill. It should answer one question: "Should I read this skill right NOW?" Start with "Use when..." and include specific triggers and symptoms.

**CRITICAL:** The description must ONLY describe triggering conditions. NEVER summarize the skill's process or workflow in the description. Testing revealed that when a description summarizes the workflow, agents follow the description as a shortcut instead of reading the full skill body. A description saying "reviews content for spec compliance then quality" caused agents to do cursory reviews, while "Use when reviewing any deliverable before handoff" forced them to actually read the skill's detailed process.

```yaml
# BAD: Summarizes workflow — agent may follow this instead of reading skill
description: Use when reviewing — checks spec compliance first, then quality

# GOOD: Just triggering conditions, no workflow summary
description: >
  Use when reviewing any deliverable before handoff. Triggers on
  'review this', 'check this', 'is this ready?', 'does this meet the brief?'.
```

**2. Explain the WHY**
Don't just write rules - explain why they matter. Agents with understanding outperform agents with commands.

- **Bad:** "ALWAYS check the brief before writing"
- **Good:** "Check the brief before writing because the most common failure mode is producing beautiful work that misses requirements. Checking the brief first catches this before you've invested time in prose that might need rewriting."

**3. Iron Laws use formal language**
The pattern "NO [action] WITHOUT [prerequisite] FIRST" works because it signals absolute authority. Use it sparingly - one Iron Law per skill.

**4. Red Flag tables close loopholes**
Agents rationalize. They find reasons to skip discipline, especially under pressure. The Red Flags table pre-closes these rationalizations by naming them explicitly.

**5. Forbidden Responses make violations detectable**
If you know what phrases an agent uses when violating a skill, you can catch violations. "Looks good!" without evidence = verification skill violated.

**6. Keep it under 3,000 words**
If the skill is longer than this, split it. Move reference material to a `references/` subdirectory. The skill body should be the essential instructions; deep context goes in references.

### Bulletproofing Against Rationalization

Skills that enforce discipline need to actively resist rationalization. Agents are smart and will find loopholes when under pressure. Three techniques from the upstream Superpowers methodology:

**Close every loophole explicitly.** Don't just state the rule — forbid specific workarounds:

```markdown
# Bad: Leaves escape routes
Skip brainstorming? Don't.

# Good: Closes specific loopholes
Skip brainstorming? Don't. Not for "simple" tasks. Not for "urgent" tasks.
Not because "the brief is clear." Simple tasks get simple brainstorms.
```

**Address "spirit vs letter" arguments.** Add this line early in discipline-enforcing skills:

```markdown
**Violating the letter of the rules is violating the spirit of the rules.**
```

This cuts off an entire class of "I'm following the spirit" rationalizations.

**Build rationalization tables from testing.** Every excuse agents make in pressure scenarios goes into the Red Flags table. These aren't imagined — they come from observing actual failure modes.

### Testing Different Skill Types

Different skill types need different pressure scenarios:

| Skill Type | Examples | Test With | Success Looks Like |
|---|---|---|---|
| **Discipline** (rules/gates) | verification, two-stage-review | Pressure scenarios: time + ambiguity + sunk cost combined | Agent follows rule under maximum pressure |
| **Workflow** (step-by-step) | brainstorming, writing-plans | Application scenarios + missing information tests | Agent applies technique correctly to new situation |
| **Methodology** (mental models) | systematic-problem-solving | Recognition + application + counter-examples | Agent knows when AND when NOT to apply |
| **Reception** (incoming info) | feedback-reception | Scenarios with conflicting, vague, and emotionally charged input | Agent evaluates technically before reacting |

### Phase 4: Test the Skill

Run your pressure scenarios WITH the skill loaded:

1. Present the scenario task prompt
2. Observe whether the agent follows the skill
3. Check against your success criteria
4. Note any places where the agent found loopholes or rationalized around the skill

### Phase 5: Close Loopholes

After testing, you'll likely find gaps:

**Common loopholes:**
- Agent follows the skill's letter but not its spirit
- Agent invokes the skill but skips key sections
- Agent rationalizes an exception not covered by Red Flags
- Description doesn't trigger on realistic user phrasings
- Skill is too long and agent loses track of requirements

**Closing methods:**
- Add the specific rationalization to the Red Flags table
- Add the specific phrase to Forbidden Responses
- Tighten the language (from "consider" to "MANDATORY")
- Add a "STOP" checkpoint before the commonly skipped step
- Restructure to put the most-skipped step earlier (front-loading)

### Phase 6: Iterate

Repeat Phase 4-5 until:
- All pressure scenarios pass
- No new loopholes are found
- The skill reads cleanly and isn't bloated with edge cases

## Skill Types

| Type | Purpose | Example |
|---|---|---|
| **Workflow** | Step-by-step process for a recurring task | brainstorming, writing-plans |
| **Gate** | Quality checkpoint that blocks progression | verification-before-completion, two-stage-review |
| **Methodology** | Framework for thinking about a class of problems | systematic-problem-solving |
| **Meta** | Governs how other skills work | using-superpowers, writing-skills |
| **Reception** | How to handle incoming information | feedback-reception |

## Skill Composition

Skills should declare their terminal states - what comes after them:

```
terminal(this-skill) = next-skill OR [list of possible next skills]
```

This prevents arbitrary jumping between skills. If brainstorming's terminal state is writing-plans, an agent can't jump from brainstorming to execution.

## Directory Structure

```
skill-name/
├── SKILL.md              # Core instructions (required, <3000 words)
├── references/           # Deep context loaded on demand
│   ├── examples.md       # Good/bad output examples
│   └── advanced.md       # Edge cases, advanced techniques
└── scripts/              # Utility scripts if needed
```

Keep SKILL.md lean. If you're writing reference material, it goes in `references/`.

## Red Flags (Rationalization Prevention)

| You might think... | But actually... |
|---|---|
| "I'll just write the skill without testing" | Skills without pressure tests contain loopholes. Test it. |
| "The description doesn't matter much" | The description is the PRIMARY triggering mechanism. It's critical. |
| "I'll add Red Flags later" | Red Flags are what prevent agents from rationalizing around the skill. Add them during writing. |
| "This skill is straightforward, no edge cases" | Every skill has edge cases. That's what pressure scenarios reveal. |
| "I'll make the skill comprehensive" | Comprehensive skills get skimmed. Keep it lean, move depth to references. |
| "ALWAYS and NEVER in all caps will force compliance" | Explaining WHY is more effective than shouting. Use Iron Laws sparingly. |
