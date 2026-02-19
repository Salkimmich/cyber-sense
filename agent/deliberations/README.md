# Deliberation Records

This directory holds **directory-structured deliberation records** produced by the cyber-sense committee skill. Every `/committee [topic]` run creates a new subdirectory here (e.g. `agent/deliberations/microservices-adoption/`) and writes the standard set of files; there is no single-file or inline-only output. The review skill reads from these directories and can write the evaluation file. The **example/** subdirectory contains minimal template files showing the structure.

## Naming convention

Filenames are **`<chronology>-<type>[-<suffix>].<ext>`**:

- **Numeric prefix (00, 01, 02, …)** = **chronology index** — order in the process. They are not file-type IDs; they ensure files sort in chronological order.
- **The rest of the name** = **type** — charter, roster, convening, deliberation, resolution, evaluation, remediation, etc.
- **Optional suffix** — When there is more than one instance of the same type, use **incrementing suffixes** (-1, -2, …) to keep filenames unique: e.g. `04-evaluation-1.yml`, `04-evaluation-2.yml` (multiple reviews); `05-remediation-1.md`, `05-remediation-2.md` (multiple remediation rounds).

So the "real" type is the type name (charter, deliberation, …); the number is when it occurs in the sequence. When the feedback loop runs (evaluate → remediate → re-evaluate → …), both evaluations and remediations can have multiple instances; the **chronology index** (04, 05, 06, 07, …) increments for each new file so lexical sort stays chronological (e.g. 04-evaluation-1 → 05-remediation-1 → 06-evaluation-2 → 07-remediation-2).

## Structure (per deliberation)

| File | Type | Purpose |
|------|------|---------|
| `00-charter.yml` | charter | Goal, context, success criteria, exit conditions, deliverable format |
| `01-roster.yml` | roster | Fixed 5-member committee (Maya, Frankie, Joe, Vic, Tammy); roles and propensities |
| `01-convening.md` | convening | Selection rationale, composition notes, outcome. Optional **Remediation parameters** (for the evaluation feedback loop): **remediation_threshold** (default 13; pass if sum of five rubric scores ≥ this), **max_remediation_rounds** (default 2). Add a short "Remediation parameters" section when this deliberation uses non-default values. |
| `02-deliberation.md` | deliberation | Full transcript: opening statements, rounds, analyses, consensus, decision space map |
| `03-resolution.yml` | resolution | Decision, summary, votes, implementation plan, signatures |
| `04-evaluation-1.yml` | evaluation | First review: resolution-only evaluation and/or transcript review (rubric scores, verdict). **Always use a number** for the first evaluation file (04-evaluation-1.yml). |
| `04-evaluation-2.yml`, … | evaluation | Subsequent reviews after remediation rounds (suffix -2, -3, …). |
| `05-remediation-1.md`, … | remediation | Committee’s response to evaluation (point-by-point, new round in 02). Present when the deliberation “went overtime.” Suffix for each remediation round. |

Optional (when evaluation feedback loop runs): `05-remediation-1.md`, then `06-evaluation-2.yml`, then `07-remediation-2.md`, then `08-evaluation-3.yml`, etc. (chronology index increments so order is preserved).

**Evaluation files** (04-evaluation-1.yml, 04-evaluation-2.yml, …) can contain (both optional):

- **resolution_evaluation** — Charter vs resolution only (no transcript). Reviewer reads `00-charter.yml` and `03-resolution.yml`, scores alignment_with_goal, completeness, feasibility, risk_mitigation; writes outcome (RATIFIED | REVISE | REJECT), critique, recommendation. Request via the review skill: e.g. "evaluate the resolution" or "run resolution-only evaluation" for this directory.
- **transcript_review** — Full transcript evaluation. Reviewer reads `02-deliberation.md` (and optionally `00-charter.yml`), scores the five rubrics (reasoning completeness, adversarial rigor, assumption surfacing, evidence standards, trade-off explicitness), writes verdict (High/Medium/Low), biggest_gaps, recommendations. Produced when you run `/review agent/deliberations/<topic-slug>`; the review skill writes to the appropriate evaluation file (04-evaluation-1.yml for first review, 04-evaluation-2.yml after first remediation, etc.).

All paths and references stay **under the cyber-sense repository**. Roster and character details come from `.claude/skills/committee/SKILL.md` and `artifacts/character-propensity-reference.md`; evaluation rubrics from `.claude/skills/review/SKILL.md` and `artifacts/evaluation-rubrics-reference.md`.

See **agent/archive/augmentation-plan.md** for full schemas and implementation details; **agent/investigation-report.md** for how this structure was derived.

## File formats: why YAML vs Markdown

- **YAML** (`.yml`) is used for **charter** (00), **roster** (01-roster), **resolution** (03), and **evaluation** (04-evaluation-1, 06-evaluation-2, …). These are **structured data**: key-value trees, lists, numeric scores, and identifiers. YAML is easy for tools or scripts to parse (e.g. threshold check on sum of rubric scores, roster membership).
- **Markdown** (`.md`) is used for **convening** (01-convening), **deliberation** (02), and **remediation** (05-remediation-1, …). These are **narrative**: prose, sections, and human-readable debate. Markdown is the right fit for long-form text and for places where the primary consumer is a human reader.

Evaluation could be expressed in Markdown with YAML frontmatter (scores in frontmatter, rationale in the body) if human readability of the full file is preferred; the current choice is **YAML** for consistent parsing and a single format for all score-bearing and config-bearing files.
