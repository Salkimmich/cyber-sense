---
Model: Gemini 3 Pro
Host: Perplexity Web
---
A useful way to think about an LLM-driven text pipeline is as an algebra of *decorated texts* where each step is a composable transformation that may also attach new metadata (“enrichment”). In that view, “types” and “scores” become first-class decorations that flow through the pipeline rather than something enforced outside it.

## Core algebra
Let `Text` be the carrier set of raw strings, and let `Meta` be a finite map (key → value) holding scores, labels, provenance, etc.  A pipeline state is a decorated object \((t, m)\in \text{Text}\times\text{Meta}\), and a pipeline step is a morphism \(f : \text{Text}\times\text{Meta}\to \text{Text}\times\text{Meta}\) (often effectful because an LLM is stochastic and may fail).  

Composition is ordinary function composition, but it’s helpful to treat `Meta` merge as an explicit operator \(m \sqcup \Delta m\) (a “join”/merge that is at least associative and has an identity empty-map), because then many pipeline laws become “about metadata merge” rather than “about prompts”.

## Scores as decorations
A rubric application is naturally a morphism from text to a score object, e.g. \(r : (t,m)\mapsto (t,\, m \sqcup \{\text{scores} := s\})\), where \(s\) can be a scalar, vector, or structured record (per-criterion).  The algebraic part is in how you *combine* scores across steps: max/min (lattice-style), weighted sums (semiring-style), or Pareto/frontier (multi-objective) are different monoidal structures with different downstream behavior.  

In existing RAG tooling, “metadata enrichment” is literally implemented as “extract structured fields with an LLM and update the document’s meta,” so your “enrichment” term lines up with common practice .

## Soft typing via (template, rubric)
A “soft type” \( \tau = (\text{template}, \text{rubric})\) can be treated as (1) a *shape* expectation (template) and (2) a *grading/validation* functional (rubric) that returns both a score and diagnostics.  Then “type checking” is not boolean; it’s a score-producing map \(\text{check}_\tau : (t,m)\to (t,\, m\sqcup\{\text{type} := \tau,\, \text{fit}:=s,\, \text{violations}:=\dots\})\).  

This is a good fit for LLM pipelines because steps themselves are specified by texts (prompts/programs-as-text), so you can store the step spec, the intended soft type, and the observed fit score together and let later steps branch on them.

## YAML metadata as the carrier
YAML front matter is a pragmatic choice for `Meta` because it keeps metadata attached to the same artifact as the text and is easy to parse and edit.  A “frontmatter format” convention explicitly generalizes Jekyll-style YAML front matter so you can embed YAML metadata at the top of many file types (Markdown, HTML, Python, SQL, etc.) while keeping the file valid for existing tools.

Architecturally, this makes each artifact a self-describing object: `content` (the text) plus `meta` (scores, types, provenance), and your enrichment steps become pure “meta-writers” whenever you don’t want to rewrite the content.

Example sketch:

```yaml
---
id: doc:pricing-email-042
soft_type:
  template: "customer_email_v1"
  rubric: "helpfulness_rubric_v3"
scores:
  helpfulness: 0.82
  factuality: 0.91
provenance:
  step: "rubric_eval"
  model: "gpt-…"
---
<the actual text here>
```

## Practical pipeline laws (worth enforcing)
- **Monotone enrichment:** An enrichment step should only add/overwrite keys in its declared namespace (e.g. `scores.*`), which makes `Meta` merges predictable and compositional.  
- **Idempotence where possible:** If a step is deterministic given frozen inputs (same rubric text, same model settings, same text), re-running it should not change `Meta`; when that’s not true, store variance/ensembles as explicit structure (e.g. `scores.helpfulness.samples`).  
- **First-class step specs:** Since “pipeline steps are specified by texts,” store each step’s spec text alongside outputs, and treat “changing the spec text” as changing the morphism; that gives you diffability and reproducibility.

We could formalize this as a small typed calculus (objects, morphisms, an explicit `Enrich` combinator, and a notion of “soft type judgment returns a score + evidence”), or map it onto a Kleisli-category model for LLM nondeterminism and failures.
