# Branch B001 — Current Accepted State

## Research Objective

Under a fixed inference-compute budget, which design features of a role-separated multi-agent research loop most reduce unsupported claims and cumulative reasoning errors compared with repeated single-agent prompting?

## Completed Cycle

C0001 is complete and accepted through Cycle Archivist review. The cycle investigated whether fresh role-separated execution can be isolated from structured state, provenance, staged functions, context partitioning, permissions, handoffs, verification, sampling, and compute allocation.

## Accepted Factual Record

- **Branch-design fact:** The B001 protocol combines seven ordered functional roles, fresh conversations, role-specific source and file permissions, externalized control and accepted state, explicit epistemic categories, exact-reference requirements, and stage-gated progression. These are distinct treatment features, not evidence that the design improves accuracy. Provenance: `AGENT_PROTOCOL.md`; `C0001-INT-01` through `C0001-INT-07` in `branches/B001/cycles/C0001/03_internal_evidence.md`.
- **Branch-design fact:** Same-model repetition, confidence, eloquence, or agreement is not independent evidence under the protocol. Provenance: `AGENT_PROTOCOL.md`; `C0001-INT-05`.
- **Search-bounded evidence-gap fact:** No source in the sixteen-source C0001 ledger holds model, task, functional stages, stage instructions, artifacts, information access, tools, evaluator, sampling opportunities, and full inference cost constant while varying only fresh invocation boundaries. This is limited to the completed C0001 search and is not a universal literature claim. Provenance: `branches/B001/cycles/C0001/04_external_evidence.md`, Research Scope and Evidence Gaps; `C0001-INTG-02`.
- **Source-reported fact, preprint:** Under requested thinking-token caps on FRAMES and four-hop MuSiQue, `C0001-SRC-01` reports single-agent systems best or statistically indistinguishable from the best multi-agent architecture in most clean regimes above the effectively non-reasoning 100-token setting. It also reports a partitioned-system crossover under some severe masking or substitution corruption. Prompt, final-answer, planner, aggregator, and state costs were not fully charged, and prompts and information flow were not equalized. Provenance: `C0001-SRC-01`; interpretations `C0001-EXT-01` and `C0001-EXT-06`.
- **Source-reported fact, preprint:** `C0001-SRC-02` reports positive coordination effects on decomposable financial-analysis tasks and dynamic navigation, and substantial degradation on sequential PlanCraft tasks under a shared reasoning-token budget. Architecture-specific orchestration and role prompts remain bundled. Provenance: `C0001-SRC-02`; interpretations `C0001-EXT-02` and `C0001-EXT-09`.
- **Source-reported facts, peer-reviewed:** `C0001-SRC-03` reports self-consistency matching or beating multi-agent debate and Reflexion at comparable query, token, and monetary budgets in its tested settings. `C0001-SRC-04` reports untuned debate as unreliable and generally more costly than simpler baselines. These studies do not equalize all prompts and information structures. Provenance: `C0001-SRC-03`, `C0001-SRC-04`; interpretations `C0001-EXT-07`, `C0001-EXT-08`.
- **Source-reported fact, peer-reviewed:** `C0001-SRC-05` reports gains from same-model multi-agent debate in several tested tasks, but the debate conditions add agents, rounds, calls, and tokens. The result is evidence for structured interaction with added inference, not an isolated fresh-role effect. Provenance: `C0001-SRC-05`; interpretation `C0001-EXT-03`.
- **Source-reported fact, preprint:** `C0001-SRC-06` reports increasing output similarity and diminishing returns as homogeneous agent count rises in vote and debate settings; model, prompt, or tool heterogeneity can preserve diversity. Semantic diversity is not equivalent to factual independence or correct complementarity. Provenance: `C0001-SRC-06`; interpretation `C0001-EXT-05`.
- **Source-reported fact, original failure study:** `C0001-SRC-07` identifies context loss, information withholding, repetition, inter-agent misalignment, and verification or termination failures in analyzed multi-agent traces. The study is primarily observational and diagnostic rather than a fixed-compute causal ablation. Provenance: `C0001-SRC-07`; interpretation `C0001-EXT-09`.
- **Source-reported facts, peer-reviewed:** `C0001-SRC-08` reports gains from one-model iterative feedback and refinement, while `C0001-SRC-09` reports that intrinsic self-correction can fail or turn correct answers into incorrect ones. These findings are task- and signal-dependent and do not isolate role separation. Provenance: `C0001-SRC-08`, `C0001-SRC-09`; External Evidence report, Conflicting or Inconclusive Findings.
- **Source-reported fact, peer-reviewed:** `C0001-SRC-10` reports that models were weak at locating reasoning mistakes but could correct them when given the error location; a small trained locator outperformed prompted large-model localization in that study. This supports a specific verifier function, not replacement of whole roles. Provenance: `C0001-SRC-10`; interpretations `C0001-EXT-03`, `C0001-EXT-10`.
- **Source-reported fact, peer-reviewed:** `C0001-SRC-11` reports factuality improvements from one-model staged draft, verification-question planning, independently answered verification questions, and revision. The method adds inference and does not compare persistent and fresh contexts at equal full cost. Provenance: `C0001-SRC-11`; interpretation `C0001-EXT-03`.
- **Source-reported fact, peer-reviewed:** `C0001-SRC-12` reports long-horizon navigation improvements from reusable external workflow records. The intervention adds information, induction, retrieval, and prompt-context costs and does not test explicit provenance ledgers or matched role separation. Provenance: `C0001-SRC-12`; interpretation `C0001-EXT-04`.
- **Source-reported fact, peer-reviewed:** `C0001-SRC-13` reports gains from sampling multiple independent reasoning paths and selecting the most consistent answer. This is an added-sampling mechanism rather than role specialization. Provenance: `C0001-SRC-13`; External Evidence report, Added Sampling and Voting.
- **Measurement facts:** `C0001-SRC-14` supports atomic fact segmentation and support-precision measurement; `C0001-SRC-15` separates citation correctness from citation completeness; `C0001-SRC-16` adds a coverage-sensitive F1@K proxy. None provides a complete stage-by-stage error-lineage measure for the branch. Provenance: `C0001-SRC-14` through `C0001-SRC-16`; External Evidence report, Factuality Metric Choice and Response Coverage.

## Current Claims

### C0001-INTG-01 — Conditional architecture fit

- **Status:** Accepted derived conclusion.
- **Scope:** The heterogeneous reasoning, question-answering, and agentic tool-task evidence in the C0001 ledger; transfer to open-ended multi-source research synthesis is uncertain.
- **Claim:** Current evidence does not support a general independent benefit from fresh role separation. Workflow effects vary with task decomposability, context condition, validation topology, state completeness, information flow, and coordination overhead.
- **Support:** `C0001-EXT-01`, `C0001-EXT-02`, `C0001-EXT-06` through `C0001-EXT-10`; `C0001-SRC-01` through `C0001-SRC-07`, `C0001-SRC-10` through `C0001-SRC-13`; branch-design facts `C0001-INT-01` through `C0001-INT-07`.
- **Dependencies and limitations:** This conclusion depends on synthesis across studies with different tasks and architectures. It is not a branch-local controlled experimental result and does not establish a zero effect in every regime.

### C0001-INTG-02 — Compute-isolation gap

- **Status:** Accepted evidence-gap conclusion.
- **Scope:** The sixteen-source C0001 ledger.
- **Claim:** The reviewed evidence does not fully isolate fresh role separation from added or differently allocated compute.
- **Support:** External Evidence report, Fixed-Compute Versus Added-Compute Evidence and Evidence Gaps; `C0001-SRC-01`, `C0001-SRC-02`, `C0001-SRC-03`; `C0001-INT-11`.
- **Dependencies and limitations:** Requested reasoning-token caps or mean budgets can leave prompt, context, completion, final-answer, orchestration, state, handoff, tool, sample, and selector costs unequal. This is an absence-of-clean-evidence finding, not proof that no qualifying study exists outside the completed search.

### C0001-INTG-03 — Measurement requirement

- **Status:** Accepted methodological requirement, not an empirical effect claim.
- **Scope:** Future branch experiments and any accepted claim about unsupported claims or cumulative reasoning errors.
- **Claim:** Evaluation must distinguish atomic claims and support correctness, separate citation correctness from completeness, account for factual coverage and task completion, and trace errors across stages as introduced, preserved, corrected, mutated, or amplified.
- **Support:** Critic Fatal Problem 2 and Required Corrections; `C0001-SRC-14`, `C0001-SRC-15`, `C0001-SRC-16`.
- **Dependencies and limitations:** The exact segmentation rules, weighting, omission treatment, adjudication procedure, evaluator mix, and reliability threshold remain unresolved.

### C0001-EXP-06 — Heterogeneous architecture effects

- **Status:** Accepted in narrowed form as a task-, context-, and coordination-regime conclusion.
- **Scope:** Conditions represented by `C0001-SRC-01`, `C0001-SRC-02`, and `C0001-SRC-07`.
- **Claim:** Architecture benefits and harms are not uniform across clean versus degraded context, decomposable versus sequential tasks, and centralized versus weakly validated coordination.
- **Support:** `C0001-EXT-01`, `C0001-EXT-02`, `C0001-EXT-06`, `C0001-EXT-09`; `C0001-SRC-01`, `C0001-SRC-02`, `C0001-SRC-07`.
- **Dependencies and limitations:** The branch has not yet operationalized a general failure-mode taxonomy or established transfer to open-ended research synthesis.

## Current Hypotheses

- **C0001-EXP-01 — Independent fresh-role effect:** Unresolved and weakened. Fresh role-separated execution may have an independent effect after full controls, but no located study isolates it, and near-direct evidence does not show a general advantage. Conditional benefits prevent universal contradiction.
- **C0001-EXP-02 — External memory and provenance:** Qualified. Structured external memory is an active component in some long-horizon navigation settings (`C0001-SRC-12`). Whether external state or explicit provenance dominates fresh invocation structure is unresolved; workflow memory must not be generalized directly to provenance correctness.
- **C0001-EXP-03 — Structured verification:** Qualified. Staged verification can improve some outcomes without multiple nominal agents (`C0001-SRC-11`), and verifier information can matter materially (`C0001-SRC-10`). Equal-compute superiority over fresh roles is unresolved, and generic same-model critique can be unreliable (`C0001-SRC-09`).
- **C0001-EXP-04 — Context-partition benefit:** Narrow hypothesis. Partitioning may help when prior context is severely corrupted or poorly utilized (`C0001-SRC-01`), but fresh invocation boundaries are not independently isolated.
- **C0001-EXP-05 — Interface-loss risk:** Qualified supported risk. Narrow contexts, permission boundaries, and handoffs may omit dependencies, fragment sequential reasoning, or propagate errors (`C0001-SRC-02`, `C0001-SRC-07`). The independent causal contribution of fresh context is unmeasured.
- **C0001-EXP-07 — Function-specific replacement:** Qualified hypothesis. Specialized trained or deterministic checks may replace particular weak verification functions. Replacement of complete critic, evidence, or integration roles is unsupported.
- **Fresh-context-plus-state interaction:** Hypothesis. Fresh execution may reduce contamination only when external state is sufficiently complete to preserve dependencies required for correction and integration.
- **Verifier-quality hypothesis:** Hypothesis. Independent, privileged, deterministic, trained, heterogeneous-model, or human verification signals may outperform a generic same-model critic at comparable cost.
- **Diversity-quality hypothesis:** Hypothesis. Role prompts may help only when they produce nonredundant supported facts or independent correct error detections, not merely stylistic or semantic variation.

## Alternative Explanations

- **Functional scaffolding, external memory, and verifier information:** Mandatory generation, challenge, evidence, and revision stages, together with external state and higher-quality verification signals, may account for most useful effects; fresh invocation boundaries may add little once information and compute are equalized.
- **Budget allocation, sampling, and selection:** Candidate count, independent sampling, selector quality, actual consumed compute, prompt tuning, and favorable metric construction may explain much of the apparent multi-agent gain.
- **Minimal null:** After full controls, fresh role separation may have no stable average independent effect. Positive and negative results may arise from task-architecture interactions and coordination overhead.
- **Decomposition plus centralized verification:** Parallel evidence gathering may help on separable tasks when a central validation bottleneck prevents propagation, while the same structure may be harmful on sequential tasks.
- **Fresh-context contamination control:** Fresh contexts may help mainly when prior context is misleading and state is complete; otherwise the same partition can become information loss.

## Known Objections and Contradictions

- Same-model agents can produce correlated or redundant judgments; agreement is not independent validation.
- Added roles can consume fixed budget, duplicate work, create handoff overhead, and introduce additional error-propagation paths.
- Apparent gains can come from added sampling, revision, retrieval, external memory, privileged verifier information, prompt tuning, or selector quality.
- Fixed token caps can conceal unequal prompt, context-processing, completion, final-answer, orchestration, state, handoff, tool, candidate, and selector costs.
- A workflow can lower unsupported-claim counts by making fewer factual claims or reducing task coverage.
- Same-model or LLM-as-judge evaluation may share the tested system’s biases.
- **Positive debate versus budget-aware neutral or negative evidence:** `C0001-SRC-05` reports added-compute gains, while `C0001-SRC-01`, `C0001-SRC-03`, and `C0001-SRC-04` report ties, losses, or simpler-baseline competitiveness under tighter accounting. Differences in inference, tuning, models, and tasks explain part but not all of the tension.
- **Self-refinement versus weak intrinsic self-correction:** `C0001-SRC-08` reports gains, while `C0001-SRC-09` reports failures or degradation. `C0001-SRC-10` suggests error-location and verifier information may be a key moderator.
- **Context partitioning versus interface loss:** `C0001-SRC-01` reports a benefit under some severe context corruption, while `C0001-SRC-02` and `C0001-SRC-07` report sequential degradation, context loss, and information withholding.
- **Diversity versus capability saturation:** `C0001-SRC-06` reports benefits from heterogeneity, but `C0001-SRC-02` does not show heterogeneous teams universally overcoming the strongest model’s limits. Diversity must be evaluated for correctness and complementarity.
- **Traceability versus support:** `C0001-SRC-14` through `C0001-SRC-16` show that atomic support precision, citation correctness, citation completeness, and coverage are distinct. More citations or provenance links do not by themselves establish correct or complete support.

## Rejected or Superseded Claims

- **Rejected:** General superiority of multi-agent or seven-role workflows over repeated or staged single-model prompting under fixed compute.
- **Rejected:** The Explorer’s four-condition ladder as a clean causal isolation design.
- **Rejected:** Same-model role agreement as independent corroboration.
- **Rejected:** Positive added-compute debate, refinement, verification, sampling, or memory results as direct proof of an independent fresh-role effect.
- **Rejected:** Citation presence, provenance-link counts, or raw unsupported-claim counts as sufficient epistemic evaluation.
- **Rejected:** Performance loss after role deletion as proof of unique role value unless the handling of freed compute is declared.
- **Rejected:** Broad deterministic replacement of whole critic, evidence, or integration roles.
- **Superseded wording:** “Role separation may reduce cumulative error by limiting objectives and context” is retained only as `C0001-EXP-01`, `C0001-EXP-04`, and `C0001-EXP-05` with the scopes and objections above.
- **Superseded wording:** “Externalized memory and explicit provenance may matter more than agent count” is replaced by the narrower `C0001-EXP-02`; memory is supported in some long-horizon tasks, while comparative dominance and explicit-provenance effects remain unresolved.

## Unresolved Questions

- What exact factor defines role separation for B001: objective specialization, invocation boundary, context reset, permissions, handoff format, or a declared combination?
- What is the primary fixed-compute matching rule, and which secondary resource measures must always be recorded?
- Can persistent staged and fresh staged workflows receive identical intermediate messages, evidence, artifacts, verifier inputs, samples, selectors, and final integration access?
- How should atomic claims, support, interpretation, hedging, omissions, claim importance, factual coverage, task completion, and usefulness be coded?
- How will an error be linked across stages as introduced, preserved, corrected, mutated, or amplified?
- What evaluator design reduces shared-model bias and establishes inter-rater reliability?
- Does fresh execution retain an effect after equalizing state, stages, evidence, verifier information, samples, selection opportunities, tools, and full cost?
- Does structured state dominate fresh context, or is there a fresh-context-by-state-completeness interaction?
- Which roles add unique function under both budget-removed and budget-reallocated ablations?
- Which task strata show positive, neutral, or negative effects?
- Do results from short-answer reasoning, static QA, and tool benchmarks transfer to multi-source open-ended research synthesis?

## Current Research Status

C0001 is completed and archived. The branch now has a qualified sixteen-source external record and accepted methodological conclusions, but no branch-local controlled experiment has established an independent fresh-role effect. The principal accepted direction is conditional architecture fit, not general multi-agent superiority.

## Suggested Next Areas

1. Define the branch estimand, factor matrix, and a full compute ledger that charges prompt and context processing, completions, final answers, state construction, handoff generation, orchestration, tools, candidate generation, and selection.
2. Define a coverage-sensitive evaluation protocol combining atomic support correctness, citation correctness and completeness, factual coverage, task completion, and adjudicated stage-by-stage error lineage.
3. Run the primary fresh-boundary isolation contrast: identical stages, messages, artifacts, evidence, tools, verifier inputs, samples, selectors, and integration rules in one persistent context versus fresh invocations.
4. Run a sampling-equated contrast and a verifier-information contrast after the primary design is coherent.
5. Later run role ablations twice: once with freed compute unused and once with freed compute reallocated.