# HANDOFF-PROMPT: Creating Effective Successor Briefings

## Purpose

Create a handoff document that enables a successor agent to continue this work effectively, avoiding pitfalls you encountered and building on lessons you learned that aren't captured in the formal documentation.

## What Makes a Good Handoff Document

A good handoff document has these properties:

### 1. Context Without Redundancy
- **What the successor needs to know** about this session's goals and what was accomplished
- **Not** just repeating what's already in the repo documentation
- Focus on: why certain choices were made, what alternatives were considered and rejected, what subtle issues emerged

### 2. Session-Specific Intelligence
- **Mistakes made** during this session and how to avoid them
- **Dead ends explored** so successor doesn't waste time re-exploring
- **Unexpected challenges** that documentation doesn't capture
- **Working hypotheses** that proved useful or unhelpful
- **Calibration insights** about mg's working style, preferences, communication patterns

### 3. Continuation Guidance
- **Current state**: What's complete, what's in-progress, what's blocked
- **Immediate next steps**: Specific, actionable tasks ready to tackle
- **Open questions**: Decisions or clarifications needed before proceeding
- **Watch-outs**: Things that seem simple but have hidden complexity

### 4. Meta-Learning
- **What worked well** in collaboration approach
- **What didn't work** and should be done differently
- **Patterns** in how mg thinks about the work
- **Communication signals** (when mg is clarifying vs. when they're stuck vs. when they're testing ideas)

### 5. Artifact-Specific Notes
- **Files that are tricky**: Which documents have subtle interdependencies
- **Formatting quirks**: Any discovered issues with markdown, links, structure
- **Incomplete sections**: What's marked "coming soon" and what's actually planned vs. placeholder

## Structure Template

Use this structure for the handoff document:

```markdown
# Session Handoff: [Date]

## Session Summary
**Duration**: [How long this session lasted]
**Main Accomplishments**: 
- [Key deliverable 1]
- [Key deliverable 2]

**Original Intent**: [What mg wanted to achieve at session start]
**Actual Outcome**: [What actually got done, how it differed from intent]

## Mistakes and Lessons

### Mistake 1: [Description]
**What happened**: [What went wrong]
**Root cause**: [Why it went wrong]  
**How to avoid**: [Specific guidance for successor]
**Example**: [Concrete instance from this session]

[Repeat for each significant mistake]

## Dead Ends Explored

### [Topic/Approach That Didn't Work]
**Why it seemed promising**: [Initial reasoning]
**Why it failed**: [What we learned]
**Don't retry unless**: [Conditions under which this might be worth revisiting]

## Current State

### Completed This Session
- [File/artifact 1] - [Status notes]
- [File/artifact 2] - [Status notes]

### In Progress
- [File/artifact] - [What's done, what remains, any blockers]

### Not Yet Started (But Planned)
- [File/artifact] - [Priority, dependencies, notes]

## Immediate Next Steps

1. **[Most urgent task]** - [Why this should be next, what makes it ready]
2. **[Second task]** - [Context needed]
3. **[Third task]** - [Dependencies or blockers]

## Working with mg: Session-Specific Insights

### Communication Patterns Observed
- When mg [does X], it usually means [Y]
- mg prefers [approach/format/style] for [type of content]
- Watch for [signal] which indicates [state/need]

### Decision-Making Process
- [How mg approached key decisions this session]
- [What criteria seemed most important]
- [What kinds of questions helped clarify thinking]

### Preferences and Style
- [Formatting preferences noticed]
- [Level of detail preferred for different document types]
- [Balance between theory and practice mg is targeting]

## Open Questions and Decisions Needed

### Needs mg's Input
1. **[Question]** - [Why it matters, what depends on it]
2. **[Question]** - [Context for the decision]

### Needs Research/Exploration
1. **[Topic]** - [What we need to learn, why it matters]

## Technical Notes

### Repository Structure
- [Any quirks about file organization]
- [Linking conventions discovered]
- [Build/test procedures if applicable]

### Tools and Workflow
- [What tools were used (if any beyond text editor)]
- [Any automation or scripts]
- [File management approach]

## Watch-Outs for Successor

### Seems Simple But Isn't
- **[Task/file]**: [Why it's more complex than it appears]

### Hidden Dependencies
- **[File A]** depends on **[File B]** because [reason]
- Changing [X] requires updating [Y, Z]

### Quality Standards
- [What level of polish mg expects]
- [What "good enough" looks like vs. needs refinement]
- [How much theoretical depth is appropriate]

## Theoretical/Conceptual Notes

### Key Insights This Session
- [Conceptual breakthroughs or clarifications]
- [How understanding evolved during session]
- [Connections made between ideas]

### Unresolved Tensions
- [Conceptual questions still open]
- [Competing framings not yet reconciled]
- [Areas where theory and practice don't quite align]

## What Worked Well

### Collaboration Patterns
- [Approaches that were productive]
- [Types of questions that helped]
- [Format/structure choices that worked]

### Process
- [What made progress smooth]
- [Effective workflows discovered]

## What To Do Differently

### Process Improvements
- [What slowed things down]
- [Better approaches identified but not yet implemented]
- [Workflow adjustments recommended]

### Communication
- [What could have been clearer]
- [Information that should have been surfaced earlier]

## Context for Specific Files

### [Filename 1]
**Status**: [Complete/In-progress/Blocked]
**Quirks**: [Anything non-obvious about this file]
**Related to**: [Dependencies or related files]
**Notes**: [Anything successor should know]

[Repeat for files with important context]

## Session Metadata

**Agent**: Claude Sonnet 4.5
**Date**: [Date]
**mg's Goals This Session**: [As understood]
**Next Session Timing**: [If known]
**Continuation Priority**: [High/Medium/Low urgency for next session]
```

## Key Principles

1. **Be specific**: "Watch out for X" is useless. "File Y has hidden dependency on Z because of reason R" is helpful.

2. **Capture the invisible**: What seemed obvious to you in this context but won't be obvious to successor without context?

3. **Save time**: What would you want to know if you were picking this up fresh? What did you learn the hard way?

4. **Be honest**: Mistakes are valuable. Dead ends are valuable. Document them frankly.

5. **Think forward**: What will successor need to know to maintain momentum rather than starting from scratch?

6. **Prioritize ruthlessly**: Not everything needs to be in the handoff. Focus on what materially affects successor's ability to continue effectively.

## Where to Place It

Save as: `/agent/handoff-[YYYY-MM-DD].md`

This location:
- Signals its purpose (it's in agent directory, not main docs)
- Is timestamped (multiple sessions can accumulate handoffs)
- Will be found by successor looking for continuation context

## Before Finalizing

Review the handoff document and ask:

- [ ] Would this help ME if I were picking up this work in 3 months?
- [ ] Have I captured mistakes that aren't obvious from the artifacts?
- [ ] Have I documented dead ends so they won't be re-explored?
- [ ] Are next steps actually actionable, not vague?
- [ ] Have I noted mg-specific context a generic collaborator wouldn't know?
- [ ] Is anything here redundant with repo documentation (and thus should be removed)?
- [ ] Have I been specific about watch-outs rather than vague warnings?

## Example Bad vs. Good Entries

**Bad**: "Be careful with the evaluation rubrics"
- Not specific, not actionable

**Good**: "The evaluation-rubrics-reference.md has examples that reference other artifacts. If you change artifact names/structure, those examples need updating too. Caught this when we moved files and examples broke."
- Specific, explains why it matters, gives concrete scenario

**Bad**: "mg prefers good documentation"
- Everyone prefers good documentation, this says nothing

**Good**: "mg prefers examples over abstract explanation. When explaining theoretical concepts, noticed engagement increased significantly when we included concrete transcripts/examples rather than just describing patterns. The Dervin essay worked well because it had the 'strategic decision' example near the end."
- Specific observation, actionable pattern, concrete instance

**Bad**: "Some essays still need to be written"
- Obvious from essays/README.md already

**Good**: "Essay 02 (From Practice to Theory) is marked 'coming soon' but mg hasn't articulated what should be in it beyond title. Before writing, confirm: does this document the historical development of the methodology, or is it about explaining why practical techniques work? Those are different essays."
- Identifies real ambiguity, suggests clarifying question, prevents wasted effort

---

**Remember**: The handoff document is for the SUCCESSOR's benefit, not for the repository's users. It's the meta-context that helps the next agent avoid your mistakes and build on your successes. Be generous with future-you or future-other-agent.
