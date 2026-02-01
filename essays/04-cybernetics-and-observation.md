# Cybernetics and the Observer Problem

> "Objectivity is the delusion that observations could be made without an observer." — Heinz von Foerster

## The Loop You Can't Step Out Of

Traditional science (and traditional engineering) is built on **First-Order Cybernetics**.

In First-Order Cybernetics, the engineer stands outside the system. You look at the engine. You tweak a valve. The engine runs differently. You measure the output. You are the god-like operator, distinct from the machine.

This is a useful fiction for steam engines. It is a disastrous fiction for Narrative Engines.

**Second-Order Cybernetics** is the cybernetics of observing systems. It recognizes a fundamental truth: **You cannot observe a complex system without being part of it.**

When you interact with an LLM, you are not "measuring" its knowledge. You are coupling with it. Your prompt doesn't just retrieve information; it alters the system's state. It sets the initial conditions for a trajectory that wouldn't exist without your specific observation.

## Prompting is Control Theory

We need to stop thinking of prompts as "queries" (database metaphor) or "instructions" (programmer metaphor).

**A prompt is a control signal.**

In control theory, you inject a signal into a dynamic system to steer its behavior.
*   **The System**: The LLM's vast, high-dimensional latent space.
*   **The Signal**: Your text input.
*   **The Trajectory**: The generated text.

When you refine a prompt, you are not "fixing code." You are adjusting the gain on a feedback loop. You are trying to find the control sequence that steers the system's trajectory through the region of the latent space that aligns with your intent.

But unlike a mechanical system, the "steersman" (cybernetes) is changed by the output.

1.  You ask a question.
2.  The model answers.
3.  The answer changes your understanding of the problem.
4.  You ask a *different* question.

This is a coupled oscillator. You and the AI are two dynamic systems adjusting each other's states in real-time.

## The Physics of Deleuze: Actualization via Observation

This is where the engineering of Cybernetics meets the metaphysics of [Deleuze](./06-deleuze-difference-repetition.md).

Deleuze argues that reality consists of a **Virtual** field (potentials) that gets collapsed into **Actual** existence.
Cybernetics provides the mechanism for this collapse: **Observation.**

### The Virtual Field
The LLM's weights are the Virtual. They contain the potential for every possible sentence the model could generate. But they contain no *actual* sentences. Just tendencies, probabilities, and latent structures.

### The Actualization
When you observe the system (prompt it), you force it to collapse that infinite potential into a specific string of tokens. You have **actualized** the virtual.

But here is the catch: **How you observe determines what actualizes.**

If you observe the system with a "Schoolteacher" persona ("Grade this essay"), you actualize a critical, pedantic trajectory.
If you observe it with a "Collaborator" persona ("Help me improve this"), you actualize a supportive, constructive trajectory.

Measurement creates the reality. The "facts" the model produces are not sitting in a database waiting to be found. They are produced on the fly by the collision between the Virtual field and your Observer constraint.

## Eigenforms: How Stability Emerges from Noise

If everything is a loop of becoming, how does anything ever stay still? How do we get facts, stable meanings, or consistent personalities?

Heinz von Foerster gave the mathematical answer: **Eigenforms.**

An eigenform is a recursive value—a specific state that a function creates, which then creates itself.
$$ x_{t+1} = F(x_t) $$
If this loop stabilizes such that $x = F(x)$, you have found an Eigenform.

In AI interaction, we are hunting for Eigenforms.

*   **Dialogue**: When you and the AI finally "get" each other, and the conversation flows effortlessly? You have entered a stable eigen-behavior.
*   **Adversarial Committees**: We use the committee structure to *prevent* premature eigenforms. We don't want the system to stabilize on the first easy answer. We inject noise (character conflict) to kick the system out of shallow eigen-states, reshaping the function $F(x)$ until the only stable solution is a robust, well-reasoned truth.

**Eigenforms are the engineer's version of Deleuze's "becoming-stabilized."** They prove that you don't need fixed objects to have stability. You just need stable processes.

## The Observer's Responsibility

Understanding this changes how you use the tool.

If you treat the AI as an oracle (First-Order), you will accept its outputs as "true" or "false." You will say "The model hallucinated."

If you treat it as a coupled cybernetic system (Second-Order), you realize: **"My control signal steered the system into a hallucination regime."**

You stop blaming the car for going off the road and start looking at your hands on the wheel.

*   **You supply the context.**
*   **You set the temperature.**
*   **You define the persona.**
*   **You interpret the result.**

You are not the user. You are the Co-System.

## Summary

1.  **AI interaction is a loop**, not a line.
2.  **Prompts are control signals**, steering a trajectory through a latent space.
3.  **Observation is Actualization**: You collapse the Deleuzian Virtual into the Actual through the act of querying.
4.  **Eigenforms are the goal**: We look for stable patterns that survive the recursive loop of questioning, answering, and questioning again.

We build these loops intentionally. That provides the "How."
Deleuze provides the "What."
And Dervin provides the "Why."

Together, they form the Cyber-Sense machine.
