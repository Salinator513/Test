# Critic — C0003

## Fair Reconstruction of the Explorer’s Direction

The Explorer proposes making the branch’s state-transfer problem operational before returning to fresh-versus-persistent comparisons. The intended frontier has three connected parts:

1. Define a minimal stage package that preserves claim identity, epistemic status, support, qualifications, objections, unresolved questions, and relations.
2. Compare package variants to test whether explicit relation and status metadata reduce unsupported promotion, qualification loss, and claim-lineage mutation.
3. Use exact-package replay and checkpoint scoring to distinguish information lost during package writing from information available in the package but not retrieved or correctly used downstream.

The favored direction is not that typed packages are already known to help. It is that package construction, package representation, downstream access, and downstream use must be separated before the branch can interpret any later workflow comparison.

## What Is Strong or Worth Preserving

- The frontier directly addresses the accepted operational gap rather than reopening the rejected general question of whether multi-agent systems are superior.
- The Explorer correctly treats package structure, typing, ordering, grouping, and relation links as active interventions rather than neutral formatting.
- The distinction among write loss, retrieval loss, and downstream misuse is worth preserving.
- Exact-package replay is a useful control for package-construction variance, provided its conclusions are limited to downstream variation under a fixed package.
- The coverage gate, task-completion controls, manipulation checks, compute ledger, and warning that lower unsupported-claim counts may reflect omission are already adequate in direction.
- The proposal explicitly marks the unresolved-question mechanism as speculation and acknowledges evaluator bias, oracle-package privilege, and transfer limits. Those cautions should remain.

## Fatal Problems

### 1. The proposed “matched-information” flat-versus-relational contrast is not actually information matched

A package with explicit support, qualification, contradiction, dependency, status, or unresolved-question links contains information that a flat list without those links does not contain, even when both contain the same atomic claim sentences. Atomic-item equality is therefore not informational equivalence. The proposed comparison can estimate the effect of supplying explicit metadata, but it cannot by itself establish a pure effect of “structure” while holding information constant.

This is fatal only to the current causal description, not to the frontier. The contrast must be renamed and split:

- **Metadata-availability contrast:** identical base claims, with versus without one predeclared relation or status field. This estimates the value of making that metadata available.
- **Representation contrast:** the same predeclared relation expressed in two forms, such as controlled prose versus a typed edge, with semantic content approximately matched. This is the closer test of representation, though equivalence still requires manipulation checks.

### 2. The frontier does not yet identify one primary estimand

The proposal simultaneously targets relation metadata, epistemic-status labels, package minimality, package-writing quality, information geometry, reader capability, retrieval, unresolved-question continuity, and task interactions. These are distinct interventions and diagnostics. A broad search across all of them would produce heterogeneous evidence that cannot jointly answer one causal question.

The research direction must declare one primary estimand before resources are spent. The smallest defensible primary estimand is:

> Under a declared end-to-end budget, what changes when one predeclared metadata type is made explicitly available in an otherwise fixed base package, with coverage, task completion, package position, downstream instructions, model settings, and evaluation held constant as far as feasible?

Write–retrieve–use decomposition should be treated as a diagnostic framework supporting that estimand, not as a second effect claim.

## Material Problems

1. **The “oracle versus agent-written” comparison is confounded.** A reference package may add privileged judgment, corrected content, better relation annotations, more labor, or downstream-informed choices. It does not identify package-writing loss unless the reference inventory and annotations are fixed before condition outputs, constructed without downstream-output access, validated independently, and scored under the same schema.

2. **Exact replay does not by itself identify retrieval failure.** Variation across readers of a byte-identical package establishes only that downstream processes vary. Retrieval failure requires an observed retrieval or selection checkpoint. Misuse requires showing that an item was available or selected but was transformed incorrectly in the final output.

3. **“Write-dominant” is undefined.** A “substantial share” needs a denominator, unit, and attribution rule. Counts of omissions, status changes, and relation breaks are not directly comparable to final unsupported claims without a lineage rule connecting upstream defects to downstream outcomes.

4. **Relation preservation and epistemic-status preservation are bundled.** A status label, a support edge, a qualification edge, and an unresolved-question link may have different effects and failure modes. Combining them in the first comparison would make any result uninterpretable.

5. **Length matching can create a second intervention.** Removing relation metadata to equalize tokens may delete useful claim text; adding filler to the control may change salience and retrieval competition. The branch must distinguish a primary budget rule from secondary token and position matching rather than pretending all dimensions can be equalized simultaneously.

6. **The proposed field ablations may create malformed packages.** Removing one field can break dependencies elsewhere in the schema. Each ablation needs a declared validity rule and a placebo or structurally valid control.

7. **Existing-cycle inspection cannot estimate causal prevalence.** Observed omissions or status promotions in prior artifacts can motivate a codebook, but those artifacts were not produced under randomized or matched package conditions. They cannot establish that writing is the dominant bottleneck.

8. **The task interaction is underdefined.** “Separable” and “dependency-dense” require predeclared task-level criteria. Classifying tasks after observing condition performance would invite circular subgroup conclusions.

## Minor Problems

- “Byte-identical” is stronger than needed for some diagnostics and insufficient for others; package hash, surrounding-context identity, position, and prompt identity should be reported separately.
- “Minimal sufficient package” risks implying a single universal minimum. Sufficiency is task-, stage-, reader-, and outcome-relative.
- “High-value item” is undefined and could become a post hoc label for items whose omission harmed performance.
- “Textually similar packages” is too weak for epistemic-status tests because small wording differences can change certainty and scope.
- Repeated-reader variance should not be called “loss” unless a reference outcome and scoring rule are defined.
- Unresolved-question continuity may be redundant with ordinary task instructions; it should remain deferred until the core contrast is coherent.

## Hidden Assumptions

- Atomic claims can be identified independently of their support, qualification, contradiction, temporal, causal, or dependency relations.
- A predeclared gold inventory and relation graph can be constructed without importing the evaluator’s preferred reasoning path.
- Status labels are correct, stable, and sufficiently unambiguous to serve as treatment metadata.
- Claim identity can be tracked reliably across paraphrase, compression, splitting, and merging.
- Package-writing, retrieval, and use errors can be assigned to one checkpoint rather than jointly caused across checkpoints.
- A downstream reader has effective access to every package item merely because the item is present.
- Token count, context position, semantic content, and total inference compute can all be held sufficiently constant in one comparison.
- A small pilot inventory represents full research synthesis and multiple stage transitions.
- A relation link helps because it preserves reasoning structure rather than because it acts as an attention cue.
- Reference-package validation does not itself introduce an additional verifier-quality intervention.

## Scope and Definition Problems

The following terms require operational definitions before research begins:

- **Minimal:** minimum fields, minimum tokens, or minimum task-sufficient information?
- **Flat package:** claims only, claims plus citations, controlled prose relations, or merely no explicit graph edges?
- **Typed relational package:** which exact status types and relation types are mandatory?
- **Same atomic information:** identical strings, identical propositions, identical evidence excerpts, or identical predeclared inventory membership?
- **Write loss:** omission, incorrect inclusion, retyping, relation deletion, qualification weakening, or unsupported synthesis introduced at package construction?
- **Retrieval:** model attention, explicit tool selection, quoted package subset, or an externally logged selection step?
- **Use failure:** selected evidence omitted from output, contradicted, misquoted, overgeneralized, or assigned the wrong epistemic status?
- **Lineage mutation:** what degree of wording or scope change creates a new claim identity?
- **Oracle/reference package:** who constructs it, from what fixed inputs, with what adjudication, and without access to which downstream artifacts?
- **Dependency-dense task:** what pre-output criterion establishes density?
- **Sufficiency:** sufficient for factual coverage, task completion, supported conclusions, or all three?

The first pilot should use one stage transition, one package schema version, one relation or status metadata type, and one predeclared task-relative inventory. Broad optimization across all seven transitions is premature.

## Risks of Misleading Research

- A lower unsupported-claim rate may be caused by fewer claims, weaker conclusions, or reduced task coverage.
- A typed package may appear superior because it contains additional relation information, not because the representation is better.
- A reference package may appear superior because it embeds privileged evaluator judgment or additional verification effort.
- Equal package length may conceal unequal information density, salience, or construction cost.
- A null result may reflect weak or invalid annotations, treatment collapse, low task sensitivity, or unreliable lineage coding.
- Positive results from structured-memory systems may be wrongly attributed to relation preservation when retrieval tools, extra calls, selectors, or larger context are bundled.
- Existing branch artifacts may be selectively coded around known errors, overstating write-stage failure.
- Model-based evaluators may prefer explicit schemas similar to their own instructions, creating format-aligned evaluation bias.
- Searching broadly for “structured memory” may duplicate C0002 and create the appearance of new independent support from already represented mechanisms or benchmark families.
- A package can preserve every listed item while changing adjacency, scope, status, or support relations enough to alter effective meaning.

## Questions That Would Not Actually Discriminate

Several proposed questions are useful for design or measurement but do not discriminate among the hypotheses as written:

- Internal questions about which fields already exist, which relations are in prose, which claim IDs can populate a pilot, and what artifacts are needed for replay help build the apparatus but do not test relation-preservation, status-preservation, or write-dominant hypotheses.
- Inspecting where prior-cycle omissions occurred cannot distinguish write-dominant from reader-dominant failure without matched counterfactual packages and observed retrieval/use checkpoints.
- Asking whether any primary structured-state studies exist does not distinguish added metadata from representation, tools, retrieval, verification, or compute.
- Annotation-scheme and resource-accounting studies improve measurement validity but do not show that typed packages improve outcomes.
- Evidence about ordering or irrelevant context does not test relation metadata unless item content and relation availability are separately controlled.
- Evidence about explicit uncertainty labels does not test support-link or dependency-link effects and should not be pooled with them.
- Open-ended research-synthesis transfer studies address scope, not the mechanism, unless they implement the corrected contrast.

## Required Corrections to the Research Direction

1. **Declare one primary estimand.** Start with one metadata type, preferably a claim–support or qualification relation, rather than the full typed-relational schema.

2. **Separate availability from representation.** Do not describe a relation-present versus relation-absent comparison as information matched. Run or conceptually distinguish:
   - relation absent versus relation explicitly available; and
   - the same relation expressed in controlled prose versus a typed field or edge.

3. **Keep epistemic-status labels separate.** Test status preservation only after status definitions and transition rules are reliable. Do not combine it with support, qualification, contradiction, and unresolved-question links in the first treatment.

4. **Recast the oracle.** Use a predeclared, independently validated **reference package**, constructed before downstream runs and without downstream-output access. Record its additional construction and validation cost. Treat it as a diagnostic upper-bound condition, not a matched production alternative.

5. **Make the decomposition observable.** Score at least four explicitly defined objects: predeclared reference inventory and relations; written package; explicitly retrieved or selected subset where the design exposes one; and final claims. Presence in context alone is not retrieval.

6. **Define attribution and denominators.** Predeclare how an upstream omission, retyping, or broken edge is linked to a downstream unsupported claim or omission. Report stage-specific rates and final outcome rates rather than an undefined “share of cumulative error.”

7. **Use manipulation checks.** At minimum verify base-claim identity, relation/status annotation correctness, package hash, token count, field validity, item position and adjacency, surrounding-context volume, reader prompt, prior-trace access, model/settings, tool access, candidate/selector opportunities, reference inventory coverage, and actual end-to-end resource use.

8. **Choose a primary resource rule.** Declare whether the primary constraint is total inference tokens, monetary cost, calls, or another budget. Record package and validation overhead separately. Use token/position-matched placebo fields where feasible, while acknowledging that placebo text can affect salience.

9. **Predeclare falsifiers.** Evidence against the favored direction includes: no benefit after equivalent relation content is expressed in both conditions; equal improvement from inert but similarly structured metadata; reduced coverage or task completion; increased status or relation errors; low annotation reliability; or downstream use failures remaining as large as package-writing failures under the same reference inventory.

10. **Avoid duplication.** External work should not re-count broad structured-memory, condensation, long-context position, or write-versus-retrieval findings already represented in C0002 as new independent evidence. It should target directness to the corrected contrast and clearly label reused benchmark or mechanism families.

## Internal Research Brief

The Internal Evidence Researcher should produce a branch-local design and duplication audit, not a causal conclusion.

- Map accepted branch terms and existing conventions into a candidate schema, distinguishing claim fields from relation fields and administrative provenance from evidential support.
- Identify one defensible pilot stage transition and one small predeclared inventory that contains enough variation to test a single relation type. Do not optimize the whole schema.
- Define operational codes for claim identity, support edge, qualification edge, status, omission, retyping, relation break, retrieval/selection, and downstream misuse.
- Identify which existing records already support the apparatus and which proposed questions would repeat C0002’s accepted package, retention, geometry, compute, and measurement findings.
- Build a factor matrix separating base claim content, metadata availability, metadata representation, ordering, adjacency, context volume, writer, validator, reader instructions, prior-trace access, model/settings, tools, sampling, selector, and final integration.
- Specify the exact objects and hashes needed for immutable replay and the checkpoints needed to observe retrieval rather than infer it from final output.
- Treat observed defects in prior cycle artifacts as examples for codebook testing only. Do not estimate prevalence or dominance from them.
- Report any schema field whose definition cannot be grounded in accepted branch concepts as an unresolved ontology choice rather than silently importing it.

## External Research Brief

The External Evidence Researcher should search for primary evidence narrowly matched to the corrected estimand and diagnostic framework.

Priority questions:

1. Are there controlled studies that vary explicit claim–support, qualification, contradiction, dependency, or uncertainty metadata while holding the base claim content and downstream task approximately constant?
2. Are there studies comparing equivalent relational content expressed in prose versus typed fields, tables, graphs, or links, rather than relation-present versus relation-absent systems?
3. Are there primary diagnostic methods that separately observe memory/package writing, explicit retrieval or selection, and downstream use, with predeclared reference inventories or controlled corruptions?
4. Are there validated claim-lineage or epistemic-transition annotation methods with reported reliability for omission, retyping, qualification change, contradiction, correction, mutation, and amplification?
5. Are there controlled information-geometry studies that can serve as confound checks for metadata experiments rather than as evidence for metadata effects?
6. Do any direct studies report sufficient end-to-end cost and component detail to separate metadata availability, representation, retrieval tools, verifier effort, extra calls, and selector opportunities?

For every candidate source, record whether it manipulates metadata availability, representation, writer quality, retrieval, geometry, or verifier quality; whether base semantic content is matched; whether the task has predeclared reference relations; whether coverage and task completion are measured; and whether total resource use is comparable.

Broad structured-memory systems, graph-memory systems, condensation methods, and long-context studies may supply mechanism or design leads, but they are not direct evidence for the primary estimand when they bundle added information, tools, calls, retrieval, or validation. Reused C0002 sources, benchmarks, and mechanism families must be marked as prior branch evidence rather than counted as new independent support.

## Handoff

Proceed with the corrected frontier: one primary metadata contrast, explicit separation of information availability from representation, and a write–retrieve–use diagnostic that observes each checkpoint. Preserve exact-package replay as a downstream control, not as proof that write loss has been isolated. Treat the full typed-relational schema, package minimality, unresolved-question continuity, geometry optimization, and stage-by-stage expansion as later work.

The next role is `internal_evidence_researcher`. The cycle remains `C0003`.