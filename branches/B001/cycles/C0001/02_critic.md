# Critic — C0001

## Fair Reconstruction of the Explorer’s Direction

The Explorer proposes a first-cycle frontier centered on causal separation rather than broad claims about whether multi-agent systems “work.” The intended comparison is to hold task, model, total inference budget, tool access, and evaluator constant while distinguishing four candidate sources of benefit: repeated prompting, structured external state and provenance, staged adversarial functions, and fresh role-separated invocations with controlled handoffs.

The core hypotheses are that role specialization may have an independent effect; external memory and provenance may explain most gains; staged critique and evidence handling may matter more than nominal agent identity; fresh narrow contexts may reduce contamination but also lose useful continuity; effects may differ by failure mode; and some role value may be replaceable by deterministic structure. The proposed research program asks the Internal Evidence Researcher to formalize factors, artifacts, handoffs, definitions, and budget-matched controls, while asking the External Evidence Researcher to locate matched-budget comparisons, ablations, failure-mode evaluations, and evidence about correlated same-model errors.

This is a fair and relevant frontier. It directly addresses the branch’s central compute confound and avoids treating repeated same-model agreement as independent evidence.

## What Is Strong or Worth Preserving

- The Explorer correctly treats role separation, external memory, adversarial staging, and context partitioning as potentially distinct interventions rather than a single package.
- The proposed progression from an unstructured repeated-prompt baseline to structured state, staged functions, and role-separated fresh invocations is useful as an initial decomposition.
- The direction explicitly recognizes both possible benefits and costs of context partitioning.
- The candidate metrics cover provenance, contradiction, uncertainty retention, error movement across stages, duplication, and ablation rather than relying only on final-answer accuracy.
- The Explorer already flags evaluator bias, task dependence, prompt overhead, tool-call differences, and the non-equivalence of possible compute measures. Those cautions are adequate and should be retained.
- The frontier remains tied to the accepted branch hypotheses and objections rather than introducing an unrelated research program.

## Fatal Problems

### 1. The four proposed workflow conditions do not isolate an independent effect of role separation

The decisive contrast appears to be condition 3, “single-agent staged workflow,” versus condition 4, “role-separated workflow.” As written, that contrast may simultaneously change fresh-context boundaries, invocation count, handoff compression, information access, role-specific prompt wording, persistence of prior outputs, and opportunities for resampling. A result from that comparison could not be attributed specifically to role separation.

This is fatal to the stated causal aim unless the conditions are rewritten as an explicit factor matrix. “Role-separated” must be operationalized as one manipulable feature, not as a bundle of fresh invocations, narrow allowlists, separate files, and controlled handoffs.

### 2. The primary outcomes are not yet operational enough to support a discriminating result

“Unsupported claim” and “cumulative reasoning error” are the central outcomes, but neither has a declared unit of analysis, coding rule, denominator, adjudication method, or treatment of omissions and hedged statements. Raw unsupported-claim counts can improve merely because a workflow produces fewer factual claims or a shorter answer. Provenance traceability can improve while source support remains wrong or irrelevant. “Cumulative error” cannot be measured without a method for linking an error across stages and distinguishing preservation, correction, mutation, and newly introduced error.

Without a predeclared scoring scheme, the comparison can produce apparently favorable but non-comparable metrics.

## Material Problems

### 1. “Agent identity,” “separate invocation,” “fresh context,” and “role specialization” are blurred

All conditions use the same underlying model. The relevant difference is therefore procedural, not identity-based. A staged workflow can be run through one persistent conversation, multiple fresh invocations, or one invocation with internal sections. Those are materially different treatments. The research direction must define these separately.

### 2. The hypotheses overlap and are not yet mutually discriminating

C0001-EXP-01, C0001-EXP-03, and C0001-EXP-04 can all explain the same observed improvement. Distinct role objectives, structured adversarial passes, and fresh narrow contexts are currently bundled. A positive result for the full role loop would not distinguish among them. The hypotheses should be converted into explicit contrasts with predicted outcome patterns.

### 3. “Fixed inference compute” is acknowledged as ambiguous but still used as if one matching rule will suffice

Tokens, calls, sampled completions, context processing, tool use, and latency are not interchangeable. A study could be token-matched while giving one condition more independent samples or more effective reasoning turns. The design needs one primary budget definition plus secondary accounting variables. Otherwise “matched compute” can conceal a systematic advantage.

### 4. The proposed metrics can reward caution, terseness, or formatting instead of better reasoning

Unsupported claims per final answer, provenance fraction, and contradiction rate are sensitive to answer length, claim granularity, and willingness to make assertions. They should be paired with task completion, coverage, usefulness, or accuracy measures and normalized by the number and importance of factual claims.

### 5. Role ablations will be confounded unless freed compute is handled explicitly

Removing a role changes both workflow structure and available compute. Reallocating the freed budget to remaining stages tests replacement efficiency; leaving it unused tests the contribution of additional compute plus role function. Both may be useful, but they answer different questions.

### 6. The external research scope is too broad for a first cycle

The questions span multi-agent prompting, self-refinement, debate, ensembles, retrieval, external memory, tool agents, multiple task families, calibration, provenance, and error propagation. This breadth risks collecting many adjacent studies that do not isolate the target factors. The first pass should prioritize direct matched-budget comparisons and clean ablations, then use adjacent work only to explain mechanisms or gaps.

### 7. The current research questions do not specify what evidence would count against the favored direction

The Explorer lists uncertainty but does not define disconfirming patterns. Examples include no benefit after matching state and staging; worse error correction under fresh contexts; higher provenance traceability without higher support accuracy; or gains disappearing after normalizing for factual coverage and compute.

## Minor Problems

- Latency is listed beside tokens and calls, but it is an operational cost rather than a direct measure of inference compute. It may be worth reporting separately.
- C0001-EXP-07 is useful but premature for the first causal comparison unless a deterministic replacement is specified precisely.
- The second comparison on context exposure is valuable, but it should follow rather than compete with the primary factor-isolation design.
- “Unique role value” needs to distinguish irreplaceable function from value under one particular budget-allocation rule.
- The examples of task families are useful for later heterogeneity analysis but could dilute the initial matched comparison.

## Hidden Assumptions

- The same structured state can be supplied across conditions without changing its content quality or creation cost.
- A persistent single-agent process and a sequence of fresh same-model invocations can be made informationally equivalent.
- Prompt overhead, handoff summaries, and state maintenance can be fully charged to the same compute budget.
- The task set offers enough opportunities for unsupported claims and cumulative errors to produce measurable differences.
- The evaluator can reliably distinguish unsupported claims, incorrect claims, weak interpretations, and omissions.
- The evaluator’s judgments are not systematically aligned with the tested model’s own biases.
- Narrow contexts reduce anchoring rather than merely hiding dependencies needed for correction.
- Role order does not itself create the observed effect.
- The final integration stage has comparable access to evidence and uncertainty across all conditions.
- More traceable provenance corresponds to better epistemic support rather than better formatting compliance.

## Scope and Definition Problems

The frontier should define the following before external evidence is interpreted:

- **Role separation:** whether it means distinct objectives, distinct invocations, distinct context windows, distinct permissions, or all of these.
- **Single agent:** whether this means one persistent conversation, one model instance, one prompt, or one model used repeatedly.
- **Structured state:** exact fields, who creates them, when they are updated, and whether their creation cost is included.
- **Adversarial structure:** whether critique is mandatory, whether it sees the generator’s reasoning or only claims, and whether revision is required.
- **Unsupported claim:** the claim unit, acceptable support relation, treatment of common knowledge, and treatment of uncertainty language.
- **Cumulative reasoning error:** an error lineage that begins in one stage and is preserved, amplified, or transformed later.
- **Fixed compute:** the primary accounting unit and how prompt, completion, tool, evaluator, and state-maintenance costs are charged.
- **Unique role value:** marginal benefit under a declared budget reallocation rule, not simply performance loss after deletion.

## Risks of Misleading Research

- Treating studies with more calls, tokens, samples, tools, or retrieval as evidence for role separation.
- Treating role labels in prompts as equivalent to fresh-context role separation.
- Treating adjacent self-refinement or debate results as direct support when the intervention differs.
- Counting provenance links without verifying that they actually support the associated claim.
- Reporting lower unsupported-claim counts without accounting for reduced factual coverage.
- Using one same-model evaluator and interpreting agreement as objective correctness.
- Comparing workflows with unequal information sets because one condition sees full transcripts and another sees compressed state.
- Interpreting an ablation loss as unique role value when the ablation also removes compute or evidence access.
- Averaging across task families in a way that hides opposite effects by failure mode.
- Allowing the broad literature search to confirm the full-loop concept through loosely related positive studies while overlooking null or negative matched-budget findings.

## Questions That Would Not Actually Discriminate

The following questions are descriptive or too broad unless tightened:

- Internal question 1 identifies factors but does not determine which controlled contrast isolates each factor.
- Internal question 3 maps seven roles into functional stages but does not show whether role count, stage function, or context separation causes an effect.
- External question 3 gathers many evaluation measures but does not distinguish the proposed hypotheses.
- External question 5 on correlated errors is relevant to limitations, but by itself does not distinguish role specialization from staging or memory.
- External question 7 on task families may explain heterogeneity but cannot establish the independent effect of role separation.
- Asking whether studies compare “multi-agent” with “single-agent” is insufficient unless both terms are operationalized and compute, information access, staging, and tools are matched.

## Required Corrections to the Research Direction

1. State one primary estimand: the marginal effect of fresh role-separated execution after holding functional stages, role instructions, external state, information access, tools, model, and compute constant.
2. Replace the four-condition ladder with an explicit factor table. At minimum separate: structured state present/absent; staged role functions present/absent; persistent versus fresh context; and handoff compression present/absent. A full factorial may be too large, so declare a minimal set of contrasts and which hypothesis each contrast tests.
3. Define “single-agent staged” so it uses the same stage prompts and artifacts as the role-separated condition, differing only in the chosen role-separation factor.
4. Declare one primary compute-matching rule and record secondary resource measures. Charge prompt overhead, state construction, and handoff generation consistently.
5. Predefine claim segmentation, support adjudication, error lineage, normalization, and evaluator procedure.
6. Pair epistemic-error metrics with task completion and factual coverage so a workflow cannot win by saying less.
7. For each hypothesis, specify a predicted pattern and a result that would count against it.
8. Separate two ablation questions: contribution with compute removed, and replaceability with compute reallocated.
9. Narrow the first external search to direct matched-budget comparisons and factor ablations. Label adjacent evidence as indirect.
10. Defer broad task-family heterogeneity and deterministic-role replacement until the primary contrast is coherent.

## Internal Research Brief

- Build a branch-local factor inventory from the protocol: objective specialization, stage order, invocation boundaries, context visibility, allowlists, external state, claim labels, provenance rules, handoff format, tool access, and evaluator access.
- Produce a condition-by-factor matrix for the proposed baseline, structured-state, staged, and role-separated workflows. Mark every factor that changes in each contrast.
- Identify the smallest contrast that changes only fresh role-separated execution while keeping stage prompts, artifacts, information, and budget accounting constant.
- Define the exact information set available at every stage and identify where compression, omission, or duplicated evidence access occurs.
- Draft operational definitions and coding rules for unsupported claim, provenance support, contradiction, error lineage, coverage, duplicate effort, and unique role value.
- Distinguish ablation-with-budget-removed from ablation-with-budget-reallocated.
- Identify which proposed questions merely repeat the accepted objections and unresolved questions, and convert them into testable design decisions.
- State branch-local disconfirming patterns for C0001-EXP-01 through C0001-EXP-05. Do not infer empirical support.

## External Research Brief

- Prioritize primary studies and benchmark reports with genuinely matched model, task, tools, information access, and inference budget.
- For every study, record how “single agent,” “multi-agent,” “role,” “fresh context,” “memory,” “critique,” and “compute” are operationalized.
- Separate direct evidence from adjacent evidence. Studies that add calls, tokens, samples, retrieval, tools, or context without a matched control must not be treated as isolating role separation.
- Seek ablations that separately vary critique or verification, structured memory or provenance, fresh invocation boundaries, and handoff structure.
- Extract null and negative results as deliberately as positive results.
- Record task family, outcome definition, factual-coverage effects, evaluator type, evaluator independence, and whether support links were checked for correctness rather than presence.
- Treat same-model error correlation and handoff/interface loss as mechanism or limitation evidence unless a study directly ties them to the target contrast.
- Report absence of clean matched-budget evidence as a finding gap rather than filling it with loosely related self-refinement, debate, or ensemble studies.

## Handoff

The frontier is worth preserving, but the researchers should not treat the proposed four workflows as a clean causal design yet. The immediate priority is to operationalize the primary outcome and construct a factor matrix that makes the staged-versus-role-separated contrast differ in only one declared feature. External evidence should then be screened against that exact contrast, with unmatched adjacent studies labeled indirect.