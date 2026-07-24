# Explorer — C0001

## Selected Frontier
Design a fixed-compute comparison that isolates the effect of role separation from two closely related features: externalized memory/provenance and repeated self-revision.

## Why This Frontier Now
The branch objective requires comparison under a fixed inference-compute budget, while the accepted state already identifies compute confounding, externalized memory, provenance, and correlated same-model judgments as central unresolved issues. A narrow factorial comparison would make later evidence gathering more useful by clarifying which intervention is being credited for any reduction in unsupported claims or cumulative reasoning errors.

## Relevant Accepted Branch State
- **Accepted sourced facts:** none yet.
- **Accepted claims:** none yet.
- **Current branch hypotheses:** role separation may reduce some cumulative errors by limiting each invocation’s objective and context; externalized memory and explicit provenance may matter more than agent count. Both are unverified.
- **Known objections:** same-model agents may produce correlated judgments; additional roles may add cost and error propagation; apparent gains may be caused by extra compute rather than role separation.
- **Unresolved questions used here:** how to construct a fixed-compute comparison, which failure modes role separation can reduce, and which roles add unique rather than duplicated value.

## Candidate Hypotheses and Possibilities

### C0001-EXP-01 — Role specialization has an independent effect
**Hypothesis, unverified:** At equal total inference compute, assigning distinct objectives to separate invocations reduces unsupported claims and cumulative reasoning errors more than repeated general-purpose prompting with the same memory and provenance tools.

### C0001-EXP-02 — Externalized memory/provenance is the main active ingredient
**Hypothesis, unverified:** Once both conditions use the same structured state, claim labels, and provenance record, a role-separated loop provides little additional benefit over a single-agent iterative process.

### C0001-EXP-03 — Structured adversarial passes matter more than agent identity
**Hypothesis, unverified:** The useful intervention is not “multiple agents” but forcing separate generation, challenge, evidence, and integration passes. A single model prompted sequentially through these functions may perform similarly if context and compute are matched.

### C0001-EXP-04 — Context partitioning reduces contamination
**Hypothesis, unverified:** Fresh invocations with narrow allowlists reduce anchoring on earlier unsupported statements, even when every invocation uses the same underlying model.

### C0001-EXP-05 — Context partitioning can also destroy useful continuity
**Hypothesis, unverified:** Narrow role contexts may omit relevant dependencies, increasing contradictions, duplicated work, or integration errors unless the external state is sufficiently complete.

### C0001-EXP-06 — Benefits vary by failure mode
**Hypothesis, unverified:** Role separation may help most with provenance loss, unchallenged assumptions, and premature convergence, while offering little protection against shared model misconceptions or uniformly weak source interpretation.

### C0001-EXP-07 — Some roles are replaceable by deterministic structure
**Speculation:** Claim ledgers, source tables, contradiction checks, or fixed evaluation rubrics may reproduce part of the value attributed to dedicated evidence or critic roles at lower inference cost.

## Possible Mechanisms or Connections
- **Objective isolation:** a narrow role objective may reduce pressure to generate, defend, verify, and synthesize simultaneously.
- **Context isolation:** fresh contexts may prevent unsupported wording from acquiring false authority through repetition.
- **External memory:** a shared state file may preserve decisions and provenance without requiring every earlier transcript to remain in context.
- **Forced disagreement:** a designated challenge pass may expose assumptions that ordinary continuation would preserve.
- **Stage-gated claims:** requiring evidence before integration may prevent hypotheses from silently becoming accepted claims.
- **Correlated-error limit:** because the underlying model is shared, role separation may diversify prompts and context without creating genuinely independent knowledge.
- **Interface loss:** compression between roles may discard nuance or uncertainty, producing a new class of cumulative error.

## Questions for Internal Evidence Research
1. What exact distinctions in the protocol could serve as experimental factors: separate invocations, role-specific objectives, fresh context, allowlists, structured state, claim labels, provenance requirements, or mandatory role order?
2. Which currently specified artifacts could be used to measure claim promotion, provenance retention, contradiction, duplication, and handoff loss without adding new external facts?
3. Can the present seven-role loop be mapped into a smaller set of functional stages so that unique role value can later be tested by ablation?
4. What information is preserved or lost at each existing handoff, and which losses could plausibly create cumulative reasoning errors?
5. Which control conditions can be described using the same total token or inference-call budget while varying only role separation, memory/provenance, or adversarial structure?
6. What branch-local definitions are needed for “unsupported claim,” “cumulative reasoning error,” “unique role value,” and “fixed compute” before comparison?

## Questions for External Evidence Research
1. What primary studies or benchmark reports directly compare multi-agent or role-specialized prompting with single-agent iterative prompting under genuinely matched inference compute?
2. What evidence isolates gains from role separation versus gains from additional sampling, longer context, self-consistency, critique/revision, retrieval, or external memory?
3. Which empirical evaluations measure unsupported claims, factuality, calibration, provenance retention, contradiction, or error propagation across multi-step reasoning?
4. Are there ablation studies of critic, verifier, debate, planner, researcher, or integrator roles that identify unique contributions?
5. What findings exist on correlated errors among agents using the same base model, and how were independence or diversity measured?
6. What fixed-budget evaluation designs are used in adjacent work on self-refinement, debate, ensembles, or tool-using agents?
7. Which task families show different outcomes—for example, fact retrieval, long-horizon synthesis, mathematical reasoning, coding, or open-ended research—and do the reported mechanisms differ?

## Potential Tests or Comparisons
A useful minimal comparison could hold the task set, model, total inference-token budget, tool access, and final evaluator constant while varying only the workflow:

1. **Repeated single-agent baseline:** general-purpose iterative prompts with no structured external state.
2. **Single-agent plus structured state:** repeated prompts using the same claim labels, provenance fields, and accepted-state file as the role loop.
3. **Single-agent staged workflow:** one model sequentially performs exploration, challenge, evidence handling, and integration under explicit stage prompts.
4. **Role-separated workflow:** fresh invocations perform the same stages with narrow objectives and controlled handoffs.

Possible measurements:
- unsupported factual claims per final answer;
- fraction of claims with traceable provenance;
- errors introduced, preserved, corrected, or amplified across stages;
- contradiction rate between intermediate artifacts and final output;
- uncertainty labels retained or lost;
- duplicate inference effort;
- performance per fixed token, call, or latency budget;
- marginal change when individual roles or artifacts are removed.

A second comparison could vary context exposure within the role-separated workflow: full prior transcript versus shallow summaries versus structured accepted state only. This would help distinguish the benefits of fresh context from the costs of information loss.

## Main Uncertainties
- “Fixed inference compute” may be operationalized by tokens, model calls, wall-clock cost, or another unit; these may not be equivalent.
- Equal token budgets may still conceal differences in prompt overhead, context reuse, tool calls, or sampling opportunities.
- Unsupported-claim counts may not capture subtle reasoning errors, omitted caveats, or low-quality synthesis.
- A single evaluator may share the same model biases as the tested workflows.
- Role separation, context partitioning, adversarial prompting, and external memory are entangled unless explicitly varied.
- Task difficulty and task type may determine whether handoff discipline helps or merely adds overhead.
- The seven-role protocol may be too large for an initial clean comparison; functional grouping or ablation may be necessary.

## Handoff to Critic
Evaluate whether the proposed frontier is narrow enough to produce a discriminating first-cycle result. Focus especially on hidden compute mismatches, whether the four workflow conditions isolate the intended factors, whether the suggested metrics can distinguish unsupported claims from broader reasoning failures, and whether any candidate hypothesis is framed too loosely to be falsifiable. Do not treat any candidate hypothesis or mechanism above as established evidence.