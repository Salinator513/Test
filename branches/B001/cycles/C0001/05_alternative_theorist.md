# Alternative Theorist — C0001

## Strongest Current Interpretation

The strongest current interpretation is **conditional architecture fit**, not a general advantage from role separation.

On the evidence assembled in C0001, fresh role-separated execution is not independently established as the cause of better research accuracy. The closest matched-budget comparison reported by the External Evidence Researcher finds that single-agent systems usually match or outperform multi-agent systems on clean multi-hop reasoning, while partitioned or coordinated systems can help in narrower circumstances: when the task naturally decomposes into parallel evidence streams, when a unified context is materially degraded, or when coordination supplies a reliable validation bottleneck (`C0001-EXT-01`, `C0001-EXT-02`, `C0001-EXT-06`, `C0001-EXT-09`).

The strongest defensible mechanism is therefore a combination of **task decomposition, controlled information flow, and verification quality**. Role-separated fresh conversations may implement those mechanisms, but the current evidence does not show that invocation separation itself adds value after stage prompts, information access, artifacts, tools, sampling opportunities, and total inference cost are held constant. This interpretation also accommodates the negative evidence: coordination overhead, context loss, redundant same-model outputs, and weak self-critique can erase or reverse any gains (`C0001-EXT-07` through `C0001-EXT-10`).

This interpretation remains provisional. No located study tests the exact target contrast, and the branch has no accepted operational definition or branch-local experiment for unsupported claims, factual coverage, or cumulative error lineage (`C0001-INT-08`, `C0001-INT-11`; External Evidence Researcher, Evidence Gaps).

## Alternative Theory 1

### Core claim

**Functional scaffolding, externalized memory, and verifier information account for most apparent benefits; fresh role separation has little or no independent effect.**

Evidence status: **evidence-backed as a serious alternative**, but not directly proven against an informationally identical fresh-context condition.

### Mechanism

A research workflow improves when it forces distinct operations—generation, challenge, evidence checking, and revision—and stores claims, provenance, and accepted state outside the transient conversation. These structures reduce simultaneous-objective pressure, make unsupported claim promotion visible, and permit verification to be performed without conditioning every judgment on the original draft.

Under this theory, the causal components are:

- mandatory staged operations rather than nominal agent identity;
- explicit claim and provenance records rather than conversational memory;
- independent or privileged verification information rather than a generic same-model critic;
- deterministic or trained checks for functions the language model performs poorly, such as locating errors.

Fresh invocations matter only insofar as they help implement partial information independence. A single model using the same stages, artifacts, and deliberately separated verification inputs could obtain the same benefit.

### Evidence it explains

- Chain-of-Verification improves factuality using one model with separated draft, verification-question, independent-answer, and revision stages, showing that multiple agent identities are unnecessary for the relevant verification structure (`C0001-EXT-03`; `C0001-SRC-11`).
- Self-Refine reports gains from a single model performing generator, feedback, and refiner functions, although it adds inference and does not prove equal-budget superiority (`C0001-EXT-05` discussion of structured stages; `C0001-SRC-08`).
- Tyen et al. separate mistake finding from correction and report that a specialized locator can outperform prompted large-model error localization. This supports verifier-signal quality rather than role count (`C0001-EXT-03`, `C0001-EXT-10`; `C0001-SRC-10`).
- Agent Workflow Memory provides evidence that reusable external records can improve long-horizon performance, making externalized memory a plausible active ingredient (`C0001-EXT-04`; `C0001-SRC-12`).
- The branch protocol itself bundles fresh conversations with structured state, epistemic labels, exact-reference rules, allowlists, and stage gates (`C0001-INT-01` through `C0001-INT-07`). This explains why any branch-level improvement could be wrongly attributed to roles alone.
- Weak and sometimes harmful same-model self-correction is expected when the verifier receives no better information than the generator (`C0001-EXT-10`).

### Evidence it struggles with

- It does not by itself explain the reported crossover where sequential partitioning helps under severe context masking or substitution unless context isolation has an additional independent effect (`C0001-EXT-01`).
- It may understate the value of genuinely parallel evidence gathering on decomposable tasks, where multiple workers can cover distinct evidence streams within a shared budget (`C0001-EXT-02`).
- Existing memory studies add workflow information, induction, retrieval, or prompt context. They do not show that a fixed, equal-quality state supplied to both workflows eliminates a fresh-role advantage.
- Single-model staging can still inherit correlated misconceptions and may fail when the same model must both generate and judge without external signals.

### Predictions

1. When a persistent single-context workflow and a fresh-invocation workflow receive identical stage prompts, intermediate artifacts, evidence, verifier inputs, and total charged compute, their unsupported-claim and error-lineage results will be similar.
2. Removing claim/provenance structure or degrading verifier information will reduce performance more than replacing fresh roles with a persistent staged process.
3. A deterministic or independently trained verifier will outperform an additional generic same-model critic at the same cost on error-localization outcomes.
4. Benefits will track support correctness, verification quality, and state completeness more strongly than the number of role labels or invocation boundaries.
5. A fresh-role workflow with poor handoffs will perform worse than a persistent staged workflow with complete external state.

## Alternative Theory 2

### Core claim

**Apparent multi-agent gains are mainly budget-allocation and selection effects: more samples, more attempts, more rounds, prompt tuning, and favorable reporting—not role separation—produce the observed improvements.**

Evidence status: **strongly evidence-backed as a confound and partial explanation**. Reporting bias is plausible but remains more speculative because the assembled evidence does not directly measure publication or reporting processes.

### Mechanism

Many systems labeled “multi-agent” receive additional opportunities to generate a correct path, criticize an answer, revise it, vote among candidates, or select a favorable completion. Even under nominal token caps, architectures may differ in actual token use, independent sample count, prompt overhead, context processing, planner and aggregator cost, or tool calls.

The performance gain may therefore come from one or more of the following:

- independent sampling increases the chance that at least one path is correct;
- voting or selection chooses among multiple candidates;
- repeated revision adds inference relative to a one-pass baseline;
- hyperparameter and prompt tuning favors the reported architecture;
- successful tasks or metrics are emphasized while null or negative conditions receive less attention;
- systems that generate fewer claims appear safer under unsupported-claim metrics without improving coverage.

Role labels then act as a convenient packaging for extra inference and selection rather than as the active ingredient.

### Evidence it explains

- The budget-aware comparison reports that self-consistency matches or beats multi-agent debate and Reflexion at comparable query, token, and monetary budgets, while debate diversity declines across rounds (`C0001-EXT-07`; `C0001-SRC-03`).
- Self-consistency obtains gains through independent sampled reasoning paths without role specialization, handoffs, or fresh epistemic identities (`C0001-EXT-07`, Evidence About Alternative Explanations; `C0001-SRC-13`).
- Positive debate results add agents, rounds, calls, and tokens, so they cannot isolate role separation (`C0001-EXT-03`; `C0001-SRC-05`).
- Untuned debate does not reliably beat simpler baselines and is sensitive to protocol and hyperparameter choices (`C0001-EXT-08`; `C0001-SRC-04`).
- The closest matched-budget comparison usually favors or ties the single-agent condition and notes actual-use and overhead-accounting limitations (`C0001-EXT-06`; `C0001-SRC-01`).
- The Critic and Internal Evidence Researcher identify hidden differences in calls, samples, prompt overhead, state maintenance, and compute reallocation as fatal confounds in the proposed ladder (`02_critic.md`, Fatal Problem 1 and Material Problems 3 and 5; `C0001-INT-11`).
- FActScore, SAFE, and ALCE demonstrate that favorable factuality or citation numbers can reflect metric construction, claim count, or citation presence rather than complete and correctly supported answers (`C0001-EXT-05` discussion of measurement; `C0001-SRC-14` through `C0001-SRC-16`).

### Evidence it struggles with

- It does not fully explain matched-budget benefits on decomposable financial-analysis tasks or context-corruption crossovers unless budget is being allocated more effectively because of task structure (`C0001-EXT-01`, `C0001-EXT-02`).
- A pure sampling account cannot explain why centralized coordination outperforms independent coordination in some settings; topology and validation bottlenecks appear relevant.
- It does not explain improvements from external memory when the key benefit is reusable information rather than repeated sampling.
- Reporting bias is not directly established by the current source set. It should be treated as a risk requiring preregistration and full condition reporting, not as a factual explanation of any particular paper.

### Predictions

1. At equal total input-plus-output tokens, equal tool calls, equal number of sampled candidates, and equal selection opportunities, much of the apparent multi-agent advantage will disappear.
2. Reallocating a removed role’s compute to independent samples or a stronger verifier will match or exceed keeping the role.
3. Performance will correlate more strongly with candidate count, actual consumed compute, and selector quality than with role count.
4. Multi-agent advantages will shrink when all prompts, hyperparameters, seeds, task subsets, and negative results are preregistered and fully reported.
5. Unsupported-claim improvements will shrink when normalized for factual coverage, claim importance, task completion, and response length.

## Additional Alternative or Null Explanation

### Minimal null: no stable general role-separation effect

**Core claim:** Once compute, information, staging, and evaluation are controlled, fresh role separation has no stable average effect. Positive and negative results arise from task-architecture interactions, coordination overhead, and measurement noise.

Evidence status: **supported as a viable null, not established as the final theory**.

This null explains why the closest matched-budget study finds single-agent systems best or statistically indistinguishable from the best multi-agent system in most tested regimes (`C0001-EXT-06`), why coordination helps decomposable tasks but sharply harms sequential planning (`C0001-EXT-02`, `C0001-EXT-09`), and why homogeneous agents become redundant (`C0001-EXT-05`). It also fits the absence of any exact fresh-context-only experiment.

The null struggles with repeated evidence that certain structures—independent verification, centralized validation, external memory, and context partitioning under degradation—can improve outcomes. The correct minimal form is therefore not “workflow structure never matters.” It is “fresh role separation has no general independent effect; only specific mechanisms and task matches matter.”

Predictions:

- Average effects across mixed task families will be near zero or unstable, masking positive effects on decomposable or degraded-context tasks and negative effects on sequential tasks.
- Role labels without changes to information, verification, or context will not improve results.
- Architecture rankings will reverse across task types and budget levels.
- Increased role count among homogeneous same-model agents will show diminishing or negative returns.

### Speculative selection-and-evaluator explanation

A more speculative possibility is that some reported gains reflect evaluator alignment with verbose, well-structured, citation-rich outputs or selection of task subsets where the workflow’s style is rewarded. This is consistent with the branch’s evaluator-bias and metric concerns but is not directly demonstrated for the cited studies. It should be tested through blinded human adjudication, multiple independent evaluators, and coverage-sensitive scoring rather than assumed.

## Hybrid Explanations

The evidence permits multiple mechanisms to operate simultaneously. The following hybrids are more credible than a single universal mechanism:

1. **Decomposition plus centralized verification.** Parallel workers broaden evidence collection, while a central verifier prevents independent errors from propagating. This fits positive decomposable-task results and negative independent-agent results (`C0001-EXT-02`, `C0001-EXT-09`).

2. **Fresh context plus external memory.** Fresh contexts may reduce anchoring or draft-conditioned verification, but only when a complete structured state preserves dependencies. Without that memory, context isolation becomes context loss (`C0001-EXT-01`; `C0001-INT-03`, `C0001-INT-07`; `C0001-EXT-09`).

3. **Sampling plus verification.** Multiple candidates create breadth, but gains depend on a selector or verifier that can recognize the correct path. Weak same-model judging can nullify the sampling advantage (`C0001-EXT-07`, `C0001-EXT-10`).

4. **Role prompts as diversity induction.** Role instructions may help when they generate complementary, correct-path evidence, but not when they merely create stylistic variation or correlated wrong answers (`C0001-EXT-05`).

5. **Task fit plus budget allocation.** Coordination may be worthwhile on decomposable research tasks because it assigns compute to parallel evidence streams, while the same overhead is wasteful on sequential reasoning. The active effect is the interaction between architecture and task structure, not a universal role benefit (`C0001-EXT-02`, `C0001-EXT-09`).

## False Dichotomies or Framing Problems

- **“Single agent” versus “multi-agent” is not the causal contrast.** Both can use the same model repeatedly. Relevant factors include invocation boundaries, objective specialization, stage order, state, permissions, sampling, and handoff compression.
- **Role separation versus staging is a false choice.** Roles are one implementation of staged functions. A persistent process can perform the same functions, and fresh invocations can be used without meaningful specialization.
- **Memory versus roles is not either-or.** Fresh-role systems may require external memory to avoid interface loss; memory can also allow a persistent staged system to match them.
- **Independent versus correlated agents is too binary.** Same-model agents can be partially diversified by prompts, tools, or information, yet remain correlated on shared misconceptions. Diversity must be measured for correctness and complementarity, not merely surface difference.
- **More compute versus better architecture is not always separable by one token cap.** The allocation of compute across samples, verification, context processing, orchestration, and tool use can matter as much as the total.
- **Accuracy versus unsupported claims is incomplete.** A system can reduce unsupported claims by saying less. Precision, coverage, citation support, task completion, and error lineage must be measured together.
- **Role contribution versus role necessity is a false equivalence.** Removing a role while discarding its budget tests role-plus-compute contribution; reallocating its budget tests replaceability.
- **Positive average effect versus no value is a false choice.** A workflow can have no general average advantage while delivering large benefits for a narrow failure mode or task structure.

## Discriminating Tests

1. **Fresh-boundary isolation test.** Use identical model, stage prompts, evidence, intermediate artifacts, state, tools, verifier, and final integration procedure. Run one condition in a persistent context and the other across fresh invocations. Replay identical intermediate messages where possible. Charge all prompt, context, completion, handoff, state-maintenance, tool, and final-answer costs. This is the primary test of an independent fresh-role effect.

2. **Stage-versus-identity test.** Compare: one persistent general prompt; one persistent staged workflow; fresh staged invocations without role-specific identities; and fresh role-labeled invocations. Equalize information and compute. A staged gain without an additional role-label gain supports Alternative Theory 1.

3. **Sampling-equated test.** Give every condition the same number of independently generated candidates and the same selector. Then vary role structure. If differences vanish, Alternative Theory 2 gains support.

4. **Verifier-information test.** Compare a generic same-model critic, an independently prompted critic with draft-hidden evidence, a deterministic checker, a trained error locator, and an oracle or human verifier where available. Hold revision compute constant. This distinguishes role separation from verifier quality.

5. **External-memory factorial.** Cross structured state present/absent with persistent/fresh execution. Keep state content fixed and charge its creation cost. If state dominates and the interaction is small, Alternative Theory 1 is favored. A large fresh-by-state interaction would support the fresh-context-plus-memory hybrid.

6. **Handoff-compression test.** Supply full prior artifacts, lossless structured artifacts, and compressed summaries while holding invocation boundaries constant. Measure omitted dependencies, contradictions, duplicated work, and error mutation. This isolates interface loss from fresh context.

7. **Task-structure stratification.** Preclassify tasks as parallel-decomposable, sequential, context-degraded, tool-heavy, or synthesis-heavy. Test architecture effects within each stratum rather than only averaging. Conditional reversals support the task-fit interpretation or null.

8. **Two-rule role ablation.** For every role, run both: deletion with freed compute unused, and deletion with freed compute reallocated to sampling, verification, or integration. The difference separates contribution from replaceability.

9. **Coverage-sensitive epistemic evaluation.** Segment atomic claims; adjudicate whether cited evidence actually supports each claim; separately score citation correctness and completeness; include factual coverage, task completion, and usefulness; and trace each error’s introduction, preservation, correction, mutation, or amplification across stages.

10. **Evaluator-robustness test.** Use blinded human adjudication or multiple evaluator families, report inter-rater reliability, and prevent the tested system from judging its own outputs as the sole authority. Architecture effects that disappear under evaluator changes suggest selection or scoring artifacts.

11. **Preregistered prompt-and-budget replication.** Fix prompts, task subsets, seeds, stopping rules, and all compute accounting before running conditions. Report every condition, including null and negative results. This directly tests the speculative selection/reporting component of Alternative Theory 2.

12. **Diversity-quality test.** Measure not only semantic diversity but whether agents contribute nonredundant supported facts or independent correct error detections. Role prompts that increase surface diversity without supported complementarity should not count as successful separation.

## Comparative Evidence Table

| Theory | Evidence it explains well | Evidence it explains poorly | Distinguishing prediction | Current status |
|---|---|---|---|---|
| Conditional architecture fit | Positive effects on decomposable tasks, degraded context, and centralized validation; negative effects on sequential tasks and independent coordination | Does not isolate whether fresh invocation itself matters | Effects reverse by task structure and validation topology | Strongest current interpretation; conditional, not final |
| Functional scaffolding, memory, and verifier information | Single-model staged verification, external-memory gains, deterministic locator value, weak generic self-critique | Context-corruption crossover and parallel breadth may require additional mechanisms | Persistent staged execution matches fresh roles when artifacts and verifier information are equal | Evidence-backed alternative; direct target test absent |
| Budget allocation, sampling, and selection | Self-consistency competitiveness, added-compute debate gains, protocol sensitivity, metric/coverage confounds | Centralized coordination effects and external-memory benefits are not pure sampling | Equal samples, selectors, and full compute accounting remove most role advantage | Strong confound and partial explanation; reporting component speculative |
| Minimal null: no stable general role effect | Matched-budget single-agent ties/wins, task-dependent reversals, redundant homogeneous agents | Reliable gains from specific verification, memory, or decomposition mechanisms | Near-zero unstable average with positive and negative task-specific interactions | Viable null; not established |
| Fresh-context contamination control | Benefit under masking/substitution; independent verification design | Clean-context results, handoff loss, and lack of direct ablation | Fresh execution helps mainly when prior context is misleading and state is complete | Plausible but weakly isolated |
| Hybrid decomposition plus centralized verification | Parallel breadth with reduced error amplification | May add unnecessary overhead on sequential tasks | Benefit appears only when subtasks are separable and verifier quality is high | Evidence-backed interaction hypothesis |

## Remaining Uncertainty

- No study isolates fresh invocation boundaries while keeping message content, artifacts, prompts, tools, verifier, and full inference cost identical.
- “Fixed compute” remains underdefined. Requested reasoning-token caps, actual consumed tokens, total input-plus-output tokens, calls, tool operations, state construction, and orchestration can produce different rankings.
- Existing evidence is concentrated in reasoning benchmarks, static question answering, and tool execution; direct evidence on multi-source open-ended research synthesis is sparse.
- The branch has no accepted outcome definitions for unsupported claims, factual coverage, citation support, or cumulative error lineage.
- Same-model output correlation is documented in adjacent vote and debate settings, but not in the exact persistent-staged versus fresh-staged contrast.
- External-memory evidence changes information availability and workflow cost, so it does not establish whether memory merely complements or fully replaces role separation.
- Context partitioning may prevent contamination or hide dependencies. The sign of the effect probably depends on state completeness and task structure.
- Verifier quality may be the dominant moderator, but the relative value of human, deterministic, trained, heterogeneous-model, and same-model verification has not been tested within the proposed branch design.
- The reporting-bias component remains speculative until preregistered replications or complete condition records are compared.
- No available theory yet explains all positive and negative findings without invoking interactions among task structure, information flow, verification, and budget allocation.

## Handoff to Integrator

Do not integrate C0001 as evidence that role separation generally reduces unsupported claims. The most defensible synthesis is that fresh role separation is an unisolated implementation choice inside a bundle of staged functions, external memory, context partitioning, permissions, verification, and budget allocation.

The Integrator should preserve at least three live explanations:

1. conditional architecture fit, especially decomposition plus centralized verification;
2. functional scaffolding, external memory, and verifier information as the main active ingredients;
3. sampling, compute allocation, selection, and metric effects as explanations for apparent gains.

The minimal null—no stable independent role-separation effect after proper controls—must remain viable. The next branch-level empirical priority should be the fresh-boundary isolation test, followed by sampling-equated and verifier-information tests, with two-rule ablations and coverage-sensitive error-lineage evaluation.