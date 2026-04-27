---
name: verification-before-completion
description: 'This skill should be used for non-code knowledge work when about to claim any work is "done",
  "complete", "finished", "ready", "sent", "submitted", or "good to go". Also triggers when reviewing
  deliverables before handoff, when the user asks "is this done?", "did you check everything?", "verify
  this", "make sure this is right", or when wrapping up any task that produces a deliverable. MANDATORY:
  invoke this skill before EVERY completion claim. If there is even a 1% chance you are about to declare
  something finished, invoke this skill first. No exceptions. This is the most important quality gate
  in the entire system.'
---

# Verification Before Completion

Evidence-based verification before any completion claim. This skill prevents premature "done" declarations by requiring fresh, concrete proof that work meets specifications before claiming it is complete.

## The Iron Law

**NO COMPLETION CLAIMS WITHOUT FRESH VERIFICATION EVIDENCE.**

This is absolute. Non-negotiable. If you are about to say "done", "complete", "here you go", "all set", or any variation - STOP. Run verification first. Then make the claim WITH the evidence.

"I'm pretty sure it's right" is not verification.
"I just wrote it so it should be fine" is not verification.
"It looks good to me" is not verification.

Verification is an ACTION, not a FEELING.

## The Gate Function

Before claiming ANY status, execute this sequence. Every time. No shortcuts.

```
1. IDENTIFY  - What proof would confirm this claim?
2. CHECK     - Execute the verification (re-read, compare, test, count)
3. READ      - Study the results carefully. Don't skim.
4. CONFIRM   - Does the evidence actually support the claim?
5. ONLY THEN - State the claim WITH the evidence attached
```

### Verification Types by Deliverable

| Deliverable | Verification Action | What to Check |
|---|---|---|
| **Email draft** | Re-read against brief | Tone, key points covered, CTA present, no typos, length appropriate |
| **Proposal** | Line-by-line against requirements | Every requirement addressed, pricing correct, no placeholders |
| **Social post** | Read aloud, check constraints | Character count, hashtags, CTA, platform format correct |
| **Strategy doc** | Map recommendations to goals | Each goal addressed, logic holds, no contradictions |
| **Research** | Source check | Claims sourced, links working, data current, no hallucination |
| **Content calendar** | Cross-reference dates and channels | No date conflicts, all channels covered, realistic cadence |
| **File creation** | Open and inspect the file | Format correct, content complete, no broken elements |
| **Multi-step task** | Checklist against plan | Every task marked complete, every verification passed |

### The Full Verification Sequence

**Step 1: Gather the spec**
Pull up the original brief, approved design, or plan. This is your source of truth.

**Step 2: Create a verification checklist**
For each requirement in the spec, write a yes/no verification item:

```
- [ ] Opening paragraph leads with material innovation (per brief)
- [ ] Three pricing tiers included (per requirements)
- [ ] Tone matches voice_core.md guidelines
- [ ] Word count within specified range
- [ ] All links/references are real and working
- [ ] No placeholder text remaining
```

**Step 3: Execute each check**
Go through the checklist one by one. For each item:
- Re-read the relevant section of the deliverable
- Compare against the spec requirement
- Mark pass or fail with evidence

**Step 4: Address failures**
If any check fails:
- Fix the issue
- Re-run that specific verification
- Do NOT just fix and declare done - verify the fix worked

**Step 5: Final declaration**
Only after every check passes, state completion WITH a summary:

```
"Done. Verified against the brief:
- Opening leads with material innovation [check]
- Three pricing tiers included [check]
- Tone matches voice guidelines [check]
- Word count: 487 (target was 400-500) [check]
- No placeholders remaining [check]"
```

## Forbidden Wording

These phrases are BANNED when claiming completion. If you catch yourself writing any of these, STOP and run verification:

- "should be" / "should work"
- "probably" / "most likely"
- "seems to" / "appears to"
- "I think it's" / "I believe it's"
- "Great!" / "Perfect!" / "Done!" (without verification evidence)
- "All set!" (without listing what was verified)
- "Here you go" (without confirmation of spec compliance)
- "I'm confident that..." (confidence is not evidence)
- "Looks good" (to whom? against what criteria?)

## Allowed Wording

These phrases are fine because they include or imply evidence:

- "Verified against the brief - all 5 requirements met"
- "Checked: word count is 487, tone matches guidelines, all links working"
- "Done. Here's what I confirmed: [list]"
- "Complete - ran through the verification checklist, everything passes"

## Common Verification Failures

| Failure Mode | What Goes Wrong | Prevention |
|---|---|---|
| **Recency bias** | "I just wrote it, it must be right" | Always re-read from the top as if seeing it for the first time |
| **Partial verification** | Checking 3 of 7 requirements | Use a checklist. Check every item. |
| **Confirmation bias** | Reading the work looking for correctness | Read looking for ERRORS. Assume something is wrong. Find it. |
| **Spec drift** | Verifying against what you remember, not the actual spec | Pull up the original brief/plan. Compare directly. |
| **Skipping edge cases** | "The main content is right" | Check headers, footers, links, formatting, dates, names, numbers |
| **Trust without verify** | Accepting subagent claims at face value | Re-verify any claim made by a subagent or prior task |

## Red Flags (Rationalization Prevention)

| You might think... | But actually... |
|---|---|
| "This is simple, I don't need to verify" | Simple work has simple verification. Do it anyway. |
| "I'm confident it's right" | Confidence without evidence is guessing. Verify. |
| "The user is waiting" | A 30-second verification prevents a 10-minute redo. |
| "I already checked while writing" | Writing-mode and verification-mode are different mindsets. Re-check. |
| "It's just a draft, it doesn't need to be perfect" | Drafts still need to meet the brief. Verify against spec. |
| "I'll just send it and fix later" | "Fix later" is debt. Verify now. |
| "Should work now" | "Should" is not evidence. Run the check. |
| "I'm tired of this task, just ship it" | Fatigue is when errors happen most. That's exactly when verification matters. |
| "I already verified the previous version" | Verification from a prior run is stale. Fresh evidence only. |

**The key pattern:** Any thought that uses "should", "probably", or "seems" before verification is a red flag. These words indicate PREDICTION, not EVIDENCE. Catch them, stop, and verify.

## Special Cases

### Verification for research tasks
- Every factual claim has a source
- Sources are real (not hallucinated)
- Data is current (check dates)
- Conclusions follow from evidence (not assumed)

### Verification for creative work
- Matches the approved tone/voice
- Meets any word count or format constraints
- Key messages are present (compare to brief)
- Nothing contradicts brand guidelines

### Verification for multi-part deliverables
- Each part individually verified
- Parts are consistent with each other (no contradictions)
- Transitions between parts are smooth
- The whole is greater than the sum (read the complete piece end-to-end)

## Integration with Other Skills

- After **writing-plans** execution: verify each task's completion before marking done
- After **two-stage-review**: verification confirms review findings were addressed
- Before ANY handoff to your human partner: mandatory verification gate
- **If `agentic-scaffold:repo-audit` is installed** and the session touched any scaffold artifacts (CHANGELOG, DECISIONS, ROADMAP, version files): run it as a final check before declaring the session complete. It catches stale changelogs, version drift, and ROADMAP/DECISIONS gaps that are easy to miss when focused on content work.
