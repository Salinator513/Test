# Explorer — C0003

## Selected Frontier

Define and test a minimal typed stage package that preserves claim identity, epistemic status, support, qualifications, objections, unresolved questions, and relation links, then use exact-package replay to separate package-writing loss from downstream reading, retrieval, and salience failures.

## Why This Frontier Now

C0002 moved the branch away from an undefined fresh-conversation effect and toward observable information-access, retention, transformation, relation-preservation, and compute factors. The immediate operational gap is that B001 has no canonical stage package or diagnostic that can tell whether a downstream error was caused when information was written into the package or when an unchanged package was later read and used.

This frontier is narrow enough to produce a concrete artifact and discriminating tests. It is also useful before another persistent-versus-fresh comparison: without a package schema, exact replay, and separate write/read diagnostics, any observed difference could still be attributed to omitted dependencies, status mutation, information geometry, or package-construction variability rather than the invocation boundary.

## Relevant Accepted Branch State

- **Accepted branch-design fact:** B001 already requires explicit epistemic distinctions and externalized accepted state, but the authorized branch record does not define a canonical serialized stage package, complete relation schema, or transformation log.
- **Accepted derived conclusion:** Effects attributed to freshness must instead be assigned to observable differences such as prior-trace access, package representation, retention, transformation, salience, retrieval, prompts, permissions, tools, sampling, selection, and compute unless a distinct residual property is defined.
- **Accepted qualified conclusion:** Filtering or package mediation may reduce harmful prior-trace interference and may also create interface loss by deleting, retyping, separating, or weakening valid dependencies.
- **Accepted methodological requirement:** State transfer must be measured across separate dimensions, including item retention, dependency coverage, relation and epistemic-status preservation, package size, transformation type, write loss, retrieval loss, and information geometry.
- **Current qualified hypothesis:** Write-time promotion, omission, classification, and relation preservation may explain more downstream failure than retrieval in some regimes.
- **Current unresolved question:** Whether relation-preserving packages outperform flat packages when atomic-item coverage, visible information, model, downstream instructions, and resource allocation are held approximately constant.

## Candidate Hypotheses and Possibilities

### C0003-EXP-01 — Relation-preservation hypothesis

**Hypothesis:** A typed relational package will reduce downstream unsupported claims and lineage mutations relative to a flat package containing the same atomic factual items because it preserves support, qualification, contradiction, dependency, and unresolved-question links.

This is not an accepted effect claim. The branch has accepted relation loss as a risk, but it has not established that adding relation links improves outcomes under matched information and compute.

### C0003-EXP-02 — Epistemic-status preservation hypothesis

**Hypothesis:** Explicitly carrying each item’s status—such as sourced fact, interpretation, derived conclusion, hypothesis, speculation, objection, or unresolved question—will reduce unsupported promotion and false certainty downstream compared with textually similar packages lacking status labels.

Distinguishing evidence would require tracking status transitions rather than only semantic similarity or final-answer correctness.

### C0003-EXP-03 — Write-dominant failure hypothesis

**Hypothesis:** A substantial share of cumulative error will originate during package construction through omission, retyping, qualification loss, or broken relation links, rather than during downstream retrieval or reasoning.

A result supporting this hypothesis would show that an oracle or independently validated package materially improves downstream performance over an agent-written package, while repeated readers of the same exact package show smaller losses.

### C0003-EXP-04 — Reader-and-geometry hypothesis

**Hypothesis:** Even with a byte-identical package, downstream performance will vary with ordering, adjacency, context volume, reader instructions, or reader capability. Exact-package replay across controlled readers may therefore reveal failures that cannot be attributed to write loss.

This possibility connects the accepted information-geometry hypothesis to a concrete diagnostic without treating package identity as sufficient informational equivalence.

### C0003-EXP-05 — Minimal-sufficient-package hypothesis

**Hypothesis:** A smaller package that preserves all predeclared high-value items and dependencies may outperform a larger package with the same core inventory plus irrelevant or weakly related material because the smaller package improves salience and reduces retrieval competition.

This remains unresolved and must be evaluated with coverage and task-completion controls so omission cannot masquerade as improvement.

### C0003-EXP-06 — Unresolved-question continuity

**Speculation:** Explicit links from unresolved questions to the claims and evidence they depend on may reduce premature closure and repeated unsupported inference in later stages.

This is only a speculative design possibility. No accepted branch evidence establishes a distinct benefit from unresolved-question links.

## Possible Mechanisms or Connections

1. **Atomic retention versus relational retention:** Two packages can contain the same sentences while differing in whether the reader can recover which source supports which claim, which qualification limits which conclusion, and which objection remains unresolved.
2. **Status mutation as cumulative error:** A hypothesis can become an apparent fact without substantial wording change. Typed status fields and transition logs may expose this failure earlier than final-answer factuality scoring.
3. **Write loss versus retrieval loss:** Comparing source inventory, written package, retrieved package subset, and final output can localize whether information disappeared before storage, was not selected later, or was selected but misused.
4. **Exact replay as a control:** Reusing the same immutable package across downstream conditions removes package-construction variance, allowing reader instructions, information geometry, context access, and invocation conditions to be studied separately.
5. **Package structure as an active intervention:** A schema is not neutral merely because factual inventory is unchanged. Typing, ordering, grouping, links, redundancy, and compression can alter salience and effective accessibility.
6. **Coverage-sensitive interpretation:** Lower unsupported-claim counts are not beneficial if a package suppresses difficult claims, dependencies, or task requirements. Package tests must jointly score support, coverage, usefulness, and lineage.

## Questions for Internal Evidence Research

1. Across the allowlisted B001 protocol, accepted state, and completed-cycle records, which fields or recurring conventions already represent claim identity, source support, epistemic status, scope, uncertainty, objections, contradictions, unresolved questions, and lineage?
2. Which required relations are currently expressed only in prose and would be lost if outputs were converted into a flat claim list?
3. At which stage transitions are omissions, status promotions, qualification loss, broken support links, or unresolved-question disappearance observable in existing cycle artifacts?
4. Can the branch define a minimal package schema using only concepts already accepted in `current_state.md`, without importing unaccepted ontology choices?
5. What branch-local artifacts would be needed to implement byte-identical package replay and prove that downstream conditions received the same package?
6. Which package-construction, validation, replay, retrieval, and downstream-reading costs must enter the fixed-compute ledger under the accepted causal-interpretation gate?
7. Can an internal factor matrix cleanly separate package content, package structure, item ordering, reader instructions, prior-trace access, model settings, tools, sampling opportunities, and downstream integration rules?
8. Which existing branch claim IDs could serve as a small pilot inventory containing facts, qualifications, hypotheses, objections, contradictions, and unresolved dependencies?

## Questions for External Evidence Research

1. Are there primary studies that compare flat summaries or memories with typed, relational, provenance-linked, graph-structured, or otherwise structured state while approximately matching underlying information inventory and end-to-end inference resources?
2. Are there primary methods that explicitly distinguish memory write failure from retrieval failure and downstream reasoning misuse using oracle memory, exact replay, controlled corruption, or equivalent diagnostics?
3. What primary-source evaluation methods measure preservation of claim-support links, epistemic status, qualifications, contradictions, temporal or causal dependencies, or unresolved questions across transformations?
4. Are there controlled studies where the same factual items are presented with different ordering, adjacency, grouping, relation links, or irrelevant-context volume, allowing information geometry to be separated from item retention?
5. What evidence exists on whether explicit uncertainty or epistemic-status labels prevent unsupported promotion, overconfidence, or factual mutation, and under what tasks and evaluator designs?
6. Are there validated annotation schemes for cross-stage claim identity and transitions such as introduced, preserved, omitted, retyped, contradicted, corrected, mutated, or amplified?
7. Which studies report full enough resource accounting to compare structured and flat state without confusing improved outcomes with added write-time calls, retrieval tools, selectors, or larger context budgets?
8. Do any primary studies test structured handoffs specifically in open-ended multi-source research synthesis rather than only memory QA, short-answer reasoning, or agentic task execution?

## Potential Tests or Comparisons

1. **Flat versus typed-relational package:** Construct two packages from one predeclared source inventory. Hold atomic items, model, downstream prompt, tools, and approximate package length constant; vary only status fields and relation links.
2. **Oracle versus agent-written package:** Compare a validated package preserving the predeclared inventory and dependencies with an agent-written package under the same schema. This estimates package-writing loss before downstream reading.
3. **Exact-package replay:** Replay one immutable package across multiple downstream runs, readers, or invocation conditions. Any variation cannot be attributed to differences in package construction, though it may still reflect sampling, reader capability, instructions, or context geometry.
4. **Field ablations:** Starting from one typed package, remove only epistemic-status labels, support links, qualifications, objections, unresolved-question links, or dependency edges one at a time while preserving the underlying text where possible.
5. **Geometry comparison:** Keep items and relation metadata constant while varying order, adjacency, grouping, and irrelevant-context volume. Measure whether the same information is used differently.
6. **Write–retrieve–use decomposition:** Score four checkpoints: source inventory to written package, written package to retrieved subset, retrieved subset to final claims, and final claims to task requirements.
7. **Dependency-density comparison:** Pilot the same package variants on at least one separable task and one dependency-dense task to test whether relation preservation matters more when conclusions require multiple linked premises.
8. **Coverage gate:** Require minimum factual coverage, task completion, and usefulness before interpreting lower unsupported-claim counts as improvement.
9. **Compute accounting:** Record package-generation and validation cost, input and output tokens by stage, retrieval and tool cost, candidate and selector opportunities, final integration cost, and the rule for unused budget.

## Main Uncertainties

- The minimal sufficient schema is unresolved; an overly large schema may add cost and burden, while an overly small schema may fail to preserve the relations of interest.
- A typed-relational package may change salience and reasoning behavior even when atomic item inventory is matched, so it should be treated as an active intervention rather than a neutral storage format.
- “Oracle package” construction may itself require judgment and could import evaluator assumptions or privileged knowledge.
- Exact package identity does not guarantee identical effective access if readers differ in context position, instructions, model capability, sampling, or surrounding context.
- Relation and status scoring may require human or model judgment; evaluator reliability and shared-model bias therefore remain material.
- Package-length matching may conflict with relation preservation. The branch must decide whether the primary constraint is equal bytes, equal tokens, equal inventory, equal total compute, or a declared combination.
- Results on a small pilot inventory may not transfer to full open-ended research synthesis or to all seven stage transitions.
- The speculative unresolved-question mechanism may prove redundant with ordinary task instructions or may increase attention to low-value uncertainties.

## Handoff to Critic

Assess whether this frontier isolates one coherent estimand or still bundles package schema, relation preservation, epistemic typing, and replay diagnostics. Identify the smallest defensible package contrast, the strongest treatment-collapse or measurement objection, and the minimum manipulation checks needed before Internal and External Evidence Researchers investigate it. In particular, test whether a flat-versus-relational comparison can truly hold atomic information and compute sufficiently constant, whether the proposed oracle creates privileged-information bias, and whether exact-package replay can distinguish write loss from reader and geometry effects without overclaiming causal identification.
