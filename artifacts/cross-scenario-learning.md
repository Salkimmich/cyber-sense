# Cross-Scenario Learning: Building Institutional Memory

## The Problem: Amnesia by Design

Every new conversation with an LLM starts fresh. No memory of past deliberations. No accumulated wisdom. No institutional knowledge.

This is by design—conversation isolation prevents context bleed and protects privacy. But it creates a critical problem for iterative sense-making:

**You keep relearning the same lessons.**

Your adversarial committee debates hiring decisions in Q2. They discover that historical analogies need explicit detail about what's actually analogous (low reasoning completeness score).

In Q4, you face another hiring decision. The committee makes the same mistake. The independent evaluation flags the same problem. You iterate and fix it.

**But the lesson doesn't transfer. The system has amnesia.**

## The Solution: Explicit Knowledge Transfer

**Cross-scenario learning** means:
- Extracting lessons from past deliberations
- Storing them in accessible formats
- Injecting relevant lessons into new deliberations
- Building a library of patterns that improve over time

You're creating **institutional memory for AI collaboration**—not by magically giving the model memory, but by explicitly managing what context gets loaded when.

## The Core Mechanism: Lesson Extraction

After each deliberation cycle (committee → Robert's Rules → independent evaluation → iteration), you extract:

### 1. What Worked
Patterns that produced high evaluation scores and useful outputs.

**Example**:
```
LESSON: Explicit trade-off quantification (2024-Q2-hiring)

When Joe and Frankie disagreed about juniors vs. seniors, the breakthrough came from quantifying trade-offs:
- Two seniors: +30% immediate productivity, -100% talent pipeline
- Two juniors: -30% immediate productivity, +100% talent pipeline  
- One each: -15% immediate productivity, +50% talent pipeline

This made the decision space explicit rather than trading vague values claims.

Application: When committee members argue from different values, force quantification of what's gained/lost under each option.
```

### 2. What Failed
Patterns that produced low evaluation scores or misleading outputs.

**Example**:
```
LESSON: Historical analogies require explicit similarity analysis (2024-Q2-hiring)

Joe cited "we tried this in 2022 and it failed" without specifying:
- What actually failed (juniors left due to no mentorship time)
- Why it failed (tight deadlines prevented allocated mentorship)
- What's different now (proposal includes allocated mentorship time)
- What constraints remain (still have tight deadlines)

Independent evaluation scored reasoning completeness at 1.2/3.0.

Application: When citing historical precedent, require explicit answers to: What failed? Why? What's similar? What's different? What does that imply?
```

### 3. Procedural Improvements
Meta-lessons about the deliberation process itself.

**Example**:
```
LESSON: Split multi-contingency amendments (2024-Q3-product-strategy)

Tammy proposed amendment: "pursue enterprise IF revenue exceeds $X AND values compatibility verified"

Joe's point of order: these are separate questions requiring separate justification.

Splitting them revealed:
- Revenue threshold was actually guesswork
- Values compatibility was unfalsifiable as stated
- Each contingency needed independent debate

Application: When amendments contain multiple contingencies (IF X AND Y), split into separate motions that can be debated independently.
```

### 4. Character Calibration
Lessons about how the committee roster behaves.

**Example**:
```
LESSON: Maya's paranoia needs Vic's evidence standards (multiple deliberations)

Pattern observed across 5 deliberations:
- Maya raises political concerns
- Without Vic's challenge, concerns become unfalsifiable
- "Someone might have hidden agenda" → speculation spiral
- Vic's "what evidence would prove/disprove this?" forces specificity

Application: When Maya raises political concerns, Vic should immediately demand falsifiability criteria before debate proceeds.
```

## Storage Format: The Lesson Library

Maintain lessons in structured format accessible to future deliberations:

```
lessons/
├── by-category/
│   ├── reasoning-completeness.md
│   ├── evidence-standards.md
│   ├── trade-off-explicitness.md
│   ├── procedural-discipline.md
│   └── character-interactions.md
├── by-scenario/
│   ├── 2024-Q2-hiring-decision.md
│   ├── 2024-Q3-product-strategy.md
│   └── 2024-Q4-resource-allocation.md
└── index.md (searchable summary)
```

### Lesson Template

```markdown
# [Lesson Name]

**Source**: [Which deliberation this came from]
**Date**: [When extracted]
**Category**: [Reasoning/Evidence/Procedure/Character/Trade-offs]

## Context
[What problem were you solving? What went wrong or right?]

## Pattern
[What specifically happened? Quote from transcript if relevant.]

## Evaluation Result
[What did independent evaluation say? Scores?]

## Insight
[What did you learn? Why did this pattern emerge?]

## Application Rule
[How should this inform future deliberations? When is it relevant?]

## Limitations
[When does this lesson NOT apply? What are edge cases?]

## Related Lessons
[Links to related patterns]
```

## Injection Protocol: When and How to Load Lessons

### Pre-Deliberation Injection

Before starting a new committee session, search the lesson library for relevant patterns:

**Search by**:
- **Topic similarity**: "hiring decisions" → load lessons from past hiring deliberations
- **Failure mode**: If past similar problems had low reasoning scores → load those lessons
- **Character patterns**: Load calibration lessons about how characters interact
- **Procedural context**: If using Robert's Rules → load procedural lessons

**Inject as preamble**:
```
Before we begin this deliberation, here are lessons from past sessions:

LESSON 1: Historical analogies need explicit similarity analysis
[paste lesson]

LESSON 2: Multi-contingency amendments should be split
[paste lesson]

LESSON 3: Maya's political concerns require Vic's evidence standards
[paste lesson]

Committee members should apply these lessons to avoid repeating past mistakes.
```

### Mid-Deliberation Injection

If the committee falls into a known failure pattern, interrupt and inject the relevant lesson:

**Detection triggers**:
- Joe cites historical precedent without detail → inject historical analogy lesson
- Amendment with multiple contingencies proposed → inject splitting lesson
- Maya raises unfalsifiable political concern → inject evidence standard lesson
- Debate seems to reach consensus too easily → inject adversarial rigor lesson

**Injection format**:
```
MODERATOR INTERVENTION:

The current debate has triggered a pattern we've seen before: [description]

In [past scenario], this led to [problem]. Independent evaluation scored it [X/3.0] because [reason].

The lesson was: [application rule]

Please restart this section of the debate with explicit attention to that lesson.
```

### Post-Evaluation Injection

After independent evaluation identifies gaps, inject lessons about how to fix them:

**Example**:
```
Independent evaluation scored reasoning completeness at 1.5/3.0, citing:
"Trade-offs were mentioned but not quantified."

LESSON FROM 2024-Q2: When values conflict, quantify trade-offs explicitly.
[paste lesson with example of quantification that worked]

Please regenerate the trade-off analysis section using this approach.
```

## Building the Institutional Memory Loop

The full cycle looks like:

```
┌─────────────────────────────────────────────┐
│  New Deliberation                           │
│  ↓                                          │
│  Load relevant lessons from library         │
│  ↓                                          │
│  Committee deliberates (with lesson context)│
│  ↓                                          │
│  Independent evaluation scores              │
│  ↓                                          │
│  Extract new lessons (what worked/failed)   │
│  ↓                                          │
│  Add to lesson library                      │
│  ↓                                          │
│  Update search index                        │
└─────────────────────────────────────────────┘
         ↓
    (repeat for next scenario)
```

**Over time**:
- Library grows richer
- Patterns become clearer
- Evaluation scores trend upward
- Common failure modes get documented and avoided
- The system learns even though individual conversations don't

## Practical Implementation

### 1. Copilot Directories

Because chat interfaces don't persist state well, maintain external storage:

```
/project-workspace/
├── copilot/
│   ├── current-deliberation/
│   │   ├── transcript.md
│   │   ├── minutes.md
│   │   ├── evaluation.md
│   │   └── lessons-to-extract.md
│   ├── lesson-library/
│   │   ├── [organized as shown above]
│   └── templates/
│       ├── lesson-template.md
│       ├── evaluation-rubrics.md
│       └── injection-prompts.md
```

### 2. Lesson Extraction Workflow

After each deliberation:

**Step 1: Review evaluation**
- What scored low? Why?
- What scored high? Why?
- What patterns emerged?

**Step 2: Extract lessons**
Use template to document:
- What the pattern was
- What evaluation said about it
- How to apply it in future

**Step 3: Categorize and store**
- Add to appropriate category files
- Link related lessons
- Update index for searchability

**Step 4: Test injection**
In next deliberation, inject the lesson and see if it actually prevents the problem.

### 3. Search and Retrieval

When starting new deliberation:

**Manual approach**:
- Review lesson index
- Identify relevant categories
- Copy relevant lessons into preamble

**Assisted approach** (if you have RAG or similar):
- Describe the new problem
- Search lesson library for semantic similarity
- System suggests relevant lessons to inject

**Hybrid approach** (practical for now):
- Maintain curated "common lessons" file
- Always inject these
- Add scenario-specific lessons manually based on topic

## Example: Learning Across Hiring Decisions

### Scenario 1: 2024-Q2 Hiring Decision

**Deliberation**: Should we hire two juniors or one senior?

**Problems encountered**:
- Joe's historical analogy lacked detail (reasoning score: 1.2)
- Trade-offs stated vaguely (trade-off score: 1.5)
- Maya's political concerns unfalsifiable (evidence score: 1.3)

**Lessons extracted**:
```
LESSON H1: Historical analogies need explicit similarity
LESSON H2: Quantify trade-offs in hiring decisions
LESSON H3: Political concerns require falsifiability criteria
```

### Scenario 2: 2024-Q4 Hiring Decision

**Pre-deliberation**: Inject lessons H1, H2, H3

**Deliberation**: Should we hire specialist or generalist?

**Result**: 
- Joe explicitly detailed what was analogous to past hires (reasoning score: 2.8)
- Trade-offs quantified: specialist +40% depth -30% flexibility (trade-off score: 2.9)
- Maya's concerns falsifiable: "If CTO objects by EOW, concern is valid" (evidence score: 2.7)

**New lessons extracted**:
```
LESSON H4: Specialist vs. generalist requires explicit definition of "specialist"
(Committee debated this for 20 minutes before realizing they defined "specialist" differently)
```

### Scenario 3: 2025-Q1 Hiring Decision

**Pre-deliberation**: Inject lessons H1, H2, H3, H4

**Result**: Smooth deliberation, high scores, new lesson about team composition dynamics

**Meta-lesson**:
The lesson library is working—common failure modes are now avoided automatically, freeing attention for genuinely novel problems.

## Advanced Patterns

### Pattern 1: Meta-Lessons About Learning

As you build the library, extract lessons about **lesson extraction**:

```
META-LESSON: Premature lesson extraction

Early in the practice, we extracted lessons too quickly—after single instances.

This led to overfitting: lessons that worked once didn't generalize.

Better approach: Extract lesson after seeing pattern 2-3 times across different contexts.

Exception: Critical failures (major decision error) warrant immediate lesson extraction.
```

### Pattern 2: Lesson Retirement

Some lessons stop being relevant:

```
LESSON [DEPRECATED]: Always include Maya in hiring decisions

Context: Early deliberations without Maya missed political dynamics.

Deprecation reason: This lesson was about learning to use the full roster. Now that roster use is standard practice, this is redundant.

Replacement: Character calibration lessons about when each perspective is essential.
```

### Pattern 3: Lesson Hierarchies

Some lessons are special cases of more general principles:

```
GENERAL PRINCIPLE: Claims require evidence proportional to stakes

SPECIFIC APPLICATIONS:
- H3: Political concerns require falsifiability criteria (high stakes)
- E1: Minor process suggestions can rely on plausibility (low stakes)
- S1: Strategic pivots require quantified predictions (high stakes)
```

Organize library to show these relationships.

### Pattern 4: Negative Lessons

Document what DOESN'T work:

```
NEGATIVE LESSON: Don't inject too many lessons

Context: 2024-Q3 product strategy—injected 12 lessons before deliberation.

Result: Committee spent more time meta-discussing lessons than deliberating the actual problem.

Insight: 3-5 lessons max per deliberation. More than that creates cognitive overhead.

Application: Prioritize most critical lessons for the specific problem. Keep others accessible but don't inject unless needed.
```

## Integration with Other Techniques

### Adversarial Committees

Lessons inform character behavior:
- Calibration lessons about how characters interact
- Guidelines for when each character's propensity is most valuable
- Known failure modes for each character

### Robert's Rules

Lessons improve procedural discipline:
- Common points of order and when to raise them
- Patterns of amendments that work/don't work
- How to handle specific procedural edge cases

### Independent Evaluation

Lessons inform evaluation rubrics:
- What "good" looks like for each rubric (examples from high-scoring deliberations)
- What failure patterns look like (examples from low-scoring deliberations)
- Edge cases where standard rubrics need adjustment

## Common Mistakes

### Mistake 1: Not extracting lessons at all

**Symptom**: Repeating the same mistakes across deliberations, never improving.

**Fix**: After every deliberation with independent evaluation, spend 15 minutes extracting at least one lesson. Even if it's "this went well, here's why."

### Mistake 2: Lessons too abstract

**Symptom**: "Be more rigorous" or "Think carefully about trade-offs"

**Fix**: Lessons must be **concrete and actionable**. "When X happens, do Y" not "generally be better at Z."

### Mistake 3: Not testing lesson effectiveness

**Symptom**: You inject lessons but don't check if they actually prevent problems.

**Fix**: After injecting a lesson, explicitly note whether it was applied. If the same problem recurs despite the lesson, the lesson needs revision.

### Mistake 4: Lesson library becomes junk drawer

**Symptom**: 50+ lessons, no organization, hard to find relevant ones.

**Fix**: Regular curation. Archive deprecated lessons. Group related lessons. Maintain searchable index. Quality over quantity.

### Mistake 5: Overfitting to specific scenarios

**Symptom**: Lessons that worked for hiring don't transfer to product strategy, require extracting everything again.

**Fix**: Extract lessons at **appropriate level of abstraction**. Not "in hiring decisions, quantify trade-offs" but "when values conflict, quantify trade-offs."

## Why This Matters: The Compounding Effect

Individual techniques (committees, Robert's Rules, evaluation) improve single deliberations.

**Cross-scenario learning makes the methodology improve over time.**

```
Without cross-scenario learning:
Deliberation 1: score 1.5
Deliberation 10: score 1.6 (slight improvement from practice)

With cross-scenario learning:
Deliberation 1: score 1.5
Deliberation 10: score 2.7 (systematic improvement from lessons)
```

The difference isn't just quality—it's **compounding quality improvement**.

Each deliberation:
- Solves the immediate problem
- Teaches you something about the process
- Improves future deliberations

The methodology gets better **faster than you could improve through practice alone** because lessons are explicit, transferable, and cumulative.

## Theoretical Foundation

This technique operationalizes:

**Second-Order Cybernetics**: Learning to learn. Not just solving problems but improving the problem-solving process itself. The system observes its own observations and adjusts.

**Organizational Learning Theory** (Argyris & Schön): Single-loop learning (solving problems) vs. double-loop learning (improving how you solve problems). Cross-scenario learning is double-loop—you're not just using AI better, you're learning how to learn to use AI better.

**Institutional Memory** (organizational theory): How organizations persist knowledge beyond individual memory. You're building institutional memory for AI collaboration even though the AI has no memory.

## Conclusion

LLMs don't remember. But **you** can remember for them.

Cross-scenario learning isn't about giving AI memory. It's about:
- Extracting lessons explicitly
- Storing them accessibly  
- Injecting them relevantly
- Testing their effectiveness
- Refining them over time

The result is a methodology that **improves faster than your intuition alone could improve it**.

You're not just solving problems with AI. You're building a knowledge base about **how to solve problems with AI** that makes every future problem easier.

That's the difference between:
- Using tools
- Building systems that make tools more useful over time

And it's what transforms AI collaboration from "helpful sometimes" to "increasingly reliable over time."

---

**Related artifacts**:
- [Adversarial Committees](./adversarial-committees.md)
- [Robert's Rules as Forcing Functions](./roberts-rules-forcing-function.md)
- [Independent Evaluation Protocols](./independent-evaluation.md)

**Related essays**:
- [Introduction to Sense-Making Methodology](../essays/03-sensemaking-101.md)
- [The Synthesis: Why Sense-Making is Inherently Cybernetic](../essays/05-the-synthesis.md)
