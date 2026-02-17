# Narrative Computing as Historical Progression

## The Paradigm Claim

Each generation of computing hardware has forced humans to adapt how we think about expressing and solving problems. This isn't a metaphor—it's a pattern with specific historical instances.

When we got fast arithmetic machines in the 1940s, we had to learn numerical analysis, error propagation, and stability theory. We called this era **numeric computing**, and it produced disciplines like computational physics and operations research.

When we got symbol manipulation machines in the 1970s, we had to learn formal logic, type theory, and algorithm complexity. We called this era **symbolic computing**, and it produced disciplines like software engineering and knowledge representation.

Now we have machines that generate coherent narrative on demand. This essay argues that **narrative computing** represents a comparable paradigm shift—not an incremental improvement to symbolic computing, but a categorical change requiring new methodology.

This is a strong claim. To defend it, we'll trace three intellectual threads that converge on the present moment: the cognitive science of narrative thought, the computational narrative intelligence research tradition, and systems-theoretic critiques of mechanism. Each thread contributes something essential. Together, they explain why Cyber-Sense methodology isn't arbitrary—it's grounded in established science while addressing a genuinely new problem.

---

## The Cognitive Thread: Narrative as Mode of Thought

### Bruner's Two Modes

In 1986, cognitive psychologist Jerome Bruner proposed something that seemed almost heretical to the dominant information-processing paradigm: there are two irreducible modes of human thought, and neither can be reduced to the other.

He called them the **paradigmatic mode** (or logico-scientific) and the **narrative mode**. The paradigmatic mode seeks truth through formal analysis, logical proof, and empirical verification. It deals in categories, abstractions, and context-independent propositions. Its imaginative application produces good theory and tight analysis.

The narrative mode operates differently. It deals with human intentions and their vicissitudes—what happens when plans meet reality, when expectations collide with events. Its imaginative application produces good stories, believable accounts, and gripping drama. It concerns itself not with truth conditions but with **lifelikeness**—whether a story rings true to human experience.

Crucially, Bruner argued these modes are complementary but irreducible:

> "Efforts to reduce one mode to the other or to ignore one at the expense of the other inevitably fail to capture the rich diversity of thought."

This wasn't postmodern relativism. Bruner was making a precise cognitive claim: humans have two distinct systems for organizing experience, and both are necessary for navigating the world.

The implications for AI collaboration are profound. If narrative is an irreducible cognitive mode—not a primitive version of logic but a different function entirely—then treating LLMs as "reasoning engines" that happen to output text is a category error. They're **narrative engines**. The text they produce follows narrative logic (coherence, plausibility, dramatic structure) rather than formal logic (validity, soundness, proof).

### Narrative Cognition Research

Bruner's insight sparked decades of research confirming that narrative isn't just how we communicate—it's how we think.

Lee Roy Beach's Theory of Narrative Thought (2010) went further, arguing that narrative is the **primary** mode of human cognition. We maintain what he called a "prime narrative"—an ongoing chronicle of our experience organized by time and causation. This prime narrative is the bedrock of intuitive reasoning, the source of private thought, and the basis for communication.

When we encounter new situations, we don't first analyze them logically and then translate to narrative for communication. We understand them *as* narrative from the start—characters with intentions, events with causes, outcomes that follow (or violate) expectations.

Empirical research supports this. Pennington and Hastie's studies of jury decision-making (1986, 1992) demonstrated that jurors construct narrative representations of evidence, not logical matrices. They organize testimony into stories, and the story that best accounts for the evidence wins. This isn't a bug in human reasoning—it's how complex judgment under uncertainty actually works.

The connection to Cyber-Sense methodology is direct: if humans naturally think through narrative, then framing AI collaboration as narrative generation and evaluation isn't artificial. It's working *with* human cognition rather than against it. Adversarial storytelling works because it leverages how humans actually process complex situations.

---

## The Computational Thread: Making Machines Tell Stories

### Early Story Generation

The dream of computational storytelling predates modern AI. As Mark Riedl notes, we can trace interest in machine-generated narrative to 1843, when Ada Lovelace first asked whether Babbage's Analytical Engine could be creative.

The first actual story generation systems emerged in the 1960s. Grimes' fairy tale generator (1960, recently rediscovered by James Ryan) may be the first system to use artificial intelligence techniques for story creation. By the 1970s, researchers like James Meehan had created systems like TALESPIN (1977), which could generate original Aesop-style fables by simulating characters with goals, plans, and beliefs.

TALESPIN is famous for its failures as much as its successes. When character goals conflicted in unexpected ways, the system produced delightfully absurd stories—like the tale where Joe Bear, hungry for honey, asks Irving Bird where to find some. Irving doesn't know, so Joe asks Irving where to ask, and Irving doesn't know that either. Joe wanders off, and the story ends with Joe still hungry and Irving still ignorant. The system had generated a "story" that was technically coherent but narratively unsatisfying.

These failures revealed something important: **narrative coherence isn't just logical coherence**. A story can be internally consistent and still feel wrong. The early systems could generate plot structures but couldn't evaluate whether those structures made good stories.

### Computational Narrative Intelligence

By the 1990s and 2000s, researchers like Riedl had begun developing more sophisticated approaches under the banner of **computational narrative intelligence**—defined as "the ability to craft, tell, understand, and respond affectively to stories."

This work produced impressive results within constrained domains. Planning-based systems could generate stories that satisfied author-specified constraints. Interactive narrative systems could adapt stories in real-time based on user actions. Training simulations used computational storytelling to create engaging educational experiences.

But there was a persistent limitation: these systems required explicit knowledge engineering. Every character's possible actions, every object's properties, every causal relationship had to be hand-specified. You could build a compelling interactive story in a well-defined microworld (a game, a training simulation), but you couldn't generate narrative about arbitrary real-world situations.

The systems could make machines tell stories. But they couldn't make machines that understood stories the way humans do—flexibly, contextually, with vast background knowledge brought to bear automatically.

### The Pre-LLM Gap

This was the state of computational narrative intelligence before large language models: sophisticated techniques that worked brilliantly within constrained domains but couldn't scale to open-world complexity.

The gap wasn't just technical. It was also conceptual. Computational narrative research focused primarily on **machines generating stories for humans to consume**—entertainment, education, training. The question of **humans using narrative machines as thinking partners** received less attention. There was no pressing need for methodology around human-AI narrative collaboration because the AI couldn't hold up its end of the collaboration.

What changed with LLMs wasn't just capability—it was the **kind** of capability. For the first time, we had systems that could generate coherent narrative about virtually any topic, drawing on vast implicit knowledge, producing outputs that follow genre conventions and maintain internal consistency across extended passages.

This created a new problem: the outputs *sound* authoritative but aren't grounded in truth. The narrative coherence that makes LLM outputs readable is exactly what makes them dangerous. A confident-sounding story can be completely wrong.

We needed methodology for working with powerful narrative engines. Computational narrative intelligence had given us theory and techniques for building such engines. What we lacked was theory and techniques for **collaborating** with them.

---

## The Systems-Theoretic Thread: Why Mechanism Fails

### Rosen's Challenge to Reductionism

While cognitive scientists studied narrative thought and AI researchers built story generators, theoretical biologist Robert Rosen was developing a rigorous argument for why certain systems—living systems especially—cannot be understood through reductionist analysis.

In *Life Itself* (1991), Rosen argued that the Cartesian-Newtonian paradigm, which treats organisms as complicated machines, is fundamentally inadequate. The problem isn't that organisms are very complex machines. It's that they're not machines at all, in the precise sense that matters.

A machine, in Rosen's framework, can be fully characterized by listing its parts and their interactions. Given complete knowledge of components and initial conditions, the machine's behavior follows deterministically. This is what makes machines simulable—you can build a model that captures everything relevant.

Living systems have a different property: **organization** that cannot be reduced to component interactions. The whole is not merely greater than the sum of parts—the whole has causal efficacy that isn't localizable in any subset of parts. Rosen called this **complexity** (in a technical sense distinct from mere complication) and demonstrated it rigorously using category theory.

The key insight for our purposes: **complex systems require semantic description**. You can describe a machine purely syntactically—rules for symbol manipulation, algorithms for state transitions. But you cannot capture a living system, or any truly complex system, without semantics—meaning, function, purpose.

### Organization vs. Mechanism

Rosen's work on anticipatory systems extended this analysis. Living organisms, he argued, contain models of their environment that allow them to anticipate future states and act accordingly. This anticipatory capacity isn't reducible to stimulus-response; it involves internal representations that carry meaning about the external world.

This has direct implications for understanding LLMs. Large language models are, at one level, pure syntax manipulation—statistical patterns over token sequences, no grounding in external reality. They produce outputs that are **syntactically** coherent (well-formed sentences, consistent style, genre-appropriate structure) but have no intrinsic **semantic** grounding (no verification against reality, no understanding of truth conditions, no causal connection to the world).

When we ask an LLM for analysis or advice, we get narrative that follows the conventions of good analysis or advice. The syntax is right. But semantic validity—whether the analysis actually applies to our situation—requires something the model cannot provide: judgment that connects symbols to reality.

This is why methodology matters. The model produces syntactically coherent narrative. Humans must supply semantic grounding through evaluation, verification, and judgment. Cyber-Sense methodology structures this division of labor: AI generates candidate narratives, humans evaluate which narratives merit belief and action.

### Second-Order Cybernetics

The cybernetic tradition adds another crucial insight: the observer is part of the system being observed.

Heinz von Foerster and the second-order cyberneticians emphasized that any observation changes the system observed. There's no view from nowhere. When you examine a system, you become entangled with it.

Applied to LLM interaction: when you prompt a model, you're not querying a static knowledge base. You're initiating a dynamic process where your framing, context, and even your presence in the conversation shape the output. The model that generated a response will find that response convincing—it was, after all, constructed to be convincing.

This explains why **independent evaluation** is essential. The generator instance and evaluator instance must be separate precisely because the hermeneutic circle is real. You cannot evaluate your own outputs without bias. The evaluator must come to the artifact fresh, without investment in its coherence, able to see only what's actually on the page.

---

## The Synthesis: What's Actually Novel

### The Convergence Point

Around 2022, these threads converged in a way that created new demands.

LLMs reached sufficient capability to generate coherent narrative across virtually any domain. Suddenly, the abstract possibility of "narrative engines" became practical reality. Anyone could generate plausible-sounding analysis, advice, arguments, and explanations on any topic.

This created urgent need for methodology that hadn't existed before. Bruner told us narrative is an irreducible cognitive mode, but he wasn't thinking about AI collaboration. Riedl and the computational narrative researchers gave us techniques for building story generators, but not for partnering with them on complex problems. Rosen explained why semantic grounding can't emerge from syntax alone, but he wasn't addressing the practical question of how humans should work with syntactic narrative generators.

The application domain was new. As the characters in the synthesis essay observe: "We've never had narrative engines powerful enough to make this methodology necessary before."

### What Cyber-Sense Contributes

The novelty of Cyber-Sense methodology isn't in its components:

- Adversarial process comes from legal tradition, peer review, red teams
- Explicit reasoning chains come from mathematical proof and philosophical argument
- Evidence standards come from empirical science and journalism
- Procedural constraints come from parliamentary tradition
- Independent evaluation comes from separation of concerns in software and double-blind review in science

What's novel is the **synthesis and application**: adapting these existing practices into a coherent methodology for human-AI narrative collaboration.

The methodology treats AI as what it actually is—a narrative engine—and designs interaction patterns appropriate to that reality. It doesn't pretend LLMs are reasoning systems that happen to output text. It takes seriously that narrative generation and truth-seeking are different processes, and builds in the adversarial structures, evaluation protocols, and human judgment that bridge the gap.

The theoretical synthesis is also novel: combining Dervin's sense-making (gaps produce bridges that change situations), second-order cybernetics (observation changes state), and Deleuzian philosophy of difference (repetition produces novelty) into what we might call **cybernetic hermeneutics**—using cybernetic principles to design interpretive protocols for AI interaction.

### Why "Narrative Computing" as Term

The terminology matters. "AI assistant" sets wrong expectations—it implies the system understands your intent, has access to truth, and acts in your interest. "Chatbot" trivializes what these systems can do. "Generative AI" is too broad—it covers image generation, code synthesis, and much else.

"Narrative computing" names what's distinctive: **the machine generates narrative**, and this shapes everything about how we must use it.

Just as "numeric computing" emphasized that you had to frame problems numerically to use arithmetic machines, and "symbolic computing" emphasized that you had to frame problems formally to use logic machines, "narrative computing" emphasizes that you must frame problems as stories to use storytelling machines.

This isn't limitation—it's recognition. Each paradigm expanded the class of problems computers could help with. Narrative computing extends to the messy, contextual, intention-laden problems that resisted both numeric and symbolic approaches. But it requires appropriate methodology.

---

## Implications and Open Questions

### Methodological Maturation

Numeric computing took roughly 30 years to develop mature methodology—from ENIAC to widespread scientific computing with established practices for numerical analysis, error handling, and algorithm design.

Symbolic computing followed a similar arc—from LISP to enterprise software with established practices for software engineering, testing, and formal verification.

We're in the early days of narrative computing. The methodologies aren't settled. Best practices are still emerging. Cyber-Sense represents one contribution to this developing field, not the final word.

What disciplines will narrative computing require? Adversarial deliberation, certainly. Evidence standards adapted for narrative claims. Assumption surfacing techniques. Institutional memory management. Perhaps entirely new practices we haven't yet imagined.

### Risks of Getting It Wrong

The stakes are significant. LLMs are being deployed at scale right now—for strategic decisions, medical triage, legal research, code generation, educational assessment, content moderation.

Most deployment treats LLMs as better versions of symbolic systems—faster search, smarter assistants, automated reasoning. This is the category error that Cyber-Sense methodology addresses.

If we don't develop appropriate methodology, we get:
- Confident-sounding bullshit at scale
- Decisions based on plausible but wrong stories  
- Automation of bias dressed as objectivity
- Trust in systems that can't bear the weight

### The Optimistic Case

Here's what's possible if we get this right:

Narrative engines can generate and evaluate more candidate solutions than humans could explore alone. They can surface perspectives we wouldn't naturally consider. They can make implicit assumptions explicit and force trade-offs into the open. They can maintain institutional memory that persists across conversations and contexts.

Not because AI is magic. Because we've developed methodologies appropriate to the tool.

The disciplines we use for high-stakes decisions—adversarial process, independent review, evidence standards—become accessible for everyday decisions. Rigorous sense-making at scale, with human judgment remaining central but amplified by narrative generation capacity.

---

## Conclusion

The three-eras framing—numeric, symbolic, narrative—is defensible, not hype. Each paradigm is defined by what the machine does (arithmetic, logic, story generation) and what methodology humans must develop to use it effectively.

Narrative computing is the current paradigm. LLMs are narrative engines. Treating them as oracles or reasoning systems is a category error with practical consequences. Appropriate methodology—like Cyber-Sense—designs interaction around what these systems actually do.

The intellectual foundations are solid. Bruner established narrative as irreducible cognitive mode. Rosen demonstrated that complex systems require semantic description beyond syntactic manipulation. Computational narrative intelligence developed techniques for story generation and analysis. Second-order cybernetics explained why observer and observed are entangled.

What's new is the application domain and the synthesis. We have powerful narrative engines now. We need practical methodology for collaborating with them. The components exist in other fields—adversarial process, evidence standards, procedural constraints, independent evaluation. The contribution is adapting these into coherent practice for human-AI narrative collaboration.

We're in the early days. The methodology will evolve. But the fundamental insight is clear: if the tool is a narrative engine, treating it like a calculator is a category error. You don't get mad at a car for not flying; you learn to drive.

---

## References

Bender, Emily M., Timnit Gebru, Angelina McMillan-Major, and Shmargaret Shmitchell. 2021. "On the Dangers of Stochastic Parrots: Can Language Models Be Too Big?" *FAccT '21: Proceedings of the 2021 ACM Conference on Fairness, Accountability, and Transparency*, 610-623.

Beach, Lee Roy. 2010. *The Psychology of Narrative Thought: How the Stories We Tell Ourselves Shape Our Lives*. Xlibris.

Bruner, Jerome S. 1986. *Actual Minds, Possible Worlds*. Harvard University Press.

Dervin, Brenda. 1998. "Sense-Making Theory and Practice: An Overview of User Interests in Knowledge Seeking and Use." *Journal of Knowledge Management* 2(2): 36-46.

Pennington, Nancy, and Reid Hastie. 1992. "Explaining the Evidence: Tests of the Story Model for Juror Decision Making." *Journal of Personality and Social Psychology* 62(2): 189-206.

Piper, Andrew, Richard Jean So, and David Bamman. 2021. "Narrative Theory for Computational Narrative Understanding." *Proceedings of the 2021 Conference on Empirical Methods in Natural Language Processing*, 298-311.

Riedl, Mark O. 2016. "Computational Narrative Intelligence: A Human-Centered Goal for Artificial Intelligence." arXiv:1602.06484.

Rosen, Robert. 1991. *Life Itself: A Comprehensive Inquiry into the Nature, Origin, and Fabrication of Life*. Columbia University Press.

Shanahan, Murray. 2024. "Talking About Large Language Models." arXiv:2212.03551.

von Foerster, Heinz. 2003. *Understanding Understanding: Essays on Cybernetics and Cognition*. Springer.

---

**Related essays**:
- [Why Narrative Engines Change Everything](./01-why-narrative-engines-change-everything.md) — the concise version of this historical argument
- [Narrative Engineering](./07-bolands-narrative-engineering.md) — Boland's independent convergence on similar conclusions

**Related artifacts**:
- [Integration with MOOLLM](../artifacts/integration-with-moollm.md) — how Cyber-Sense maps onto an infrastructure designed for narrative computing
