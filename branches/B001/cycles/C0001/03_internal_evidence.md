# Internal Evidence Researcher — C0001

## Current Research Questions

1. Which branch-specified features are distinct experimental factors rather than one bundled “multi-agent” treatment?
2. What branch artifacts can preserve or expose claim promotion, provenance, contradiction, duplication, and handoff loss?
3. What is the smallest contrast that could vary fresh role-separated execution while holding stage functions, instructions, artifacts, information access, tools, and compute accounting constant?
4. Which outcome and budget terms require operational definitions before the comparison can be interpreted?
5. Which parts of the frontier have actual branch support, and which remain hypotheses or repeated speculation?

## Relevant Accepted Internal Evidence

### C0001-INT-01 — Ordered role separation with fresh conversations
- **Status:** Protocol fact; stored design specification, not empirical evidence of effectiveness.
- **Exact file:** `AGENT_PROTOCOL.md`, lines 8–14.
- **Relevance:** The branch explicitly implements seven ordered roles and states that each role is a fresh ChatGPT conversation. This supplies two separable candidate factors: functional role order and fresh invocation boundaries.
- **Limitations:** The protocol does not show that either feature reduces unsupported claims. It also does not isolate fresh conversations from role-specific objectives, permissions, files, or handoffs.

### C0001-INT-02 — Mandatory stage order and controlled progression
- **Status:** Protocol fact; stored workflow constraint.
- **Exact file:** `AGENT_PROTOCOL.md`, lines 10–14 and 47–54; `branches/B001/state/control.json`, lines 3–8.
- **Relevance:** The control sequence enforces a fixed stage order, and only the Cycle Archivist may advance the cycle. This means stage order and stage-gated progression are active components of the branch design and must be held constant or varied explicitly in any comparison.
- **Limitations:** The files contain no evidence that the specific order is optimal or that stage gating independently improves outcomes.

### C0001-INT-03 — Externalized branch memory
- **Status:** Protocol fact; stored design specification.
- **Exact file:** `AGENT_PROTOCOL.md`, lines 34–40; `branches/B001/state/control.json`; `branches/B001/state/current_state.md`.
- **Relevance:** The branch externalizes control state and accepted knowledge into repository files rather than relying on conversational continuity. This is direct internal support that structured external memory is part of the tested loop and therefore a potential confound when comparing it with a less structured baseline.
- **Limitations:** The branch has not measured memory quality, maintenance cost, omission rate, or whether the same state can be supplied equivalently to another condition.

### C0001-INT-04 — Explicit epistemic typing and exact-reference discipline
- **Status:** Protocol fact; stored evidence-handling rule.
- **Exact file:** `AGENT_PROTOCOL.md`, lines 16–26 and 47–51.
- **Relevance:** The protocol requires distinctions among sourced fact, interpretation, derived conclusion, hypothesis, speculation, objection, and unresolved question, and asks roles to refer to prior claims and files exactly. These are concrete structured-state/provenance interventions that can be separated from role count.
- **Limitations:** The protocol gives categories but no scoring rule for whether labels are correct, whether a cited source actually supports a claim, or how label errors are adjudicated.

### C0001-INT-05 — Same-model repetition is not independent evidence
- **Status:** Accepted protocol rule.
- **Exact file:** `AGENT_PROTOCOL.md`, line 26.
- **Relevance:** The branch already forbids treating repetition, confidence, eloquence, or same-model agreement as independent evidence. This directly constrains interpretation of apparent consensus across roles and supports the Critic’s warning against counting repeated conclusions as corroboration.
- **Limitations:** This is a methodological rule, not measured evidence about the degree or structure of correlated errors.

### C0001-INT-06 — Role-specific source and tool permissions
- **Status:** Protocol fact; stored treatment feature.
- **Exact file:** `AGENT_PROTOCOL.md`, lines 28–32 and 34–41.
- **Relevance:** Only the External Evidence Researcher may browse the public web, and every role is restricted to an explicit file allowlist. Tool access and source access therefore differ by role and are part of the workflow treatment unless equalized in a comparison.
- **Limitations:** The branch contains no measurement of how much any observed outcome is caused by permission separation rather than role objectives or fresh context.

### C0001-INT-07 — Context visibility is deliberately partitioned
- **Status:** Protocol fact; stored context-design feature.
- **Exact file:** `AGENT_PROTOCOL.md`, lines 34–45; current prompt allowlist as reflected in the files authorized for C0001.
- **Relevance:** Roles may open only explicitly allowlisted files, and recovery behavior depends on the authorized output and control state. This confirms that context partitioning and controlled handoffs are real branch features, not merely labels.
- **Limitations:** The protocol does not quantify what relevant information is omitted, duplicated, or distorted at handoffs. It also does not establish informational equivalence with a persistent-context condition.

### C0001-INT-08 — No accepted empirical record yet
- **Status:** Accepted branch-state fact.
- **Exact file:** `branches/B001/state/current_state.md`, lines 8–12.
- **Relevance:** The branch explicitly records no accepted external evidence and no accepted claims. Therefore none of the Explorer’s candidate mechanisms or workflow comparisons can be treated as internally established findings.
- **Limitations:** This item establishes absence of accepted support, not evidence against the hypotheses.

### C0001-INT-09 — Correlated same-model judgments are an accepted objection
- **Status:** Known objection; not a sourced fact.
- **Exact file:** `branches/B001/state/current_state.md`, lines 18–20.
- **Relevance:** This objection bears directly on whether multiple fresh roles provide independent checking. It also explains why role agreement cannot be used as a validity metric.
- **Limitations:** No internal data quantify correlation or identify conditions under which prompt and context diversity do or do not reduce it.

### C0001-INT-10 — Added roles may add cost and propagate error
- **Status:** Known objection; not a sourced fact.
- **Exact file:** `branches/B001/state/current_state.md`, lines 18–21.
- **Relevance:** This is directly relevant to the fixed-compute frontier and to the possibility that handoffs introduce interface loss, duplication, or additional failure points.
- **Limitations:** The branch has no measured role-level cost, error lineage, handoff loss, or comparison with a repeated single-agent process.

### C0001-INT-11 — Extra compute is an accepted confound
- **Status:** Known objection; not a sourced fact.
- **Exact file:** `branches/B001/state/current_state.md`, lines 18–21.
- **Relevance:** The branch already recognizes that apparent gains may come from additional compute rather than role separation. This makes matched budget accounting a required design condition, not a new empirical finding.
- **Limitations:** No primary compute unit or accounting method has been accepted. Tokens, calls, context processing, tool use, state maintenance, and sampling opportunities remain unresolved in the current files.

## Relevant Hypotheses and Speculation

- **Unidentified state hypothesis 1:** Role separation may reduce some cumulative errors by limiting each invocation’s objective and context. Exact file: `branches/B001/state/current_state.md`, lines 14–16. This is unverified and is restated more specifically as `C0001-EXP-01`, `C0001-EXP-04`, and `C0001-EXP-06` in `branches/B001/cycles/C0001/01_explorer.md`.
- **Unidentified state hypothesis 2:** Externalized memory and explicit provenance may matter more than agent count. Exact file: `branches/B001/state/current_state.md`, lines 14–16. This is unverified and is restated as `C0001-EXP-02`.
- **C0001-EXP-01:** Distinct objectives in separate invocations have an independent effect at equal compute. Status: hypothesis, unverified. It is not discriminated from staging or context partitioning by the proposed conditions.
- **C0001-EXP-02:** Structured state and provenance are the main active ingredient. Status: hypothesis, unverified. No internal result compares equalized state across workflows.
- **C0001-EXP-03:** Structured adversarial passes matter more than nominal agent identity. Status: hypothesis, unverified. The Critic notes that stage function and invocation structure must be separated.
- **C0001-EXP-04:** Fresh narrow contexts reduce contamination. Status: hypothesis, unverified. No branch-local outcome data establish reduced anchoring or unsupported-claim carryover.
- **C0001-EXP-05:** Narrow contexts can destroy useful continuity. Status: hypothesis, unverified. The protocol’s allowlists make the mechanism possible, but no loss has been measured.
- **C0001-EXP-06:** Effects differ by failure mode. Status: hypothesis, unverified. The branch has not operationalized or counted the named failure modes.
- **C0001-EXP-07:** Deterministic ledgers, tables, checks, or rubrics may replace some dedicated roles. Status: speculation. No deterministic replacement is specified or tested.

## Prior Contradictions or Objections

1. **Current-state timing contradiction:** `branches/B001/state/current_state.md`, line 30 says “Cycle 1 has not started,” while `branches/B001/state/control.json`, lines 5–7 assigns cycle 1 to the Internal Evidence Researcher, and both `01_explorer.md` and `02_critic.md` exist. The accepted-state status line is stale relative to control and cycle artifacts. This does not authorize modification of state.
2. **Clean ladder versus bundled treatment:** The Explorer presents the four workflows as a useful minimal comparison (`01_explorer.md`, lines 67–85). The Critic argues that the decisive staged-versus-role-separated contrast simultaneously changes invocation boundaries, handoff compression, information access, prompt wording, persistence, and resampling (`02_critic.md`, lines 22–34). The Critic’s objection prevents treating the ladder as a causal isolation design.
3. **Role specialization versus procedural factors:** `C0001-EXP-01`, `C0001-EXP-03`, and `C0001-EXP-04` offer overlapping explanations. The Critic explicitly states that agent identity, separate invocation, fresh context, and role specialization are blurred (`02_critic.md`, lines 38–45).
4. **Metric availability versus metric validity:** The Explorer lists unsupported claims, provenance fraction, contradiction, uncertainty retention, error movement, duplication, and budget efficiency (`01_explorer.md`, lines 75–83). The Critic objects that these lack claim units, denominators, adjudication, coverage controls, and error-lineage rules (`02_critic.md`, lines 30–34 and 50–56).
5. **Ablation interpretation:** The Explorer proposes marginal change when roles or artifacts are removed (`01_explorer.md`, line 83). The Critic notes that role removal also changes compute and distinguishes budget-removed from budget-reallocated ablations (`02_critic.md`, lines 54–56 and 133–144).

## Changes Across Recent Cycles

No prior cycles exist for comparison. Current cycle is C0001, so there are no preceding Dense Cycle Summaries within the authorized range.

Within C0001, the Critic narrows the Explorer’s broad factorial direction into two immediate requirements:
- define one primary estimand: the marginal effect of fresh role-separated execution after equalizing functional stages, instructions, state, information, tools, and compute;
- operationalize claim segmentation, support adjudication, error lineage, coverage, and budget accounting before interpreting results.

These are design corrections, not new empirical findings.

## Duplicated or Previously Explored Ideas

- `C0001-EXP-01` substantially restates the accepted branch hypothesis that role separation may reduce cumulative error through narrower objectives and contexts.
- `C0001-EXP-02` substantially restates the accepted branch hypothesis that external memory and provenance may matter more than agent count.
- `C0001-EXP-04` and `C0001-EXP-05` elaborate the already recognized context-isolation tradeoff; they are not internally supported discoveries.
- `C0001-EXP-06` reformulates the unresolved question about which failure modes role separation can reduce.
- The Explorer’s fixed-compute warning repeats the accepted compute-confound objection.
- The Critic’s same-model correlation warning is consistent with the protocol’s rule that repeated same-model agreement is not independent evidence; repetition here strengthens procedural emphasis but does not add independent support.

## Internal Evidence Gaps

- No accepted external evidence or accepted empirical claims exist.
- No branch-local factor matrix has yet been stored.
- “Role separation,” “single agent,” “structured state,” “adversarial structure,” “unsupported claim,” “cumulative reasoning error,” “fixed compute,” and “unique role value” lack accepted operational definitions.
- No claim segmentation, support-adjudication, denominator, factual-coverage, or omission-coding procedure exists.
- No error-lineage record shows where errors are introduced, preserved, corrected, amplified, or transformed.
- No compute ledger records prompt tokens, completion tokens, context processing, state-maintenance cost, tool use, samples, or calls by stage.
- No evidence establishes that different conditions can receive equivalent information sets.
- No evaluator design establishes independence, reliability, or treatment of shared-model bias.
- No provenance record tests support correctness rather than citation presence.
- No ablation evidence distinguishes role contribution from freed-compute reallocation.
- No internal evidence measures handoff compression, omitted dependencies, duplicated work, or contradiction introduced by the seven-role interfaces.

## Questions Requiring External Evidence

1. Are there primary studies or benchmark reports that compare role-separated fresh invocations with a staged single-model workflow while matching model, task, stage prompts, information access, tools, and inference budget?
2. Which studies separately ablate fresh-context boundaries, structured memory/provenance, critique or verification stages, and handoff compression?
3. How do direct studies operationalize and account for fixed compute, including prompt/context processing, completions, sampling opportunities, tool calls, and state-maintenance overhead?
4. Which evaluations define claim units, verify that evidence actually supports each claim, normalize for factual coverage, and trace error lineage across stages?
5. Do matched studies report null or negative findings, especially worse correction under fresh contexts or gains that disappear after compute and coverage normalization?
6. What direct evidence exists about correlated errors among same-base-model agents, and does any study connect correlation to the exact role-separated-versus-staged contrast?
7. Which role or stage ablations distinguish contribution with compute removed from replaceability with compute reallocated?

## Handoff to External Evidence Researcher

Treat the branch as having no accepted empirical support for any claimed benefit of role separation. Screen first for direct matched-budget evidence addressing a narrowly defined contrast: same model, task, functional stages, stage instructions, artifacts, information set, tools, evaluator, and primary compute budget, with fresh role-separated execution as the declared varying factor. Record every additional difference as a confound. Separate direct evidence from adjacent self-refinement, debate, ensemble, retrieval, or tool-agent evidence. Extract null and negative results deliberately. For each source, report operational definitions, budget accounting, outcome coding, factual-coverage controls, evaluator independence, provenance-support verification, and whether ablation compute was removed or reallocated.