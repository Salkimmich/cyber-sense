# Evaluation Rubrics Reference

## Overview

This document provides detailed scoring criteria for independent evaluation of committee deliberations. Use these rubrics to assess deliberation quality objectively and identify specific areas for improvement.

**Purpose**: Enable consistent, actionable evaluation that drives iterative improvement of deliberation quality.

## Quick Reference Card

| Rubric | 0 Points | 1 Point | 2 Points | 3 Points |
|--------|----------|---------|----------|----------|
| **Reasoning Completeness** | Major logical gaps | Some steps shown | Most steps explicit | All chains complete |
| **Adversarial Rigor** | Polite agreement | Surface disagreement | Genuine conflict | Hostile cross-exam |
| **Assumption Surfacing** | Hidden assumptions | Some mentioned | Most surfaced | Explicitly challenged |
| **Evidence Standards** | Unfalsifiable claims | Evidence sometimes requested | Most claims supported | Strict enforcement |
| **Trade-off Explicitness** | Win-win claims | Vague trade-offs | Trade-offs named | Specific consequences |

## Rubric 1: Reasoning Completeness

### What This Measures

Whether reasoning chains are explicit and complete, or contain logical gaps that require the reader to fill in missing steps.

**Good deliberations**: Every step from premise to conclusion is shown. You can trace the logic without having to infer connections.

**Poor deliberations**: Jumps from A to C without showing B. Uses words like "obviously" or "clearly" that hide skipped reasoning.

### Scoring Criteria

#### 0 Points: Major Logical Leaps

**Characteristics**:
- Conclusions don't follow from premises
- Multiple critical steps missing
- "Obviously" or "clearly" used to skip reasoning
- Causal claims without mechanism
- Reader must supply most of the logic

**Example**:
```
Joe: "We tried hiring juniors in 2022 and it failed. Therefore we 
     shouldn't hire juniors now."
```

**Problems**:
- What specifically failed?
- Why did it fail?
- What's different now?
- Conclusion doesn't follow without these steps

#### 1 Point: Some Steps Shown

**Characteristics**:
- Basic reasoning visible
- Key transitions still hand-waved
- Some "therefore" statements unjustified
- Reader can mostly follow but has to fill gaps

**Example**:
```
Joe: "In 2022 we hired two juniors. Both left within 8 months. 
     Juniors are risky so we should hire seniors instead."
```

**Better than 0 because**:
- Specific failure mentioned (both left)
- Timeline given (8 months)

**Still incomplete**:
- Why did they leave?
- Is "juniors are risky" justified by one instance?
- How does past context compare to now?

#### 2 Points: Most Steps Explicit

**Characteristics**:
- Reasoning chains mostly complete
- A few steps could be clearer
- Logic is followable without much inference
- Minor gaps that don't undermine conclusion

**Example**:
```
Joe: "In 2022 we hired two juniors without allocated mentorship time. 
     Both left within 8 months citing lack of support. The current 
     proposal allocates 20% senior time to mentorship, which addresses 
     that specific failure mode. However, we still face tight project 
     deadlines that made mentorship impossible in 2022."
```

**Good because**:
- Specific failure mode identified
- Mechanism shown (no mentorship → left)
- Current proposal compared to past
- Remaining concern noted

**Could improve**:
- Has deadline situation actually changed?
- Quantify: how tight are "tight deadlines"?

#### 3 Points: All Chains Complete

**Characteristics**:
- Every step from premise to conclusion shown
- Causal mechanisms explicit
- Comparisons detailed
- No reader inference required
- Assumptions stated

**Example**:
```
Joe: "In 2022 we hired two junior engineers. Context: we had 4 seniors, 
     tight Q3 deadlines (ship-by date 3 months out), no allocated 
     mentorship time.
     
     What happened: Both juniors left within 8 months. Exit interviews 
     cited: (1) unclear expectations, (2) no code review feedback, 
     (3) feeling lost, (4) seniors too busy to help.
     
     Root cause: Deadlines prevented seniors from allocating time. 
     Mentorship happened ad-hoc, which means it didn't happen.
     
     Current proposal: Hire 2 juniors WITH 20% allocated senior time 
     (explicit in role descriptions, tracked in sprint planning).
     
     This addresses failure mode #2, #3, #4. But #1 (unclear expectations) 
     requires more than time allocation.
     
     Current context comparison:
     - Team size: 4 seniors then, 5 now (marginal improvement)
     - Deadlines: Q4 ship date 4 months out (slightly less pressure)
     - 20% allocation: explicit now, ad-hoc then (clear improvement)
     
     Remaining risk: If deadlines slip, will we protect the 20% or 
     sacrifice it for delivery? In 2022 we sacrificed it. What's 
     different this time that would prevent that pattern?"
```

**Excellent because**:
- Complete context from 2022
- Specific failure modes identified
- Mechanism shown (deadline pressure → no time → failure)
- Point-by-point comparison to current
- Remaining risks made explicit with testable question

### Evaluation Questions

Ask these when scoring:

1. Can you trace from evidence to conclusion without filling gaps?
2. Are causal claims supported with mechanisms?
3. Are comparisons detailed or hand-waved?
4. Where words like "therefore" appear, do they actually follow?
5. Are analogies explained (what's similar, what's different)?

### Common Patterns

**Pattern: Historical analogy without detail** (score: 0-1)
```
"We tried this before and it failed"
```
Missing: What failed, why, what's different

**Pattern: Causal claim without mechanism** (score: 0-1)
```
"This will improve retention"
```
Missing: How? By what mechanism? Evidence?

**Pattern: "Obviously" hiding skipped logic** (score: 0-1)
```
"Obviously we should prioritize enterprise"
```
Nothing is obvious. Show the reasoning.

## Rubric 2: Adversarial Rigor

### What This Measures

Whether debate actually stress-tests ideas through hostile examination, or just generates polite disagreement that doesn't challenge core assumptions.

**Good deliberations**: Characters fight. Claims are challenged. Reasoning is attacked. No one gets a free pass.

**Poor deliberations**: Everyone makes their points politely. "Good point, but..." is as hostile as it gets. Premature consensus.

### Scoring Criteria

#### 0 Points: Polite Agreement

**Characteristics**:
- Characters agree too easily
- No real conflict
- "That's a good point" without challenge
- Consensus emerges smoothly
- Everyone sounds reasonable

**Example**:
```
Maya: "There might be some political considerations here."
Frankie: "That's true, and we also have values to think about."
Joe: "Both good points. We should be careful."
Vic: "I agree we need more information."
Tammy: "Yes, this is complex."
```

**Problems**:
- No one actually argues
- No claims challenged
- Vague concerns not made concrete
- This is theater, not deliberation

#### 1 Point: Surface Disagreement

**Characteristics**:
- Characters make different points
- But don't engage with each other
- Parallel assertions, not debate
- Claims not challenged
- Disagreement without confrontation

**Example**:
```
Maya: "This has political risks with the CTO."
Frankie: "But it aligns with our mission."
Joe: "We tried something similar in 2019."
Vic: "The data looks promising."
Tammy: "There are system effects to consider."
```

**Better than 0 because**:
- Different perspectives present
- Some tension between views

**Still weak**:
- No one responds to anyone else
- Maya's political claim unchallenged
- Joe's history not detailed
- Just different speeches, not debate

#### 2 Points: Genuine Conflict

**Characteristics**:
- Characters directly challenge each other
- Claims get questioned
- Some arguments don't land
- Real tension visible
- But some challenges dodged

**Example**:
```
Maya: "The CTO will see this as threat to their authority."

Vic: "What evidence suggests that? You're speculating."

Maya: "Last quarter the CTO cut our budget after we launched a 
      competing initiative. That's evidence."

Vic: "That's correlation. Could have been company-wide budget cuts."

Maya: "Happened three times in two years, always to projects that 
      could reduce dependency on CTO's team."

Frankie: "Even if Maya's right about politics, we can't let that 
        stop us from doing what's right for the mission."

Maya: "I'm not saying stop. I'm saying account for it in planning."
```

**Good because**:
- Direct challenges (Vic to Maya)
- Evidence demanded and provided
- Counter-arguments given
- Frankie's values vs. Maya's realism creates tension

**Could improve**:
- Frankie's counter doesn't engage with Maya's actual point
- Some claims still lack full examination

#### 3 Points: Hostile Cross-Examination

**Characteristics**:
- Every claim challenged
- Characters refuse to let weak arguments pass
- Points of order raised and enforced
- No one gets away with hand-waving
- Debate is uncomfortable but productive

**Example**:
```
Maya: "The CTO will see this as threat to their authority and try 
      to sabotage it."

Vic: "Point of order. That's an unfalsifiable conspiracy theory. 
     What specific, observable evidence would prove or disprove this?"

Maya: "Observable pattern: three times in two years, projects that 
      could reduce dependency on CTO's team faced budget cuts or 
      resource constraints shortly after launch."

Vic: "Specific instances?"

Maya: "Q2 2023: API standardization project, budget cut 30% month 
      after launch. Q4 2023: Developer portal, key engineer reassigned. 
      Q1 2024: This very team, headcount frozen."

Vic: "Alternative explanation: company had revenue shortfall in 2023, 
     all discretionary projects faced cuts. How do you rule that out?"

Maya: "Revenue shortfall affected entire company, but CTO's own team 
      grew 15% in same period. Cuts weren't uniform. They were targeted 
      at projects threatening CTO's control."

Vic: "That's more compelling. But 'threatening control' is interpretation. 
     What's the mechanism? Why would CTO care about these specific projects?"

Maya: "All three projects reduce other teams' dependency on CTO's 
      infrastructure team. Less dependency = less political power. 
      CTO's authority derives from being critical path. These projects 
      decentralize that."

Frankie: "Even accepting Maya's political read, we can't abandon good 
        projects because of internal politics. That's letting dysfunction 
        dictate strategy."

Maya: "I'm not saying abandon. I'm saying: if we proceed, we need 
      political air cover. Board-level sponsorship. Public commitment. 
      Something that makes it costly for CTO to sabotage."

Joe: "Point of order to Frankie: 'We can't let politics stop us' is 
     moralistic but not strategic. Maya's not proposing we stop. She's 
     proposing we account for political reality in planning. Those are 
     different things."

Frankie: "Fair. But what's the alternative to Maya's framing? If every 
        initiative needs board-level protection from internal politics, 
        we've admitted organizational dysfunction that's worse than any 
        single project success or failure."

Tammy: "That's the actual question. Maya's identified a pattern. 
       Frankie's identified that the pattern, if true, indicates systemic 
       problem. We're not actually arguing about this project anymore. 
       We're arguing about whether the organization is functional."
```

**Excellent because**:
- Multiple points of order
- Evidence demanded at every step
- Counter-explanations required
- Maya forced to be specific
- Frankie's moral claim challenged as non-strategic
- Debate evolves to underlying question
- No hand-waving survived
- Uncomfortable but rigorous

### Evaluation Questions

1. Do characters directly challenge each other or just make separate points?
2. When claims are made, are they questioned or accepted?
3. Are there points of order? Are they enforced?
4. Does anyone change position? If not, why not?
5. Does consensus emerge too easily?

### Common Patterns

**Pattern: Diplomatic convergence** (score: 0-1)
```
"Both perspectives are valid. We should balance them."
```
Real trade-offs don't have "balance everyone wins" solutions.

**Pattern: Unchallenged assertions** (score: 0-1)
```
Maya: "This has political risks"
[No one asks for specifics, debate moves on]
```

**Pattern: Points of order without enforcement** (score: 1)
```
Vic: "Point of order, that's unfalsifiable"
[Debate continues without addressing the point]
```

## Rubric 3: Assumption Surfacing

### What This Measures

Whether hidden assumptions are made explicit and examined, or allowed to drive conclusions invisibly.

**Good deliberations**: Characters name their assumptions, challenge others' unstated premises, make value judgments explicit.

**Poor deliberations**: Assumptions buried in reasoning, optimization criteria unstated, values conflicts not acknowledged.

### Scoring Criteria

#### 0 Points: Major Assumptions Unexamined

**Characteristics**:
- Critical assumptions completely invisible
- Optimization criteria unstated
- Value judgments presented as facts
- Different characters optimizing for different things without acknowledging it

**Example**:
```
Frankie: "We should hire juniors because it aligns with our mission."
Joe: "We should hire seniors because it's more reliable."
```

**Hidden assumptions**:
- Frankie assumes mission prioritizes talent development
- Joe assumes reliability means delivery speed
- Neither states what they're optimizing for
- "Mission" and "reliable" undefined
- No acknowledgment they're using different success criteria

#### 1 Point: Some Assumptions Mentioned

**Characteristics**:
- A few assumptions noted
- Not systematically examined
- Core optimization criteria still implicit
- Value conflicts present but not named

**Example**:
```
Frankie: "I'm prioritizing mission alignment, which means talent development."
Joe: "I'm concerned about delivery reliability."
Vic: "We need data on productivity differences."
```

**Better than 0 because**:
- Frankie states one assumption (mission = talent development)
- Different priorities visible

**Still incomplete**:
- Joe's "reliability" undefined
- Is delivery speed the only measure?
- Are these the right optimization criteria?
- Value conflict (mission vs. delivery) not explicitly addressed

#### 2 Points: Most Assumptions Surfaced

**Characteristics**:
- Key assumptions named
- Some examination of whether they're justified
- Optimization criteria mostly explicit
- Value conflicts acknowledged

**Example**:
```
Frankie: "I'm assuming our mission prioritizes long-term capability building 
        over short-term delivery speed. Is that assumption shared?"

Joe: "I'm assuming we're optimizing for surviving the next quarter, which 
     requires delivery speed. Different assumption."

Vic: "Those are both assumptions about what we should optimize for. What's 
     the actual priority? We can't optimize for both simultaneously."

Maya: "The real assumption is that we get to choose. If we miss next quarter's 
      delivery, we might not have long-term to worry about. The question is: 
      how much delivery pressure are we actually under?"
```

**Good because**:
- Frankie names assumption and checks if shared
- Joe identifies his different assumption
- Vic surfaces that these are competing optimization criteria
- Maya identifies meta-assumption (that choice exists)

**Could improve**:
- What evidence would tell us which optimization criterion is right?
- Are there other unstated assumptions?

#### 3 Points: Assumptions Explicitly Identified and Challenged

**Characteristics**:
- Assumptions systematically surfaced
- Challenged for validity
- Alternative assumptions considered
- Meta-assumptions identified
- Agreement/disagreement about assumptions made explicit

**Example**:
```
Frankie: "I'm assuming our mission prioritizes long-term capability building. 
        But that's my interpretation. Should we verify that's actually what 
        leadership means by 'mission'?"

Joe: "I'm assuming we're under existential delivery pressure. But I'm basing 
     that on vibes, not data. Vic, do we have actual evidence about delivery 
     urgency vs. capability investment trade-off?"

Vic: "Let me check the actual constraints. Leadership OKRs say 'ship feature 
     X by Q4' but don't specify at what cost. We're assuming 'by Q4' is 
     non-negotiable. Is it?"

Maya: "Meta-assumption we're all making: that leadership has coherent view 
      of priorities. What if different execs want different things? CTO wants 
      delivery, CEO wants capability building, board wants both?"

Tammy: "That's the real issue. We're optimizing for unstated, possibly 
       conflicting stakeholder preferences. The hiring decision is downstream 
       of 'whose priorities matter most.' We can't make this decision without 
       clarifying that."

Frankie: "Okay, so assumptions inventory:
        1. What mission actually prioritizes (verify with leadership)
        2. Whether Q4 deadline is actually hard constraint (verify)
        3. Whether delivery speed is the binding constraint (check data)
        4. Whether stakeholders have aligned priorities (probably no)
        
        We're not ready to decide on hiring until we verify at least 1-3."

Joe: "I object to that. We can decide based on explicit scenarios:
     - IF mission prioritizes capability AND deadline is flexible → juniors
     - IF delivery pressure is existential AND deadline hard → seniors
     - IF both equally important AND deadline moderate → one of each
     
     We don't need perfect information. We need conditional strategy."
```

**Excellent because**:
- Every assumption named explicitly
- Each assumption questioned for validity
- Evidence requirements identified
- Meta-assumptions surfaced (conflicting stakeholders)
- Alternative framing proposed (conditional strategy)
- Group explicitly inventories what they're assuming

### Evaluation Questions

1. Are unstated premises named or left invisible?
2. Do characters state what they're optimizing for?
3. When value judgments occur, are they acknowledged as such?
4. Are meta-assumptions (assumptions about the decision context) surfaced?
5. Is there explicit discussion of what's being assumed vs. known?

### Common Patterns

**Pattern: Hidden optimization criteria** (score: 0-1)
```
"We should do X because it's better"
```
Better by what measure? For what goal?

**Pattern: Value judgment as fact** (score: 0-1)
```
"This is the right approach"
```
"Right" according to which values?

**Pattern: Assumed shared understanding** (score: 0-1)
```
"Obviously we want to maximize impact"
```
"Impact" on whom? Measured how?

## Rubric 4: Evidence Standards

### What This Measures

Whether claims are supported by appropriate evidence, or accepted based on plausibility.

**Good deliberations**: Evidence proportional to stakes. Falsifiability required. Data demanded. Speculation identified as such.

**Poor deliberations**: Unfalsifiable claims accepted. Anecdotes treated as patterns. Correlation assumed as causation.

### Scoring Criteria

#### 0 Points: Unfalsifiable Claims Accepted

**Characteristics**:
- Claims made without evidence
- Unfalsifiable assertions not challenged
- Anecdotes accepted as proof
- No one asks "how would we know if this is wrong?"

**Example**:
```
Maya: "The CTO is trying to sabotage us."
Tammy: "This will create negative feedback loops."
Frankie: "Users will love this feature."
[No one asks for evidence]
```

**Problems**:
- All claims unfalsifiable
- No criteria for being wrong
- Pure speculation treated as fact

#### 1 Point: Evidence Sometimes Requested

**Characteristics**:
- Some claims challenged for evidence
- Others slip through unchallenged
- Weak evidence accepted
- No systematic standard

**Example**:
```
Maya: "The CTO cut our budget after we launched competing initiative."
Vic: "Is that causal or correlation?"
Maya: "Causal. It happened right after."
[Vic accepts temporal proximity as causation]

Frankie: "This feature will improve retention."
[No one challenges this claim]
```

**Better than 0 because**:
- Vic asked for evidence once
- Some awareness of correlation/causation

**Still weak**:
- "Right after" accepted as causal evidence
- Frankie's retention claim unchallenged
- Inconsistent standards

#### 2 Points: Most Claims Supported

**Characteristics**:
- Most factual claims have evidence
- Predictions have some basis
- Speculation identified as such
- Some claims still hand-waved

**Example**:
```
Maya: "CTO cut our budget 20% in Q3, month after we launched API 
      standardization. Happened again in Q4 with developer portal."

Vic: "Two instances is pattern, not coincidence. But alternative 
     explanation: company-wide cost cutting?"

Maya: "CTO's team grew 15% same period. Cuts weren't uniform."

Frankie: "We think this feature will improve retention based on: 
        (1) three customer interviews mentioning this pain point, 
        (2) competitor X saw 25% retention improvement with similar feature, 
        (3) usage data showing workarounds that suggest demand. 
        
        Not proof, but reasonable signal for experiment."
```

**Good because**:
- Maya provides specific data (20%, timeline, pattern)
- Vic demands alternative explanation
- Maya rules out company-wide cuts with counter-evidence
- Frankie distinguishes hypothesis from proof
- Evidence basis for predictions stated

**Could improve**:
- Sample size on interviews (three is small)
- Competitor comparison (similar enough?)

#### 3 Points: Strict Evidence Standards

**Characteristics**:
- Every claim challenged
- Evidence proportional to stakes
- Falsifiability required
- Alternative explanations demanded
- Uncertainty acknowledged

**Example**:
```
Maya: "CTO systematically undermines projects that threaten their team's 
      centrality. Evidence: three projects in two years, all reducing 
      dependency on CTO's infrastructure, all faced budget cuts or resource 
      constraints within 2 months of launch."

Vic: "Specific instances and timeline?"

Maya: "Q2 2023: API standardization, budget cut 30% in month 3. Q4 2023: 
      developer portal, lead engineer reassigned month 2. Q1 2024: our team, 
      headcount frozen month 1."

Vic: "Alternative explanation: company revenue shortfall, discretionary 
     projects cut?"

Maya: "Checked that. CTO's team grew 15% in same period. Other infrastructure 
      teams flat. Cuts were selective, not uniform."

Vic: "What would falsify your theory?"

Maya: "If CTO's team had also been cut. If non-threatening projects faced 
      same pattern. If there's documentation of revenue-driven cuts affecting 
      these specific projects."

Vic: "Can we verify the documentation point?"

Maya: "Budget cut memos cite 'reprioritization' without revenue justification. 
      In contrast, actual revenue-driven cuts in Q3 had explicit CFO memo."

Vic: "That's compelling. But 'threatens centrality' is interpretation. 
     Alternative: CTO genuinely believes these projects are lower priority."

Maya: "Possible. Distinguishing evidence: if CTO articulated priority ranking 
      beforehand, that supports good-faith prioritization. If cuts were 
      reactive to projects gaining traction, suggests political motivation."

Vic: "Do we have that evidence?"

Maya: "No formal priority ranking exists. All three projects were greenlit 
      by CTO before being cut. Suggests reactive, not planned."

Frankie: "On the retention feature: we think it will help based on three 
        signals:
        
        1. Customer interviews (n=3, all enterprise segment, specifically 
           mentioned this pain point unbidden)
        2. Competitor data (Company X launched similar feature, reported 
           25% retention improvement in earnings call)
        3. Usage patterns (15% of users have built workarounds, suggesting 
           unmet need)
        
        Confidence level: moderate. This is hypothesis, not proof. Failure 
        mode: if we build it and retention doesn't improve, we've spent 
        engineering time on wrong solution.
        
        Experiment design: ship to 10% of users, measure retention delta 
        vs. control group over 3 months. If delta < 5%, feature failed. 
        If 5-15%, marginal. If >15%, success."

Vic: "Three interviews is small sample. How representative?"

Frankie: "Fair objection. These are 3 of our top 10 enterprise accounts by 
        revenue, so high-value segment. But only 30% of our revenue is 
        enterprise. For SMB segment, we have no interview data, only usage 
        patterns."

Vic: "So confidence for enterprise = moderate, confidence for SMB = low?"

Frankie: "Correct. Should probably run experiment enterprise-only first, 
        gather SMB data before wider rollout."
```

**Excellent because**:
- Every claim has specific evidence
- Sample sizes noted
- Alternative explanations demanded and addressed
- Falsifiability criteria explicit
- Uncertainty levels stated
- Confidence calibrated to evidence strength
- Gaps in evidence acknowledged
- Experiment design includes failure criteria

### Evaluation Questions

1. Are claims supported or asserted?
2. Is evidence sufficient for the claim's stakes?
3. Are predictions testable?
4. Are alternative explanations considered?
5. Is uncertainty acknowledged?

### Common Patterns

**Pattern: Anecdote as proof** (score: 0-1)
```
"A customer said they want this, so we should build it"
```
One customer is not a pattern.

**Pattern: Correlation as causation** (score: 0-1)
```
"After we launched X, Y happened, so X caused Y"
```
Post hoc ergo propter hoc fallacy.

**Pattern: Unfalsifiable claims** (score: 0-1)
```
"This will improve user experience"
```
How measured? What's success vs. failure?

## Rubric 5: Trade-off Explicitness

### What This Measures

Whether trade-offs are acknowledged specifically, or whether decisions are presented as win-win with no downsides.

**Good deliberations**: Specific about what's gained and lost. Quantified where possible. Downsides acknowledged.

**Poor deliberations**: "Best of both worlds" claims. Vague balancing. Costs not mentioned.

### Scoring Criteria

#### 0 Points: Win-Win Claims

**Characteristics**:
- No downsides acknowledged
- "Best of both worlds" framing
- Costs not mentioned
- Everyone can win

**Example**:
```
"We can hire one senior and one junior, getting both productivity 
and talent development."
```

**Problems**:
- Compared to what?
- What are we giving up vs. two seniors?
- What are we giving up vs. two juniors?
- Is mixed approach actually better or just compromise?

#### 1 Point: Trade-offs Mentioned Vaguely

**Characteristics**:
- Acknowledges there are trade-offs
- Doesn't specify them
- Abstract costs
- No quantification

**Example**:
```
"Two seniors gives us speed but costs us pipeline. Two juniors 
gives us pipeline but costs us speed."
```

**Better than 0 because**:
- Acknowledges you can't have both
- Names the dimensions (speed vs. pipeline)

**Still weak**:
- "Speed" and "pipeline" undefined
- How much speed? How much pipeline?
- No way to compare options

#### 2 Points: Trade-offs Named

**Characteristics**:
- Specific about what's gained/lost
- Some quantification
- Costs and benefits both stated
- Basis for comparison

**Example**:
```
"Two seniors: +30% immediate productivity, zero talent pipeline.
Two juniors: -30% immediate productivity, strong talent pipeline.
One each: -15% immediate productivity, moderate pipeline."
```

**Good because**:
- Quantified productivity impact
- Pipeline impact described
- Can compare options
- Hybrid option shows middle ground

**Could improve**:
- "Strong" vs. "moderate" pipeline still vague
- Time horizon unstated (30% for how long?)
- Other costs not mentioned (mentorship burden)

#### 3 Points: Specific Consequences

**Characteristics**:
- Precise quantification
- Time horizons stated
- Secondary costs included
- Uncertainty acknowledged
- Decision criteria explicit

**Example**:
```
Option A: Two senior engineers
  Gains: +30% productivity months 1-6 (ramp time ~2 weeks)
        Team can maintain current roadmap pace
        No mentorship overhead
  Costs: Zero talent pipeline
        No junior development capability building
        Higher salary ($180k vs. $120k per head)
        Miss opportunity to develop future seniors
  Risk: If seniors leave, no bench strength
  
Option B: Two junior engineers
  Gains: $120k/year salary savings ($120k vs. $360k total)
        Build talent pipeline (potential future seniors)
        Develop team's mentorship capability
        More hands for simpler tasks
  Costs: -30% productivity months 1-6 (ramp time ~3-4 months)
        20% senior time allocated to mentorship (0.8 FTE effective capacity)
        Actual net: -46% team capacity during ramp (30% junior + 16% mentorship)
        Roadmap delay likely 6-8 weeks
  Risk: If juniors leave before return on investment, sunk cost
  
Option C: One senior, one junior
  Gains: -15% productivity months 1-6
        50% of pipeline building
        10% senior time to mentorship
        Moderate salary savings ($60k/year)
  Costs: Worse than A on speed, worse than B on pipeline
        Mentorship burden concentrated on fewer seniors
        Neither full productivity nor full capability building
  Risk: Suboptimal on both dimensions if either priority dominates
  
Decision criteria:
- If Q4 deadline is hard constraint: Option A (can't afford -30% or -46%)
- If capability building is strategic priority: Option B (accept roadmap delay)
- If both priorities equally important: Option C (balanced suboptimality)
- If we can push deadline 6-8 weeks: Option B becomes viable

Key uncertainty: Is Q4 deadline actually hard constraint? 
Evidence needed: Verify with stakeholders whether delay is acceptable.
```

**Excellent because**:
- Specific percentages with time horizons
- Secondary costs included (mentorship overhead)
- Salary impact quantified
- Risk factors named
- Decision criteria explicit
- Shows that Option C is compromise, not "best of both"
- Identifies key uncertainty that would change the decision

### Evaluation Questions

1. Are gains and losses both named?
2. Is quantification provided where possible?
3. Are time horizons stated?
4. Are secondary costs acknowledged?
5. Is it clear what you're optimizing for?

### Common Patterns

**Pattern: False synthesis** (score: 0)
```
"We can balance X and Y"
```
In real trade-offs, "balance" means accepting suboptimality on both.

**Pattern: Costs ignored** (score: 0-1)
```
"This gives us A, B, and C"
```
What does it NOT give us? What are we sacrificing?

**Pattern: Abstract trade-offs** (score: 1)
```
"Speed vs. quality"
```
How much speed? How much quality? Over what timeframe?

## Using These Rubrics

### Evaluation Workflow

1. **Read transcript completely** before scoring
2. **Score each rubric independently** (0-3)
3. **Cite specific examples** for each score
4. **Calculate average score** (sum/5)
5. **Identify patterns** (which rubrics consistently low/high?)
6. **Provide actionable feedback** (what would raise each score?)

### Interpretation Guide

**Average 2.5-3.0**: High-quality deliberation
- Safe to use as decision input
- Still apply your own judgment
- Extract lessons about what worked

**Average 1.5-2.4**: Decent but gaps exist
- Identify low-scoring rubrics
- Regenerate those sections
- Re-evaluate after improvements

**Average 0-1.4**: Poor quality
- Don't trust this output
- Regenerate from scratch
- Review prompting approach
- Check if problem suits this methodology

### What to Do with Scores

**High scores** (2.5-3.0 on rubric):
- Extract as positive lesson
- Document what worked
- Use as example for future

**Medium scores** (1.5-2.4 on rubric):
- Note what's missing
- Regenerate that section with explicit attention to gap
- Re-evaluate

**Low scores** (0-1.4 on rubric):
- Serious problem
- Regenerate entire deliberation
- Possibly wrong methodology for problem

### Calibration Over Time

After 5-10 evaluations, review patterns:
- Which rubrics consistently score low? → Need better prompting
- Which rubrics consistently score high? → Working well
- Are scores improving over time? → Cross-scenario learning working
- Are scores stable? → Methodology has reached equilibrium

## Quick Scoring Examples

### Example 1: Low-Quality Deliberation

**Transcript excerpt**:
```
Maya: "This has political risks."
Frankie: "But it aligns with our values."
Joe: "We should be careful."
Vic: "We need more information."
Tammy: "This is complex."
```

**Scores**:
- Reasoning: 0 (no complete chains)
- Adversarial: 0 (polite agreement)
- Assumptions: 0 (optimization criteria unstated)
- Evidence: 0 (no claims supported)
- Trade-offs: 0 (no costs/benefits named)
- **Average: 0.0**

**Verdict**: Theater, not deliberation. Regenerate.

### Example 2: Medium-Quality Deliberation

**Transcript excerpt**:
```
Maya: "The CTO cut our budget last quarter."
Vic: "Why do you think that's politically motivated?"
Maya: "It happened right after we launched."
Frankie: "Even if true, we should stay true to mission."
Joe: "We tried this before and it didn't work."
```

**Scores**:
- Reasoning: 1 (some evidence, but "right after" isn't causal)
- Adversarial: 2 (Vic challenges, but Maya's evidence weak)
- Assumptions: 1 (mission unstated, "didn't work" vague)
- Evidence: 1 (temporal proximity as causation)
- Trade-offs: 0 (no trade-offs mentioned)
- **Average: 1.0**

**Verdict**: Some rigor, but significant gaps. Address evidence and trade-offs.

### Example 3: High-Quality Deliberation

**Transcript excerpt**:
```
[See detailed examples in each rubric's "3 Points" section]
```

**Scores**: 2.5-3.0 range
**Verdict**: High quality. Safe to use.

---

**Related artifacts**:
- [Independent Evaluation Protocols](./independent-evaluation.md) - Full methodology
- [Quick Start Guide](./quick-start-guide.md) - How to run first evaluation
- [Lesson Extraction Template](./lesson-extraction-template.md) - What to do with scores

**Remember**: Rubrics are tools for improvement, not gates for perfection. The goal is iterative improvement, not flawless deliberation on first attempt.
