# From Practice to Theory: How We Got Here

We didn't start with critical theory. We started with broken agents.

This essay explains the genesis of the Cyber-Sense methodology: how practical engineering failures with Large Language Models (LLMs) led to a rediscovery of narrative theory, and why "treating the model like a committee" turned out to be more than a metaphor.

## The Engineering Problem

Like many early adopters, I began by treating LLMs as better search engines or smarter databases. I wanted them to solve problems: generate code, analyze data, make decisions.

And like everyone else, I hit the **plausibility wall**.

The models would produce outputs that looked perfect at first glance. They followed the genre conventions of a correct answer. They used the right terminology. They had the right structure.

But they were frequently, confidently, subtly wrong.

### The "Statistical Ghost" Phenomenon

I realized I wasn't interacting with a reasoning mind. I was interacting with a **statistical ghost** of human discourse.

When I asked a question, the model wasn't "thinking." It was traversing a high-dimensional latent space to find the most probable completion for the pattern I had initiated. It was a **narrative engine**, conjuring a story about what an answer *should* look like based on its training data.

This explained why they were so good at "genre-faithful screeds"—long, eloquent passages that said very little. They were maximizing probability, effectively smoothing out the nuance and edge cases that constitute actual insight.

## The Pivot: Narrative as Feature, Not Bug

If the tool is a narrative engine, treating it like a calculator is a category error. You don't get mad at a car for not flying; you learn to drive.

I started asking: **If this thing is intrinsically a storyteller, what kinds of problems are best solved by telling stories?**

It turns out, almost all the important ones.

### Humans Are Narrative Engines Too

We like to think of ourselves as rational agents, but cognitive science suggests otherwise. We make sense of the world by constructing narratives.

*   **Legal Systems**: We don't just apply code; we tell stories about precedent and intent.
*   **Business Strategy**: We don't just optimize metrics; we tell stories about market position and future growth.
*   **Scientific Discovery**: We frame hypotheses as stories about how the universe might work, then try to break them.

Humans have faced "wicked problems"—problems with no single correct answer, where the definition of the problem itself is contested—for millennia. And our primary tool for handling them has been **adversarial narrative generation**.

## Rediscovering the Committee

How do humans make high-stakes decisions when truth is uncertain? We rarely do it alone.

We form committees. We empanel juries. We seek second opinions.

We create structures where:
1.  **Multiple viewpoints are forced to interact.**
2.  **Procedures (like Robert's Rules of Order) constrain the chaos.**
3.  **Conflict is not a bug, but the method of discovery.**

I decided to try this with the LLM.

### The Experiment

Instead of asking one agent for "the answer," I spun up multiple agents with conflicting personas:
*   **The Optimist**: Looks for opportunity.
*   **The Skeptic**: Looks for risk.
*   **The Bureaucrat**: Looks for process and precedent.

Then I made them talk to each other.

The results were immediate and striking. The "genre convergence" disappeared.
*   When the Optimist proposed a generic, happy-path plan, the Skeptic attacked it.
*   The Optimist was forced to generate a *new*, more robust narrative to defend its position.
*   The Bureaucrat spotted process holes that neither of the others cared about.

By forcing the "statistical ghosts" to argue, I wasn't getting "better math." I was getting **better reasoning**.

## Why It Works: Constrained Latent Space Traversal

From a theoretical perspective, the "Committee" approach avoids the trap of the most probable path.

A single model query tends to collapse towards the mode of the distribution—the most generic, safe answer.

An adversarial committee forces the system to explore the **tails of the distribution**.
*   The Skeptic forces the narrative into the "failure mode" region of latent space.
*   The Optimist forces it into the "success scenario" region.
*   Robert's Rules acts as a **forcing function**, preventing the conversation from looping or dissolving into incoherence.

We aren't creating consciousness. We are creating a **dynamic system of constraints** that forces the narrative engine to generate something richer, more specific, and more rigorous than it would on its own.

## The Theory Emerges

This practical success led me backward into theory.

*   **Cybernetics**: The system (human + AI committee) is a feedback loop. My observation of the debate changes the debate. The system is steering itself through the problem space.
*   **Sense-Making**: We aren't "finding" the answer. We are *constructing* a bridge across a gap in our understanding, exactly as Brenda Dervin described.
*   **Narrative Rationality**: We are judging the output not just by logical validity, but by narrative coherence and fidelity to the constraints we set.

## Conclusion

This repository—**Cyber-Sense**—is not a philosophy project. It is an engineering log.

The techniques documented here (Adversarial Committees, Robert's Rules, Independent Evaluation) are not abstract rituals. They are **workarounds for the inherent limitations of narrative engines**.

They are the "driving lessons" for the vehicle we actually have, rather than the "flying lessons" for the AGI we wish we had.

If we accept that LLMs are storytelling machines, we can stop trying to force them to be calculators and start using them to help us write better, truer stories about the wicked problems we face.

---

**Next**: [Introduction to Sense-Making](./03-sensemaking-101.md) - The theoretical foundation for treating interpretation as cybernetic process
