# Integrator — C0001

## Research Question Addressed

Under a fixed inference-compute budget, does fresh role-separated execution independently reduce unsupported claims and cumulative reasoning errors relative to repeated or staged single-model prompting, once structured memory, provenance, functional stages, information access, verification, tools, sampling opportunities, and evaluation are controlled?

C0001 does not answer that causal question directly. It establishes that the branch protocol bundles several distinct interventions and that no located study varies only fresh role-separated execution while holding the other factors and full inference cost constant.

## Evidence Assessment

### Sourced facts

1. The branch protocol implements seven ordered roles in fresh conversations, uses role-specific file and source permissions, externalizes control and accepted state, requires epistemic typing and exact references, and forbids treating same-model agreement as independent evidence (`C0001-INT-01` through `C0001-INT-07`; `AGENT_PROTOCOL.md`). These are facts about the branch design, not evidence that the design improves accuracy.

2. No located external study satisfies the target estimand exactly: identical model, task, stage functions, stage instructions, artifacts, information, tools, evaluator, sampling opportunities, and full inference cost, with only fresh invocation boundaries varied (External Evidence Researcher, Research Scope and Evidence Gaps; `C0001-EXT-06`; `C0001-SRC-01`, `C0001-SRC-02`).

3. The closest matched reasoning-token comparison reports that single-agent systems are usually best or statistically indistinguishable from the best multi-agent architecture on clean multi-hop reasoning, except for an effectively non-reasoning 100-token regime; partitioned execution can cross over under severe masking or substitution corruption (`C0001-EXT-01`, `C0001-EXT-06`; `C0001-SRC-01`). The comparison does not charge all prompt, final-answer, planner, aggregator, or state costs and does not equalize prompts and information flow.

4. A controlled agent-architecture benchmark reports positive coordination effects on decomposable financial-analysis tasks and dynamic navigation, but large negative effects on sequential PlanCraft tasks under a shared reasoning-token budget (`C0001-EXT-02`, `C0001-EXT-09`; `C0001-SRC-02`). Architecture-specific orchestration and role prompts remain bundled, and the source is a preprint.

5. Budget-aware comparisons report that self-consistency can match or beat multi-agent debate and Reflexion at comparable query, token, and monetary budgets, while debate diversity can decline through dependent rounds (`C0001-EXT-07`; `C0001-SRC-03`). Untuned debate is also reported as unreliable and generally more costly than simpler baselines (`C0001-EXT-08`; `C0001-SRC-04`).

6. Positive debate, self-refinement, Chain-of-Verification, self-consistency, and workflow-memory studies add inference, samples, verification work, retrieval, or information relative to simple baselines (`C0001-EXT-03`, `C0001-EXT-04`, Fixed-Compute Versus Added-Compute Evidence; `C0001-SRC-05`, `C0001-SRC-08`, `C0001-SRC-11`, `C0001-SRC-12`, `C0001-SRC-13`). They support component mechanisms but do not isolate fresh role separation.

7. Chain-of-Verification improves factuality using one model with staged draft, verification-question planning, independently answered verification questions, and revision (`C0001-EXT-03`; `C0001-SRC-11`). This shows that multiple nominal agent identities are not necessary for at least one useful verification structure, but the method adds inference and is not a fixed-compute persistent-versus-fresh comparison.

8. A mistake-localization study reports that models can correct errors when given their location but are poor at locating errors themselves; a small trained locator outperformed prompted large-model localization in that setting (`C0001-EXT-03`, `C0001-EXT-10`; `C0001-SRC-10`). This is evidence about verifier information and specialization, not generic role count.

9. Agent Workflow Memory reports improved long-horizon navigation performance from reusable external workflow records (`C0001-EXT-04`; `C0001-SRC-12`). The intervention adds information, induction, retrieval, and prompt context and therefore does not establish whether memory replaces or complements role separation under equal information and cost.

10. Homogeneous same-model outputs become increasingly redundant as agent count rises in vote and debate experiments, while model, prompt, or tool heterogeneity can preserve diversity (`C0001-EXT-05`; `C0001-SRC-06`). Semantic diversity is not equivalent to independent correctness, and this source is a preprint on mostly static benchmarks.

11. Trace analysis across multi-agent frameworks identifies context loss, information withholding, repetition, inter-agent misalignment, and verification or termination failures as observed failure categories (`C0001-EXT-09`; `C0001-SRC-07`). This supports interface loss as a real risk, but the study is primarily observational rather than a fixed-compute causal ablation.

12. FActScore, ALCE, and SAFE provide complementary measurement components: atomic factual support precision, citation correctness and completeness, and a coverage-sensitive F1@K proxy (`C0001-EXT-05` discussion of factuality metrics; `C0001-SRC-14`, `C0001-SRC-15`, `C0001-SRC-16`). None supplies the branch’s full stage-by-stage cumulative-error lineage measure.

### Source interpretations

- The external record weakens any general claim that a seven-role or multi-agent workflow improves accuracy merely because it separates roles. The near-direct and budget-aware evidence is neutral or negative in many clean reasoning settings (`C0001-EXT-06` through `C0001-EXT-10`).
- Positive results are better explained as conditional effects of task decomposition, search breadth, verification quality, external memory, context management, sampling, or selector quality than as evidence for agent identity or fresh invocation boundaries alone (`C0001-EXT-01` through `C0001-EXT-05`; `C0001-EXT-07`).
- Same-model role agreement cannot be counted as independent validation. The protocol already prohibits that inference (`C0001-INT-05`), and adjacent diversity evidence supports redundancy as a practical concern (`C0001-EXT-05`).

### Derived conclusions

- C0001 provides no adequate basis to accept an independent fresh-role effect.
- The strongest current synthesis is conditional architecture fit: workflow structure can help when it matches task decomposition, context conditions, and verification needs, and can harm when coordination overhead, handoff loss, or sequential dependencies dominate.
- Evidence does not truly isolate role separation from added compute. The strongest studies control a requested or mean reasoning-token budget, but none fully equalizes prompts, context processing, final-answer generation, state construction, handoff creation, orchestration, tool calls, independent candidate count, and selector opportunities.
- Externalized memory, staged verification, verifier information, and sampling are supported as active or plausible components, but their relative contributions within an informationally and computationally matched role-separated comparison remain unresolved.

## Main Interpretation

The main interpretation is **conditional architecture fit, with no established general independent benefit from fresh role separation**.

Fresh role-separated execution is one implementation of a larger bundle: objective specialization, mandatory stage order, fresh context, role-specific permissions, controlled information access, external state, claim and provenance records, handoff compression, verification stages, and budget allocation (`C0001-INT-01` through `C0001-INT-07`). A full-loop improvement would not identify which element caused the change.

The external evidence is consistent with a moderator model:

- Decomposition and parallel breadth can help when subtasks are separable and coordination provides a validation bottleneck (`C0001-EXT-02`; `C0001-SRC-02`).
- Partitioned information flow may help when a unified context is materially corrupted or poorly utilized (`C0001-EXT-01`; `C0001-SRC-01`).
- The same coordination can harm sequential reasoning, tool-heavy execution, or incomplete-handoff settings (`C0001-EXT-09`; `C0001-SRC-02`, `C0001-SRC-07`).
- Structured verification can improve factuality without multiple agent identities, but verifier information and added inference are material (`C0001-EXT-03`, `C0001-EXT-10`; `C0001-SRC-10`, `C0001-SRC-11`).
- Homogeneous same-model agents are not independent judges and can become redundant (`C0001-EXT-05`; `C0001-SRC-06`).

The appropriate branch-level conclusion is therefore not that role separation works or fails universally. It is that **fresh role separation remains an unisolated implementation variable whose sign and magnitude may depend on task structure, state completeness, verifier quality, information topology, and compute allocation**.

## Alternative Interpretations

### 1. Functional scaffolding, external memory, and verifier information are the main active ingredients

This alternative is evidence-backed as a serious explanation but not directly proven against an identical fresh-invocation condition. Single-model staged verification, external workflow memory, and specialized error localization all show that useful functions can arise without nominally separate agents (`C0001-EXT-03`, `C0001-EXT-04`, `C0001-EXT-10`; `C0001-SRC-10`, `C0001-SRC-11`, `C0001-SRC-12`). It predicts that persistent staged execution will match fresh execution when prompts, artifacts, evidence, verifier inputs, and compute are equal.

### 2. Budget allocation, sampling, selection, and metric construction explain much of the apparent gain

This alternative is strongly supported as a confound and partial explanation. Self-consistency can outperform dependent debate at comparable resource levels, positive debate studies usually add agents and rounds, and unsupported-claim metrics can reward short or low-coverage answers (`C0001-EXT-07`, `C0001-EXT-08`; `C0001-SRC-03`, `C0001-SRC-04`, `C0001-SRC-05`, `C0001-SRC-13` through `C0001-SRC-16`). It does not fully explain coordination benefits on decomposable tasks or benefits from added external memory.

### 3. Minimal null: no stable average independent role-separation effect

This remains viable. It predicts near-zero or unstable average effects after full controls, with positive effects on decomposable or degraded-context tasks and negative effects on sequential or coordination-heavy tasks (`C0001-EXT-01`, `C0001-EXT-02`, `C0001-EXT-06`, `C0001-EXT-09`). It is not equivalent to claiming that workflow structure never matters.

### 4. Fresh context reduces contamination under specific conditions

This remains plausible but weakly isolated. The masking and substitution crossover supports a narrow context-partition mechanism (`C0001-EXT-01`), while context-loss findings and clean-context results limit the claim (`C0001-EXT-06`, `C0001-EXT-09`). A fresh context may help only when prior context is misleading and external state remains sufficiently complete.

### 5. Hybrid decomposition plus centralized verification

This is the strongest mechanism-specific hybrid. Parallel workers may broaden evidence collection, while a central verifier limits error propagation (`C0001-EXT-02`, `C0001-EXT-09`). It predicts benefits on separable tasks with high-quality validation and costs on sequential tasks or weak-verifier settings.

## Claim Decisions

### Claim ID: C0001-EXP-01

- **Proposed status:** Unresolved and weakened; do not accept as a current claim.
- **Evidence and source IDs:** `C0001-EXT-06`, `C0001-EXT-07`, `C0001-EXT-08`; `C0001-SRC-01`, `C0001-SRC-03`, `C0001-SRC-04`; Critic Fatal Problem 1 and Material Problems 1–3.
- **Reasoning:** No study isolates distinct objectives in fresh invocations from staging, context, handoffs, information access, sampling, or compute. The closest matched-budget evidence finds no general multi-agent advantage.
- **Scope:** Independent effect of fresh role-separated execution under full controls.
- **Limitations:** Conditional benefits on decomposable or degraded-context tasks prevent treating the hypothesis as contradicted universally.

### Claim ID: C0001-EXP-02

- **Proposed status:** Qualified hypothesis; narrower component claim accepted, comparative dominance unresolved.
- **Evidence and source IDs:** `C0001-EXT-04`; `C0001-SRC-12`; `C0001-INT-03`, `C0001-INT-04`; External Evidence Researcher, Evidence Gaps 4 and 11.
- **Reasoning:** Structured external memory can improve some long-horizon tasks and is a material treatment feature in the branch. No evidence shows that memory and provenance are the main ingredient after equalizing information and construction cost, and the cited memory study does not evaluate unsupported claims or provenance correctness.
- **Scope:** External memory as an active component in long-horizon agent tasks.
- **Limitations:** Do not generalize from workflow memory to explicit claim provenance, and do not infer that memory replaces role separation.

### Claim ID: C0001-EXP-03

- **Proposed status:** Qualified and narrowed.
- **Evidence and source IDs:** `C0001-EXT-03`, `C0001-EXT-07`, `C0001-EXT-10`; `C0001-SRC-03`, `C0001-SRC-08`, `C0001-SRC-10`, `C0001-SRC-11`.
- **Reasoning:** Structured verification and revision can improve some outcomes without multiple agent identities. However, the stronger wording “matter more than agent identity” is not directly tested under equal compute and information. Generic same-model critique is unreliable unless it receives useful independent or privileged information.
- **Scope:** Staged verification as a potentially useful mechanism.
- **Limitations:** Most positive studies add inference; results are task- and verifier-dependent.

### Claim ID: C0001-EXP-04

- **Proposed status:** Qualified, narrow hypothesis.
- **Evidence and source IDs:** `C0001-EXT-01`, `C0001-EXT-06`, `C0001-EXT-09`; `C0001-SRC-01`, `C0001-SRC-07`.
- **Reasoning:** Partitioning can help under severe masking or substitution, consistent with reduced contamination or improved filtering. Fresh context alone is not isolated, and clean-context results generally do not favor multi-agent execution.
- **Scope:** Degraded-context conditions where prior context is misleading or poorly utilized.
- **Limitations:** The effect may instead come from decomposition, prompt changes, message passing, or aggregation.

### Claim ID: C0001-EXP-05

- **Proposed status:** Qualified as a supported risk, not a universal outcome.
- **Evidence and source IDs:** `C0001-EXT-09`; `C0001-SRC-02`, `C0001-SRC-07`; `C0001-INT-07`.
- **Reasoning:** Context loss, information withholding, and error propagation are observed failure modes, and sequential tasks can degrade sharply under coordination. This supports interface loss as a credible cost of narrow handoffs.
- **Scope:** Workflows with incomplete state, compressed handoffs, sequential dependencies, or weak validation.
- **Limitations:** Observational trace evidence does not quantify the independent causal effect of fresh contexts.

### Claim ID: C0001-EXP-06

- **Proposed status:** Accepted as a derived, task-conditional conclusion.
- **Evidence and source IDs:** `C0001-EXT-01`, `C0001-EXT-02`, `C0001-EXT-06`, `C0001-EXT-09`; `C0001-SRC-01`, `C0001-SRC-02`, `C0001-SRC-07`.
- **Reasoning:** Architecture rankings differ across clean versus corrupted context, decomposable versus sequential tasks, and centralized versus independent coordination. The evidence supports heterogeneity rather than a uniform effect.
- **Scope:** Benchmarked reasoning and agentic tool tasks represented in the cited studies.
- **Limitations:** Direct evidence on open-ended multi-source research synthesis is sparse; failure-mode categories are not yet operationalized for this branch.

### Claim ID: C0001-EXP-07

- **Proposed status:** Qualified hypothesis; generic replacement claim unresolved.
- **Evidence and source IDs:** `C0001-EXT-03`, `C0001-EXT-10`; `C0001-SRC-10`; Critic Minor Problem 2.
- **Reasoning:** A trained mistake locator can outperform prompted large-model localization, supporting replacement of a specific weak function by a specialized checker. There is no evidence that deterministic ledgers, rubrics, or checks can replace entire evidence or critic roles in this research loop.
- **Scope:** Specific, operationalized verification functions.
- **Limitations:** The strongest supporting example uses a trained classifier and privileged error-location framing, not a zero-cost deterministic rule.

### Claim ID: C0001-INTG-01

- **Proposed status:** Accept as the main derived conclusion.
- **Evidence and source IDs:** `C0001-EXT-01`, `C0001-EXT-02`, `C0001-EXT-06` through `C0001-EXT-10`; `C0001-SRC-01` through `C0001-SRC-07`, `C0001-SRC-10` through `C0001-SRC-13`; `C0001-INT-01` through `C0001-INT-07`.
- **Reasoning:** Current evidence supports conditional architecture fit and component mechanisms, not a general independent fresh-role advantage.
- **Scope:** Current external record and branch design as of C0001.
- **Limitations:** This is a synthesis of heterogeneous studies, not the result of the branch’s own controlled experiment.

### Claim ID: C0001-INTG-02

- **Proposed status:** Accept as an evidence-gap conclusion.
- **Evidence and source IDs:** External Evidence Researcher, Research Scope, Fixed-Compute Versus Added-Compute Evidence, and Evidence Gaps 1–5 and 10; `C0001-EXT-06`, `C0001-EXT-07`; `C0001-SRC-01`, `C0001-SRC-02`, `C0001-SRC-03`; `C0001-INT-11`.
- **Reasoning:** The literature reviewed does not fully isolate role separation from added or differently allocated compute. Reasoning-token caps or mean budgets leave unbalanced prompt, context, orchestration, state, tool, sample, and selector costs.
- **Scope:** The sixteen-source external ledger assembled in C0001.
- **Limitations:** This is an absence-of-clean-evidence finding, not proof that no such study exists outside the completed search.

### Claim ID: C0001-INTG-03

- **Proposed status:** Accept as a methodological requirement.
- **Evidence and source IDs:** Critic Fatal Problem 2 and Required Corrections 4–6; `C0001-EXT-05` discussion of metrics; `C0001-SRC-14`, `C0001-SRC-15`, `C0001-SRC-16`.
- **Reasoning:** Unsupported-claim evaluation must segment atomic claims, verify support correctness, normalize or pair precision with coverage and task completion, and track error lineage. Citation presence alone is inadequate.
- **Scope:** Future branch experiments and state claims about unsupported claims or cumulative errors.
- **Limitations:** The exact coding protocol, adjudication procedure, and reliability standard remain to be defined.

## Accepted New Facts

The Archivist should add the following to the accepted factual record, preserving source type and limitations:

1. **No exact target-factor study was located in C0001.** No source in the C0001 ledger holds stage prompts, role instructions, artifacts, information, tools, evaluator, sampling opportunities, and full inference cost constant while varying only fresh invocation boundaries.

2. **Near-direct matched-budget evidence is neutral or negative overall.** `C0001-SRC-01` reports single-agent systems best or tied in most clean multi-hop settings under requested thinking-token caps, with a partitioned-system crossover only under some severe context corruption. Full inference cost and information flow were not equalized.

3. **Architecture effects are task-conditional.** `C0001-SRC-02` reports gains on decomposable financial-analysis and dynamic navigation tasks but substantial degradation on sequential planning under a shared reasoning-token budget.

4. **Simpler budget-aware baselines can explain debate gains.** `C0001-SRC-03` reports self-consistency matching or beating debate and Reflexion at comparable resource levels; `C0001-SRC-04` reports untuned debate as unreliable and generally costlier.

5. **Structured verification does not require multiple nominal agents.** `C0001-SRC-11` reports factuality gains from one-model staged verification, with added inference and no equal-budget fresh-context test.

6. **Verifier information is a material component.** `C0001-SRC-10` reports weak error localization by prompted models and stronger correction once an error location is supplied.

7. **External workflow memory can improve long-horizon performance.** `C0001-SRC-12` reports navigation gains from reusable workflow records, while adding information and memory-processing costs.

8. **Homogeneous same-model agents can become redundant.** `C0001-SRC-06` reports increasing output similarity and diminishing returns as homogeneous agent count rises; this does not establish factual independence or apply directly to the target research loop.

9. **Multi-agent interfaces introduce documented failure modes.** `C0001-SRC-07` identifies context loss, information withholding, repetition, misalignment, and verification or termination failures in analyzed traces.

10. **Available metrics cover only parts of the target outcome.** `C0001-SRC-14` supports atomic fact segmentation and support precision; `C0001-SRC-15` separates citation correctness and completeness; `C0001-SRC-16` adds a coverage-sensitive proxy. None traces stage-level error lineage.

## Qualified or Narrowed Claims

- Replace “role separation reduces cumulative error” with: **fresh role separation may help in specific task and context regimes, but its independent effect is unestablished and may be negative when coordination or handoff costs dominate** (`C0001-INTG-01`).
- Replace “externalized memory and provenance matter more than agent count” with: **external memory is an empirically supported active component in some long-horizon tasks; explicit provenance is a useful measurement and control structure, but comparative dominance over invocation structure is unresolved** (`C0001-EXP-02`).
- Replace “adversarial passes matter more than agent identity” with: **structured verification can improve some outcomes without multiple agent identities, and verifier information may matter more than a generic critic label; equal-compute comparative superiority is unresolved** (`C0001-EXP-03`).
- Preserve context partitioning as a two-sided hypothesis: it may reduce contamination under degraded context, and it may cause dependency loss when state or handoffs are incomplete (`C0001-EXP-04`, `C0001-EXP-05`).
- Accept task and failure-mode heterogeneity as the current evidence-backed direction, with limited transfer to open-ended research synthesis (`C0001-EXP-06`).

## Rejected or Unsupported Claims

- Reject any general statement that multi-agent or seven-role execution is superior to single-agent prompting under fixed compute.
- Reject treating the Explorer’s four-condition ladder as a causal isolation design; the staged-versus-role-separated contrast changes multiple factors simultaneously (Critic Fatal Problem 1).
- Reject counting agreement among fresh same-model roles as independent corroboration (`C0001-INT-05`, `C0001-EXT-05`).
- Reject using positive added-compute debate, self-refinement, verification, self-consistency, or memory studies as direct evidence for an independent role-separation effect.
- Reject raw unsupported-claim counts, citation presence, or provenance-link counts as sufficient outcome measures without support correctness, coverage, task completion, and claim segmentation.
- Reject interpreting a role-deletion loss as unique role value unless the treatment of freed compute is declared.
- Reject the broad speculation that deterministic structure can replace whole roles; retain only function-specific replacement hypotheses.

## Contradictions and Tensions

1. **Positive debate versus budget-aware neutral or negative findings:** `C0001-SRC-05` reports gains with additional agents and rounds, while `C0001-SRC-01`, `C0001-SRC-03`, and `C0001-SRC-04` show ties, losses, or simpler-baseline competitiveness under tighter budget accounting. Added inference, protocol tuning, model, and task differences explain part but not all of the discrepancy.

2. **Self-refinement gains versus weak intrinsic self-correction:** `C0001-SRC-08` reports broad gains, while `C0001-SRC-09` reports that intrinsic self-correction can fail or degrade correct answers. `C0001-SRC-10` suggests the key distinction is error-location or verifier information, not the mere presence of a revision stage.

3. **Context partitioning as protection versus interface loss:** `C0001-SRC-01` reports benefits under some severe context corruption, while `C0001-SRC-02` and `C0001-SRC-07` document sequential degradation, context loss, and information withholding. State completeness and task structure may determine the sign.

4. **Diversity as value versus capability saturation:** `C0001-SRC-06` reports benefits from heterogeneous models, prompts, or tools, but `C0001-SRC-02` does not find heterogeneous teams universally overcoming the limits of the strongest available model. Surface or semantic diversity must not be equated with correct complementarity.

5. **Provenance traceability versus epistemic support:** `C0001-SRC-14` through `C0001-SRC-16` show that atomic support precision, citation correctness, citation completeness, and coverage are distinct. A workflow can improve traceability formatting without improving support quality or completeness.

6. **Current-state timing:** `current_state.md` says Cycle 1 has not started, while control and cycle artifacts show C0001 is in progress (`C0001-INT-03`, Prior Contradictions or Objections). The Archivist should correct this stale status when updating accepted state.

## Remaining Hypotheses

1. **Conditional architecture fit:** decomposable tasks with centralized validation may benefit; sequential tasks or high-overhead workflows may not.
2. **Functional scaffolding hypothesis:** staged operations, structured state, provenance, and verifier information account for most useful effects, with little independent contribution from fresh invocation boundaries.
3. **Budget-allocation hypothesis:** sampling, selection, actual compute consumption, and prompt tuning explain a large share of reported multi-agent gains.
4. **Minimal null:** after full controls, fresh role separation has no stable average effect, but interacts with task and context conditions.
5. **Fresh-context contamination-control hypothesis:** fresh execution helps mainly when prior context is misleading and state is complete.
6. **Fresh-context-plus-memory interaction:** context isolation is beneficial only when external state preserves all dependencies required for correction and integration.
7. **Verifier-quality hypothesis:** independent, privileged, deterministic, trained, heterogeneous-model, or human verification signals outperform a generic same-model critic at comparable cost.
8. **Diversity-quality hypothesis:** role prompts help only when they produce nonredundant supported facts or independent correct detections, not stylistic variation.
9. **Interface-loss hypothesis:** handoff compression and permission partitioning introduce omissions, contradictions, duplication, and error mutation that can offset specialization benefits.

## Unresolved Questions

- What is the branch’s primary definition of fixed inference compute: total input-plus-output tokens, model-priced cost, calls, or another unit? Which secondary resource measures must always be recorded?
- Can persistent and fresh staged workflows be made informationally equivalent, including identical intermediate messages, evidence, verifier inputs, and final integration access?
- What exact feature is meant by “role separation”: objective labels, invocation boundaries, context reset, permissions, handoff files, or a declared combination?
- How should atomic claims be segmented, and how should support, interpretation, omission, hedging, and claim importance be adjudicated?
- How will cumulative errors be linked across stages as introduced, preserved, corrected, mutated, or amplified?
- How should factual coverage, task completion, usefulness, and response length be combined with unsupported-claim precision?
- Which evaluator design reduces shared-model bias and provides inter-rater reliability?
- Does fresh execution add value after equalizing stage prompts, state, evidence, samples, selectors, and full compute?
- Does structured state dominate fresh context, or is there a fresh-context-by-state-completeness interaction?
- Which roles add unique function after running both budget-removed and budget-reallocated ablations?
- Do findings from short-answer reasoning and tool benchmarks transfer to multi-source open-ended research synthesis?

## Proposed Updated Branch State

# Branch B001 — Proposed Current Accepted State after C0001

## Research objective

Under a fixed inference-compute budget, which design features of a role-separated multi-agent research loop most reduce unsupported claims and cumulative reasoning errors compared with repeated single-agent prompting?

## Accepted factual record

- The branch protocol combines ordered functional roles, fresh conversations, role-specific permissions, externalized control and accepted state, epistemic labels, exact-reference requirements, and controlled handoffs. These are separate candidate factors rather than one indivisible “multi-agent” treatment (`C0001-INT-01` through `C0001-INT-07`).
- No source located in C0001 isolates fresh invocation boundaries while keeping stage prompts, role instructions, artifacts, information, tools, evaluator, sampling opportunities, and full inference cost constant.
- The closest matched reasoning-token comparison reports single-agent systems best or tied in most clean multi-hop settings, with partitioned execution helping under some severe masking or substitution corruption; full costs and information flow were not equalized (`C0001-SRC-01`).
- A controlled architecture benchmark reports positive coordination effects on decomposable financial-analysis and dynamic-navigation tasks and large negative effects on sequential planning under a shared reasoning-token budget (`C0001-SRC-02`).
- Budget-aware evidence reports self-consistency matching or beating debate and Reflexion at comparable resource levels; untuned debate is unreliable and generally costlier (`C0001-SRC-03`, `C0001-SRC-04`).
- Structured one-model verification can improve factuality with added inference, so multiple nominal agents are not necessary for that mechanism (`C0001-SRC-11`).
- Verifier information is material: models may correct identified errors more reliably than they locate them, and a specialized locator can outperform prompted large-model localization (`C0001-SRC-10`).
- Reusable external workflow memory can improve long-horizon navigation, while adding information and memory-processing cost (`C0001-SRC-12`).
- Homogeneous same-model vote and debate outputs can become increasingly redundant; prompt, model, or tool heterogeneity can preserve diversity, but diversity is not equivalent to independent correctness (`C0001-SRC-06`).
- Multi-agent traces exhibit context loss, information withholding, repetition, misalignment, and verification or termination failures (`C0001-SRC-07`).
- FActScore, ALCE, and SAFE provide partial measurement tools for atomic support, citation correctness and completeness, and coverage sensitivity, but not complete stage-level error lineage (`C0001-SRC-14` through `C0001-SRC-16`).

## Current claims

- **C0001-INTG-01 — Conditional architecture fit:** Current evidence does not support a general independent benefit from fresh role separation. Workflow effects vary with task decomposability, context condition, verification topology, state completeness, and coordination overhead. Status: accepted derived conclusion, limited to the current heterogeneous evidence base.
- **C0001-INTG-02 — Compute isolation gap:** The C0001 evidence does not fully isolate role separation from added or differently allocated compute. Status: accepted evidence-gap conclusion.
- **C0001-INTG-03 — Measurement requirement:** Unsupported-claim and cumulative-error evaluation must combine atomic claim segmentation, support correctness, citation correctness and completeness, factual coverage, task completion, and stage-level error lineage. Status: accepted methodological requirement; exact coding protocol unresolved.
- **C0001-EXP-06 — Heterogeneous effects:** Architecture benefits and harms vary by task and failure mode. Status: accepted as a task-conditional derived conclusion, with sparse evidence for open-ended research synthesis.

## Current qualified hypotheses

- Fresh role separation may help when tasks decompose into parallel evidence streams, prior context is degraded, or centralized verification provides a reliable validation bottleneck.
- Fresh role separation may harm sequential or tool-heavy tasks when coordination consumes fixed budget or handoffs omit dependencies.
- Structured stages, external memory, and verifier information may account for most useful effects, but their comparative dominance over fresh invocation boundaries is unresolved.
- Fresh context may reduce contamination only when external state is complete enough to prevent interface loss.
- Sampling, selection, and budget allocation may explain much of the apparent multi-agent advantage.
- Specialized verification functions may be replaceable by trained or deterministic checks, but replacement of entire roles is unsupported.

## Rejected interpretations

- General superiority of multi-agent or seven-role workflows under fixed compute.
- Same-model role agreement as independent validation.
- Positive added-compute debate, refinement, verification, or memory results as direct proof of role separation.
- Citation presence or raw unsupported-claim counts as sufficient epistemic evaluation.
- Role-deletion loss as proof of unique role value without an explicit freed-compute rule.

## Known objections and risks

- Same-model agents can produce correlated or redundant judgments.
- Added roles can consume budget, duplicate work, propagate errors, and introduce context or handoff loss.
- Apparent gains can come from added sampling, revision, retrieval, verifier information, external memory, prompt tuning, or selector quality.
- Fixed token caps can hide unequal prompt, context, orchestration, tool, state, final-answer, and sample costs.
- A workflow can lower unsupported-claim counts by making fewer claims or reducing task coverage.
- Same-model or LLM-as-judge evaluation can share tested-system biases.
- Direct evidence on multi-source open-ended research synthesis remains sparse.

## Unresolved questions

- What exact factor and estimand define role separation for the branch?
- What full compute ledger and primary matching rule will be used?
- Can a persistent staged and fresh staged condition receive identical information and intermediate artifacts?
- What claim-segmentation, support-adjudication, coverage, and error-lineage protocol will be accepted?
- How will evaluator independence and reliability be established?
- Does fresh execution retain any effect after equalizing samples, selectors, verifier inputs, state, tools, and cost?
- Which roles provide unique function under both budget-removed and budget-reallocated ablations?
- Which task strata show positive, neutral, or negative effects?

## Current research status

Cycle 1 has completed through integration. The proposed state awaits Cycle Archivist review and formal adoption. No branch-local controlled experiment has yet established an independent role-separation effect.

## Suggested Next Frontier

The highest-value next frontier is a **fresh-boundary isolation design with an accepted measurement and compute protocol**.

The primary contrast should execute identical stage prompts, intermediate artifacts, evidence, tools, verifier inputs, sampling opportunities, and final integration rules in:

1. one persistent staged context; and
2. fresh staged invocations.

Role labels should not be the initial varying factor. Where possible, identical intermediate messages should be replayed so that the declared treatment is invocation/context boundary rather than content. The compute ledger should charge prompt and context processing, completion tokens, state creation, handoff generation, tool operations, independent samples, selector work, and final-answer generation. Outcomes should include atomic support correctness, citation correctness and completeness, factual coverage, task completion, and adjudicated stage-by-stage error lineage.

A second-priority contrast should equalize candidate count and selector quality to test the sampling and budget-allocation explanation. A third should compare generic same-model critique with draft-hidden, deterministic, trained, heterogeneous-model, or human verification signals at matched revision cost. Role ablations should later be run under both budget-removed and budget-reallocated rules.

The next Explorer retains responsibility for selecting the actual cycle frontier.

## Handoff to Cycle Archivist

Adopt the proposed branch state only with the stated qualifications. Do not record a general benefit from role separation. Preserve the negative and neutral matched-budget findings, the absence of an exact target-factor study, the compute-accounting gap, the context-partitioning benefit/cost tension, and the same-model correlation limitation.

Record `C0001-INTG-01`, `C0001-INTG-02`, and `C0001-INTG-03` as the principal integrated conclusions. Retain `C0001-EXP-06` in narrowed form. Keep `C0001-EXP-01` unresolved and weakened; keep `C0001-EXP-02`, `C0001-EXP-03`, `C0001-EXP-04`, `C0001-EXP-05`, and `C0001-EXP-07` as qualified hypotheses or risks within the scopes stated above.

Correct the stale current-state status that says Cycle 1 has not started. The Archivist should construct the official `current_state.md` from the proposed state, then perform its own authorized archive and cycle-control actions. The Integrator does not advance the numeric cycle.