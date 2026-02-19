# Plan: Evaluation Feedback Loop (Send Back to Committee Below Threshold)

**Goal:** When the independent evaluation scores a deliberation below a configurable threshold, the evaluation is sent back to the committee. The committee acts on the critique (e.g. takes recommendations, adds a round, revises synthesis) to raise scores. This is a **general feature of the methodology**, not specific to one debate.

**Scope:** Planning only. No changes to skills or artifacts until this plan is approved.

**Decisions (locked in):**
- **Variant 2:** Remediation as separate files (05-remediation-1.md, 07-remediation-2.md).
- **Score:** **Sum** of five rubric scores (0–15).
- **Threshold:** **Sum &lt; 13** triggers remediation (pass if sum ≥ 13). Default **13**; overridable in the **convening file** (01-convening.md or a designated place that defines how this debate will run).
- **Max remediation rounds:** **2**.
- **Invocation wording:** For explanatory logs use **"Committee respond to evaluation"**; where brevity counts use **"remediation"**.
- **Threshold/config:** Stored in convening (parameters of how the debate will run); no need to duplicate in the evaluation file.
- **First evaluation file:** Always **04-evaluation-1** (always use a number; no 04-evaluation.yml).
- **Committee output:** Always directory (no inline-only mode).
- **Artifacts:** Add "Evaluation feedback loop" subsection to `artifacts/independent-evaluation.md` and link from `artifacts/README.md`.

---

## 1. Threshold and Trigger

- **Score:** **Sum** of the five rubric scores (0–15). Each rubric 0–3; total 0–15.
- **Threshold:** Sum **&lt; 13** → below bar → trigger remediation. Default **13**; overridable in the **convening file** (e.g. 01-convening.md or a small config that defines how this deliberation runs).
- **Trigger:** After review writes to an evaluation file (e.g. `04-evaluation-1.yml`), check: **sum &lt; threshold** (default 13) → invoke remediation (committee respond to evaluation). Type: **remediation** (e.g. `05-remediation-1.md`).
- **Cap:** **Max 2 remediation rounds.** After 2 rounds, stop even if still below threshold; document "improved but below bar."

---

## 2. Two Schemes

### Scheme A: Append-only re-deliberation (response round in 02)

**Flow:**
1. Committee runs → 00, 01, 02, 03 written.
2. Review runs → **04-evaluation-1.yml** written with `transcript_review` (aggregate, recommendations, etc.).
3. If aggregate &lt; threshold: **Committee is re-invoked** (remediation round) with inputs: charter (00), full transcript (02), evaluation (04). Instructions: "The independent evaluation scored this deliberation below the acceptable threshold. Your task: address the critique. You may add another round of debate (addressing the evaluator's recommendations), revise the synthesis/resolution, or take another tactic to raise the scores. Output: append to 02-deliberation.md a new section **## Response to evaluation** containing your additional round(s) and any revised Final Consensus / KEY TENSIONS / DECISION SPACE MAP / VERDICT; if the resolution changes, update 03-resolution.yml."
4. Append to **02-deliberation.md**: a single new section "## Response to evaluation" (and optionally "## Round 2 Analysis", "## Revised consensus", etc.). Do **not** overwrite the original transcript.
5. If 03 was revised, overwrite or version 03-resolution.yml.
6. Re-run review on the **full** 02 (including the new section). Write the new review to **04-evaluation-2.yml** (second evaluation file).
7. If aggregate ≥ threshold, stop. Else repeat from step 3 up to max rounds (next: 05-remediation-2, then 06-evaluation-3, etc.).

**Artifacts:**
- 02 grows by one (or more) "Response to evaluation" blocks.
- **04-evaluation-1.yml**, **04-evaluation-2.yml**, … (one evaluation file per review; multiple evaluations when the loop runs).

**Pros:**
- Single transcript file; full audit trail (original + response) in one place.
- No new file types; fits existing 00–04 layout.
- Committee has full freedom (extra round, revised synthesis, or other tactic).
- Simple mental model: "below bar → committee gets another turn."

**Cons:**
- No formal requirement to respond point-by-point to recommendations; committee might address critique vaguely.
- 02 can get long after multiple rounds.
- Need a clear convention for multiple evaluations in 04 (e.g. list of rounds vs. single latest).

---

### Scheme B: Remediation (structured response document)

**Flow:**
1. Same as Scheme A through step 2 (committee → review → **04-evaluation-1.yml**).
2. If aggregate &lt; threshold: Frame the evaluation as a **motion to recommit** (Robert's Rules): "The evaluator moves to recommit the deliberation to the committee with the following amendments: [list of recommendations from the evaluation file]."
3. Committee is re-invoked with: charter, 02, and the latest evaluation file (e.g. 04-evaluation-1.yml). Instructions: "You are the committee. The evaluator has moved to recommit with the amendments above. You must reconvene and produce a **point-by-point response** (remediation): for each recommendation, state whether you accept it, reject it (with reason), or amend it, and what you will add or change. Then add to the deliberation (e.g. a new round) and update synthesis/resolution as needed. Output: (1) A **05-remediation-1.md** (or a fixed section in 02) that maps each recommendation to your response; (2) Appended material in 02 (new round addressing the recommendations); (3) Updated 03 if needed."
4. Create **05-remediation-1.md** (first remediation round). Content: e.g. "Recommendation 1: [text]. Committee response: [accept / reject because … / amend: …]. We add the following to the transcript: …"
5. Append the new round to 02; update 03 if applicable.
6. Re-run review on full 02; store result in **06-evaluation-2.yml** (second evaluation file). Chronology index increments so lexical order stays chronological: 04-evaluation-1 → 05-remediation-1 → 06-evaluation-2 → 07-remediation-2 → 08-evaluation-3, etc.
7. If aggregate ≥ threshold, stop; else repeat from step 3 up to max rounds (next: **07-remediation-2.md**, then **08-evaluation-3.yml**, etc.).

**Artifacts:**
- 02 gains "Response to evaluation" content (new round(s)).
- **05-remediation-1.md**, **07-remediation-2.md**, … (type: **remediation**; chronology index 05, 07, …; one file per remediation round).
- **04-evaluation-1.yml**, **06-evaluation-2.yml**, **08-evaluation-3.yml**, … (type: **evaluation**; chronology index 04, 06, 08, …; one file per review).

**Pros:**
- Clear accountability: every evaluator recommendation gets an explicit response.
- Aligns with Robert's Rules (motion to recommit); fits existing protocol language.
- Evaluator (or user) can verify that each gap was addressed.
- Good for methodology documentation and teaching.
- **If remediation is a separate file (05-remediation-1, etc.):** Lexical sort (00→…→04-evaluation-1→05-remediation-1→06-evaluation-2→…) matches chronological order; and **presence of 05-remediation-* (or any 05-*, 06-*, …) is visible at a glance** — you can see which deliberations "went overtime." That can be a useful signal (e.g. question complexity, contentiousness, or first-pass quality) without opening files.

**Cons:**
- New artifact (05) or a rigid section format in 02; schema and README must be updated.
- More formal; risk of bureaucratic feel if responses are shallow.
- Slightly more complex flow (two outputs: 05 + 02 update).

---

## 3. Weighing the factors

| Factor | Scheme A (append-only) | Scheme B (motion to recommit) |
|--------|------------------------|--------------------------------|
| **Auditability** | Good (full transcript in 02); weaker on "did they address each point?" | Better (explicit recommendation → response) |
| **Simplicity** | Simpler: no new file; one place to look | More structure: 05 or fixed section; two places to look |
| **Methodology fit** | Generic "do another round" | Strong fit: Robert's Rules, formal recommit |
| **Flexibility** | Committee can respond in any form | Committee encouraged to respond point-by-point; can still add round + 05 |
| **Adoption cost** | Low: review + committee skills only | Medium: review + committee + 05 schema + deliberations README |
| **Risk of shallow response** | Higher (committee might summarize vaguely) | Lower (05 forces mapping) |

**Weighing:** Accountability and methodology fit favor Scheme B. Simplicity and lower adoption cost favor Scheme A. For a *general* feature that will be used across many deliberations, **accountability** (did the committee actually act on the critique?) matters more than minimal artifact set. Scheme B's point-by-point response also makes it easier to re-run review and check "did this recommendation get addressed?" without re-reading the whole transcript. The extra artifact (05) is a small, one-time schema cost.

**Decision:** **Scheme B, Variant 2** — Remediation as **separate files**: **05-remediation-1.md**, **07-remediation-2.md**, … (chronology index increments so 04-evaluation-1 → 05-remediation-1 → 06-evaluation-2 → 07-remediation-2 sort correctly). Multiple evaluations: **04-evaluation-1.yml**, **06-evaluation-2.yml**, **08-evaluation-3.yml**, …. Invocation: use **"Committee respond to evaluation"** in explanatory logs; use **"remediation"** where brevity counts.

---

## 4. What would have to change (general)

### 4.1 Review skill (`.claude/skills/review/SKILL.md`)

- **Threshold:** Document that the score is the **sum** of five rubrics (0–15). **Sum &lt; 13** (default) triggers remediation. Threshold is overridable in the **convening file** (parameters of how this debate will run). Below threshold → send back to committee (remediation).
- **After writing the evaluation file:** State that if **sum &lt; threshold** (default 13), the user or workflow should invoke the committee to run a **remediation** round ("Committee respond to evaluation" / "remediation"); point to the committee skill.
- **Multiple evaluations:** Each review is written to a separate evaluation file (04-evaluation-1.yml, 06-evaluation-2.yml, …). The **latest** evaluation file's **sum** is used for the pass/fail check. **Max 2 remediation rounds.**

### 4.2 Committee skill (`.claude/skills/committee/SKILL.md`)

- **New mode:** "Response to evaluation" or "Re-deliberate from evaluation." Triggered when the user (or workflow) invokes the committee with a deliberation directory whose 04 shows aggregate below threshold.
- **Inputs:** Read 00-charter.yml, 02-deliberation.md, and the latest evaluation file (e.g. 04-evaluation-1.yml or 06-evaluation-2.yml) — especially `transcript_review`: scores, biggest_gaps, recommendations.
- **Instructions:** (1) Frame the evaluation as a motion to recommit with the listed recommendations. (2) Produce a **remediation** artifact: either a section "## Response to evaluation (motion to recommit)" in 02, or a separate file **05-remediation-1.md** (then 07-remediation-2.md, etc.): for each recommendation, state accept / reject with reason / amend, and what the committee will add or change. (3) Produce "## Round 2: [topic]" (or similar): a new round of debate that addresses those points. (4) Produce any revised "Final Consensus," "KEY TENSIONS," "DECISION SPACE MAP," "VERDICT," "CONCLUSION" if changed. (5) Append all of that to 02-deliberation.md. (6) If the resolution changes, update 03-resolution.yml.
- **Output:** Remediation file (05-remediation-1.md, etc.) if using Variant 2; append to 02; optionally update 03. Next review writes to the next evaluation file (06-evaluation-2.yml, etc.).
- **Max rounds:** **2 remediation rounds**; after that, stop and report "improved but below threshold."

### 4.3 Deliberation record schema (agent/deliberations/README.md, augmentation-plan.md)

- **02-deliberation.md:** Allow optional section "## Response to evaluation (motion to recommit)" and "## Round 2: …" (and Round 3 if max &gt; 1). Describe that these appear when the feedback loop runs.
- **Evaluation files:** Use **04-evaluation-1.yml** for the first review; when the loop runs, write subsequent reviews to **06-evaluation-2.yml**, **08-evaluation-3.yml**, … (chronology index increments). Type: **evaluation**; suffix -1, -2, … per review. The **latest** evaluation file's aggregate is used for the threshold check.
- **Remediation files:** **05-remediation-1.md**, **07-remediation-2.md**, … (type: **remediation**; chronology index 05, 07, …). **Convening file** holds the parameters (threshold, max remediation rounds); no need to duplicate in the evaluation file.

### 4.4 Artifacts (optional)

- **artifacts/independent-evaluation.md** (or similar): Add a short "Evaluation feedback loop" subsection: when score is below threshold, send the evaluation back to the committee; committee responds (motion to recommit); re-review; repeat until pass or max rounds.
- **artifacts/README.md:** If we add a new doc for the loop, link it next to "Independent evaluation."

### 4.5 Invocation (user or tooling)

- **Manual:** User runs `/committee [topic]` → review runs → if below threshold, user runs "committee respond to evaluation for agent/deliberations/&lt;topic-slug&gt;" (or similar). Then runs review again.
- **Semi-automated:** A script or agent that (1) runs committee, (2) runs review, (3) if aggregate &lt; threshold, runs "committee respond to evaluation" for that directory, (4) runs review again, (5) repeats until aggregate ≥ threshold or max rounds. No skill changes required for this; the skills only need to support the "response to evaluation" mode and multi-round 04.

### 4.6 Threshold and convening

- **Default threshold:** Sum 13 (pass if sum ≥ 13). **Overridable in the convening file** (01-convening.md or a designated place) so each deliberation can specify how it will run (e.g. `remediation_threshold: 12`, `max_remediation_rounds: 2`).

---

## 5. Summary

- **Trigger:** **Sum &lt; 13** (default; overridable in convening) after transcript review → committee does **remediation** (05-remediation-1.md, etc.). **Max 2** remediation rounds. Score = **sum** of five rubrics (0–15). Multiple evaluations and remediations use incrementing chronology indices (04, 05, 06, 07, …).
- **Chosen scheme:** Scheme B — **remediation** (type name). Structured response in 02 or in separate files **05-remediation-1.md**, **07-remediation-2.md**, …; multiple **evaluation** files **04-evaluation-1.yml**, **06-evaluation-2.yml**, ….
- **Committee:** Gets 00, 02, and latest evaluation file; produces remediation (point-by-point) and "Round 2"; append to 02, update 03; next review writes to next evaluation file (06-evaluation-2.yml, etc.).
- **Review:** Re-run on full 02; write to next evaluation file (06-evaluation-2.yml, 08-evaluation-3.yml, …); check threshold again; stop when pass or max rounds.
- **Changes:** Review skill (threshold, multi-round 04, when to send back); committee skill (response-to-evaluation mode, inputs, output format); deliberations README and augmentation-plan (02 section, 04 multi-round); optional artifacts; invocation pattern (manual or script).

No edits to the repo are made in this plan; implement when approved.
