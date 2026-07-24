# Alternative Theorist — C0003

## Strongest Current Interpretation

The strongest current interpretation is a **relation-information account**, stated narrowly rather than as a general endorsement of typed packages.

**Core claim.** When a downstream stage receives an explicit, correct claim–support or qualification relation that is absent from an otherwise fixed base package, it may produce fewer unsupported promotions, broken qualifications, and support-lineage errors because the package supplies a substantive information object that the reader would otherwise have to reconstruct.

**Mechanism.** The relation narrows the downstream inference problem. Instead of independently discovering which evidence supports which claim, which limitation restricts which conclusion, or which items must be combined, the reader can condition on a supplied relation. This may reduce reconstruction failures, especially where support is dispersed or multi-item. `C0003-EXT-03` and `C0003-EXT-04` show that claim–evidence recovery and multi-sentence or multi-page evidence relations are difficult and measurable. `C0003-INT-05` and `C0003-INT-06` preserve the branch-local reasons to treat relation loss as a plausible interface failure and to measure relation preservation separately.

**What this interpretation does not claim.** It does not claim that typed edges are superior to controlled prose, that relation metadata is always correct, that more links are monotonically beneficial, that package writing is the dominant bottleneck, or that the effect survives fixed end-to-end compute. The Critic’s correction is decisive: relation-present versus relation-absent is not information matched. It estimates the value of making a relation available, not a pure structural-format effect. No located source directly tests the corrected contrast in B001-style open-ended synthesis under matched full resources (`C0003-EXT-08`).

**Current evidential status.** Evidence-backed as a plausible mechanism and justified experimental target; unsupported as an established performance effect. The strongest external support is indirect: relational information can be difficult to reconstruct, representation changes behavior, and explicit metadata can causally alter evidence use. Those facts justify a narrow pilot but do not identify why a positive result would occur.

## Alternative Theory 1

### Representation, Geometry, and Format-Familiarity Account

- **Core claim:** Apparent benefits from typed claim–support or qualification metadata may arise mainly from how the same or similar relational content is serialized and positioned, not from preserving an epistemically meaningful relation as such.
- **Mechanism:** Typed fields or edges can shorten token distance between related items, increase adjacency, reduce redundant prose, impose a familiar schema, create salient delimiters, or reduce the number of transformations required before use. Conversely, they can harm readers whose learned format preferences differ. The active variables are information geometry, compactness, ordering, grouping, delimiter conventions, and reader-specific format familiarity.
- **Evidence it explains:**
  - `C0003-EXT-01`: approximately equivalent entity-relation content produces different outcomes across triples, paths, and natural-language representations, with model-specific preferences.
  - `C0003-EXT-01` and `C0003-SRC-04`: table serialization, order, partition marks, and prompt choices affect performance even when the underlying cells are similar.
  - `C0003-EXT-09`: metadata may function through attention capture rather than improved evidence reasoning.
  - `C0003-INT-04`, `C0003-INT-05`, and `C0003-INT-06`: package representation, salience, adjacency, and retrieval geometry are already accepted observable factors and risks.
  - A result where typed edges outperform uncontrolled prose, where effects differ sharply by reader model, or where gains vanish after position and token-path matching.
- **Evidence it struggles with:**
  - A robust benefit for explicit relation availability when representation, position, adjacency, token length, and surrounding context are held approximately constant.
  - Better handling of selectively corrupted links: if readers use relation correctness rather than merely follow salient structure, correct links should help and incorrect links should predictably harm in relation-specific ways.
  - Improvement in claim-level support assignment without corresponding changes in generic retrieval or attention measures.
- **Predictions:**
  1. Equivalent controlled prose and typed edges will converge when relation content, adjacency, order, length, and reader instructions are matched.
  2. Effects will vary substantially by reader model and serialization family.
  3. Inert but similarly shaped metadata or delimiters may reproduce part of the gain.
  4. Reordering, grouping, or shortening a flat package may recover much of the typed-package advantage.
  5. Benefits will correlate with reduced relation-token distance and improved observed selection, not necessarily with epistemic-status fidelity.

**Status:** Evidence-backed alternative. The evidence establishes representation sensitivity, though not that it fully explains a future C0003 treatment effect.

## Alternative Theory 2

### Authority-Cue and Evaluator-Alignment Account

- **Core claim:** Explicit labels, links, and structured fields may change answers because they appear authoritative, recent, validated, or evaluator-compatible, rather than because the reader reasons better from the underlying evidence.
- **Mechanism:** The reader may treat a `supports`, `qualified_by`, or status field as an instruction-like cue. The cue can increase compliance with the linked claim, suppress independent checking, or bias confidence. Structured evaluators may then reward outputs that mirror their own claim–evidence schema, creating an apparent improvement even when real support quality is unchanged. Human-validated reference packages intensify this mechanism by combining metadata with privileged correction and verifier labor.
- **Evidence it explains:**
  - `C0003-EXT-02`: swapping publication-time, source, or visual metadata over fixed conflicting text causally changes which evidence models follow; the effect is not necessarily epistemically beneficial.
  - `C0003-EXT-09`: metadata can act as a superficial authority or attention cue.
  - `C0003-EXT-10`: epistemic-marker meanings vary across datasets and cannot be presumed stable.
  - `C0003-EXT-11`: structured and multi-object annotation contains material judgment variance.
  - `C0003-EXT-07`: structured prewriting can improve organization and breadth while still transferring source bias or fabricating associations.
  - The Critic’s evaluator-format-alignment and reference-package-privilege objections.
- **Evidence it struggles with:**
  - Gains that survive format-blinded human evaluation and do not depend on outputs mirroring the evaluator’s schema.
  - Reader behavior that tracks link correctness under blinded correct-link, corrupted-link, and placebo-link conditions rather than trusting all structured links similarly.
  - Improvements when relation information is presented in low-authority controlled prose with no gold, verified, or system-like framing.
  - Benefits localized to correct support use rather than generalized confidence, verbosity, or schema compliance.
- **Predictions:**
  1. Incorrect but authoritative-looking links will pull conclusions toward the linked claims, possibly increasing confident support errors.
  2. Gold or “validated” framing will produce larger effects than identical unlabeled relation content.
  3. Structured model-based evaluators will report larger gains than format-blinded human evaluators when evaluator alignment contributes materially.
  4. Placebo fields with authoritative names may change behavior even without valid relational content.
  5. The treatment may improve schema conformity and apparent citation linkage while leaving citation completeness, source correctness, or task coverage unchanged.

**Status:** Evidence-backed alternative for metadata generally; partly speculative for claim–support edges specifically because no direct corrected experiment exists.

## Additional Alternative or Null Explanation

### Reader-Bottleneck, Resource-Allocation, and Selection Null

**Core claim.** After relation content, representation, geometry, prompts, tools, sampling, selection, and end-to-end resources are controlled, explicit metadata may have little or no stable benefit because the downstream reader remains the dominant bottleneck or because apparent gains in prior systems came from added resources rather than metadata.

**Mechanisms.** Several minimal mechanisms can produce the same observed pattern:

1. **Reader non-use:** The relation is present but not selected, attended to, or correctly applied. Presence in context is not retrieval (`C0003-INT-08`; `C0003-EXT-05`).
2. **Writer and validator privilege:** A reference package improves performance because experts corrected content, adjudicated links, or spent extra labor, not because the package schema is intrinsically better.
3. **More compute or longer processing:** Multi-pass extraction, self-augmentation, retrieval, uncertainty estimation, curation, outlining, or validation creates more opportunities to find correct evidence. `C0003-EXT-13` and the Fixed-Compute section explicitly identify these bundles.
4. **Repeated sampling and selection:** Multiple candidate responses, more retrieval attempts, or a stronger selector can improve final outcomes even if relation metadata adds no value. The current sources do not isolate these opportunities under the accepted budget gate.
5. **Better prompts:** Specialized prompts can direct attention to evidence relations without requiring a typed package. A package effect can disappear when the control receives equally strong relation-seeking instructions.
6. **Selection and reporting effects:** Positive tasks, formats, models, or metrics may be emphasized while null or harmful conditions, coverage loss, false links, and noise sensitivity receive less weight. The branch record does not provide a branch-local experiment or a complete external fixed-compute comparison capable of excluding this explanation.

**Evidence it explains.** It explains why iterative claim–evidence extraction improves recall while adding calls and false positives; why uncertainty-aware systems improve only with sampling and training machinery; why STORM improves organization and breadth while bundling retrieval, roles, curation, and outlining; and why exact replay can still show downstream variation under a fixed package.

**Evidence it struggles with.** A predeclared, sufficiently powered experiment in which correct relation metadata improves support precision and coverage under a fixed end-to-end budget; the same relation content and geometry are controlled; selection and candidate opportunities are equal; and observed retrieval and use show a relation-specific pathway.

**Predictions.** Under strict budget matching, effects will shrink or reverse; equivalent prompt scaffolding will recover much of the gain; reference-package advantages will exceed production-package advantages; and reader errors will remain substantial even with validated relations. Stronger or better-instructed readers may benefit less from explicit links because they can reconstruct them, or more because they can exploit them—so the sign of reader capability interaction remains unresolved and must be tested rather than assumed.

**Status:** The no-stable-benefit portion is an unresolved null, not an established zero effect. The resource-allocation and selection mechanisms are evidence-backed confounds; reporting bias is plausible but not directly demonstrated by the current ledger.

## Hybrid Explanations

The available evidence favors a multi-mechanism account over a single universal theory.

1. **Relation information plus geometry.** A correct support relation may genuinely add missing information while a compact typed representation also makes that information easier to select. A positive effect would then be jointly caused by information availability and geometry; neither a relation-absent control nor an uncontrolled prose control can isolate the components.

2. **Relation information plus authority cue.** Correct links can improve support assignment while authoritative presentation simultaneously encourages over-trust. This predicts gains on supported claims and harms under corrupted or incomplete links. Relation precision and relation coverage must therefore be scored separately.

3. **Geometry plus reader bottleneck.** Better adjacency may improve observed selection, but the reader may still misuse selected evidence. Exact replay with explicit selected-subset logging can show improved retrieval without improved final support.

4. **Writer quality plus validator privilege plus selection.** A reference package may contain better relations because it was created and adjudicated with more labor. Downstream gains would then combine write-quality improvement, verifier information, and possibly more favorable item selection. This is a diagnostic upper bound, not a matched production treatment.

5. **Coverage–noise tradeoff.** More relations can recover dispersed evidence and improve coverage while also introducing false links, irrelevant dependencies, and noise. `C0003-EXT-12` directly supports this sign-reversing possibility. A system can improve one outcome and worsen another without either result being anomalous.

6. **Task × reader × relation interaction.** Dependency-dense tasks may benefit more from correct explicit relations, while separable tasks may gain little and suffer more from added metadata. Different reader models may reverse format preferences. The current evidence makes this plausible but does not provide a predeclared interaction estimate.

## False Dichotomies or Framing Problems

1. **“Structure versus information” is a false dichotomy.** Typed relations can both add substantive information and change representation. Relation availability and relation representation require separate contrasts.

2. **“Write loss versus retrieval loss” can be falsely exclusive.** A weak package may omit one dependency, the reader may fail to select another retained item, and the final stage may misuse a selected item. One final error can have multiple contributing checkpoints.

3. **“Correct package versus capable reader” is not an either–or choice.** A correct package can be necessary but insufficient, and a capable reader can compensate for missing relations at additional cost.

4. **“More coverage versus fewer unsupported claims” is not a single quality axis.** A package can reduce unsupported output by suppressing difficult claims, or improve coverage while increasing false links. Support precision, relation precision, coverage, task completion, usefulness, and omission severity must remain separate.

5. **“Typed edge versus flat list” is too coarse.** Controlled prose, grouped prose, inline citations, tables, triples, graphs, and schema fields differ in content, adjacency, compactness, and learned familiarity. A binary package label hides the actual treatment.

6. **“Positive versus null effect” hides treatment collapse and subgroup cancellation.** A null can mean no causal effect, weak annotations, unread metadata, insensitive tasks, unreliable measurement, opposing task or model effects, or no distinct manipulation.

7. **“Role separation versus no role separation” remains the wrong immediate framing.** The present evidence concerns metadata, representation, access, writer quality, verifier information, retrieval, prompts, sampling, selection, and compute. None isolates fresh invocation boundaries or role separation itself.

## Discriminating Tests

1. **Metadata-availability test.** Hold base claims fixed. Add one predeclared correct claim–support or qualification relation in the treatment. Include relation-absent, correct-relation, corrupted-relation, and inert-placebo conditions. This separates useful relation information from generic structured-cue effects.

2. **Equivalent-content representation test.** Express the same predeclared relation in controlled prose and in a typed field or edge. Match position, adjacency, order, and surrounding context as closely as feasible; report remaining token and density differences. Typed superiority here favors the representation/geometry account over the pure added-information account.

3. **Authority-framing test.** Present byte-identical relation content with neutral, “system-validated,” and unlabeled framing. A framing effect without content change supports the authority-cue account.

4. **Evaluator-blinding test.** Compare format-blinded human judgments with structured model-based evaluation. A large evaluator-by-format interaction supports evaluator alignment rather than genuine support improvement.

5. **Correct-versus-corrupted link sensitivity.** Correct links should improve claim-specific support use; corrupted links should produce predictable claim-specific harm. Equal following of correct and incorrect links supports cue compliance or blind trust.

6. **Observed write–retrieve–use chain.** Record the reference inventory and relations, written package, explicit selected subset, and final claims. Score each transition separately. This distinguishes absent-at-write, present-but-unselected, selected-but-unused, and selected-but-misused cases.

7. **Exact-package replay across readers.** Replay the same hashed package with identical surrounding context and prompt across reader models and repeated samples. Model-specific or high-variance effects favor reader/format or sampling accounts; stable relation-specific gains favor the relation-information account.

8. **Prompt-equivalence control.** Give the relation-absent condition a prompt that explicitly asks the reader to reconstruct support links, with matched output and compute limits. Recovery of performance would show that prompt specialization, not package metadata alone, explains the benefit.

9. **Budget-reallocation pair.** Run the comparison twice: first leave metadata-construction savings or costs unused; then reallocate them under a predeclared rule. Differences between the two estimates expose whether resource allocation drives the result.

10. **Candidate and selector control.** Equalize repeated sampling, retrieval attempts, candidate count, and selector access. A gain that disappears under equal opportunities supports the sampling/selection explanation.

11. **Geometry-only perturbation.** Keep relation content constant while varying adjacency, order, delimiters, and irrelevant context. If performance follows geometry rather than relation coding, Alternative Theory 1 gains support.

12. **Coverage and noise stress test.** Vary relation precision and relation coverage independently. The relation-information account predicts benefit from correct missing links; the authority-cue account predicts disproportionate harm from authoritative incorrect links; the null predicts small effects once reader and resource controls are imposed.

13. **Predeclared task-strata test.** Define separable and dependency-dense tasks before outputs are observed. A relation benefit concentrated in dependency-dense tasks supports a genuine dependency-reduction mechanism; post hoc strata should not be used.

14. **Reference-package decomposition.** Separately compare agent-written, independently validated without correction, corrected reference, and corrected-plus-validated packages, with all extra labor and inference cost recorded. This distinguishes schema value from validation and privileged correction.

## Comparative Evidence Table

| Theory | Main causal variable | Evidence it explains well | Evidence or result that would weaken it | Current status |
|---|---|---|---|---|
| Relation-information account | Availability of a correct claim–support or qualification relation | Difficulty of reconstructing dispersed claim–evidence links; need for relation-aware scoring; plausible interface-loss mechanism | No gain over relation-absent control under matched budget, or gains equally produced by inert structure | Plausible, experimentally justified, not established |
| Representation/geometry account | Serialization, adjacency, order, compactness, delimiters, reader format familiarity | `C0003-EXT-01`; table and KG representation sensitivity; model-specific preferences | Stable benefit when equivalent content and geometry are matched; relation-specific corrupted-link response | Evidence-backed alternative |
| Authority-cue/evaluator-alignment account | Perceived validation, trust cue, recency/appearance cue, evaluator format match | `C0003-EXT-02`, `C0003-EXT-09`, marker instability, format-aligned scoring risk | Format-blinded human gains; neutral framing; correct links used while equally salient corrupted links are rejected | Evidence-backed for metadata generally; partly speculative for support edges |
| Reader-bottleneck null | Failure to select or use relations despite their presence | Exact replay variation; retrieval/use separation; persistent reader errors | Clear relation-specific pathway from supplied link to selected item to supported final claim | Unresolved null |
| Resource-allocation/sampling/selection account | Extra calls, longer processing, validation, candidates, selectors, stronger prompts | Iterative extraction, UAlign, STORM, self-augmentation, reference-package privilege | Benefit under equal end-to-end resources and equal candidate/selector opportunities | Evidence-backed confound |
| Coverage–noise hybrid | Correct-link recall and false-link/noise exposure jointly change | Recall–precision tradeoffs, noise sensitivity, fabricated associations | Monotonic improvement across independent relation precision and coverage manipulations | Evidence-backed interaction account |

## Remaining Uncertainty

No current theory is adequate as a general explanation. The strongest interpretation is plausible because explicit support relations are substantive and difficult to reconstruct, but the same evidence also shows that metadata, format, ordering, and authority cues can redirect behavior without improving epistemic quality. The branch has no internal causal estimate, no direct external corrected contrast, no validated full lineage codebook, no implemented selected-subset checkpoint, and no accepted full resource rule.

The largest unresolved identification problem is not whether metadata changes outputs; that is already plausible. It is whether a correct claim–support or qualification relation improves supported task performance through relation-specific information use after representation, geometry, authority framing, evaluator alignment, prompts, tools, sampling, selection, writer/validator privilege, coverage, and compute are controlled.

The null remains live. A positive pilot may still be local to one reader, serialization, task, or evaluator. A null may still conceal treatment collapse, weak annotations, reader non-use, opposing subgroup effects, or inadequate power. No outcome should be generalized to role separation or fresh invocation boundaries.

## Handoff to Integrator

Preserve the relation-information account as the strongest current interpretation, but do not accept it as an empirical effect claim. Integrate the following as coequal live alternatives: representation/geometry and model-specific format familiarity; authority-cue and evaluator alignment; and a reader-bottleneck/resource-allocation null. Treat coverage–noise and writer–validator privilege as likely hybrid mechanisms rather than edge cases.

The first defensible pilot should use one stage transition, one predeclared claim–support or qualification relation type, and two separate contrasts: relation absent versus correctly available, and equivalent controlled prose versus typed representation. It should include corrupted-link and inert-placebo controls, neutral versus validated framing, explicit selected-subset logging, claim-level final-use lineage, package and surrounding-context hashes, coverage and task-completion gates, blinded evaluation, reliability reporting, equal candidate and selector opportunities, and a declared end-to-end budget with a saved-budget rule.

Do not infer that typed packages, full relational schemas, role separation, or fresh contexts are beneficial from the current evidence. The correct integrative conclusion is that the competing mechanisms are now sufficiently specified to test, while the causal direction remains unresolved.