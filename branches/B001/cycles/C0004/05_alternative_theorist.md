# Alternative Theorist — C0004

## Strongest Current Interpretation

The strongest current interpretation is a **conditional relation-information account**, not a claim of established benefit.

**Core interpretation:** Supplying a correct, explicit claim–support relation may reduce the downstream need to reconstruct which evidence supports which factual claim. The effect should be most likely when evidence is dispersed, several items are plausible candidates, qualifications are easy to lose, or the receiving role must transform evidence into competing explanations while preserving source boundaries.

**Proposed mechanism:** The relation provides substantive information that narrows the support search space. It may alter which evidence the Alternative Theorist selects, make support attribution more accurate, reduce unsupported factual extensions, and preserve scope or qualification.

**Current support:** `C0004-EXT-01` through `C0004-EXT-08` provide indirect evidence that evidence organization, relational maps, curated selection, explicit binding, structured retrieval, facts-first generation, semantic filtering, and evidence sufficiency can matter in their own settings. `C0004-EXT-03` and `C0004-EXT-13` especially support separating selected evidence from correct final attribution. The accepted internal record also supports a write–select–use decomposition and separate availability and representation estimands.

**Current limitation:** No located study tests the corrected relation-availability or equivalent-content representation contrast in the target handoff under matched prompts, geometry, candidates, selectors, evaluation, and full resources. Positive systems bundle relation information with ordering, compression, curation, validation, retrieval, prompts, repeated calls, or specialized models. The strongest current interpretation is therefore an experimentally justified hypothesis, not an evidence-backed effect estimate.

## Alternative Theory 1

### C0004-ALT-01 — Geometry and search-burden account

- **Core claim:** Apparent benefits from explicit claim–support relations may arise mainly because the treatment changes information geometry and reduces search burden, not because the reader represents or reasons over a distinct epistemic support relation.
- **Status:** Evidence-backed alternative mechanism hypothesis. It is supported indirectly, not established for the B001 handoff.

### Mechanism

A relation-present package may move claims and evidence closer together, shorten the effective package, make relevant evidence appear earlier, reduce the number of candidate passages, add delimiters, create repeated identifiers, or make stopping easier. These changes can improve effective access even if the reader does not interpret the link as a support relation. Typed fields may also be easier for a particular model to parse than controlled prose, while another model may prefer prose.

### Evidence it explains

- `C0004-EXT-01`: ranked evidence improved verification success and reduced reading, but ordering, stopping, visible evidence quantity, and interaction changed.
- `C0004-EXT-02`: EvidenceMap reduced comprehension time, while also compressing and reorganizing the source material.
- `C0004-EXT-07`: semantic filtering outperformed a token-budget lexical heuristic in a narrow setting, supporting relevance-sensitive selection beyond raw retained-token quantity, but not a distinct support-edge effect.
- `C0004-EXT-12`: attribution procedures perform differently by model scale and tuning, consistent with format and reader-capability interactions rather than a universal representation advantage.
- The accepted `C0003-INTG-03` and `C0003-INTG-05` already treat serialization, position, adjacency, salience, and reader format familiarity as live mechanisms.

### Evidence it struggles with

This account would struggle with a result in which:

1. relation content improves final support attribution after adjacency, order, token distance, delimiters, package length, and reader instructions are closely matched;
2. neutral controlled prose and typed relations both outperform a relation-absent condition by similar amounts despite different surface forms;
3. the reader can explicitly identify and correctly apply the relation while geometry is experimentally varied without changing the effect; or
4. correct links help while surface-matched corrupted links are rejected rather than followed.

`C0004-EXT-05` is also harder to explain solely through geometry because explicit evidence binding contributed within a larger mechanized system, although binding remained bundled with scrutiny, validation, and judging.

### Predictions

- Effects will shrink substantially when adjacency, order, token distance, package length, delimiters, and visible evidence quantity are matched.
- Reordering or separating linked items will reduce the apparent benefit even when the relation content is unchanged.
- Compact controlled prose may match typed fields when it provides the same relation content at the same location.
- Effects will vary by reader model, parser reliability, context length, and package density.
- Improvements will appear first in selection speed or selection accuracy and need not propagate to correct final attribution.

## Alternative Theory 2

### C0004-ALT-02 — Authority-cue compliance account

- **Core claim:** A claim–support marker may operate as an endorsement or validation cue. Correct links can improve outputs because the reader follows them, but the same mechanism can propagate false links without genuine evidence verification.
- **Status:** Evidence-backed adverse mechanism hypothesis. Direct transfer to claim–support edges in the target handoff remains untested.

### Mechanism

Source IDs, citations, typed edges, labels such as “supports,” and validation-looking formatting can increase perceived credibility or reduce the perceived need to inspect the evidence. The reader may treat the relation as an instruction about what to trust rather than a descriptive object to verify. When links are correct, this can mimic a reasoning benefit. When links are wrong, it can create supported-looking factual errors and amplify package mistakes.

### Evidence it explains

- `C0004-EXT-09`: PaperTrail’s granular provenance changed reported trust without significantly changing behavioral reliance or confidence. This shows that provenance display can alter epistemic response without corresponding use.
- `C0004-EXT-10`: fabricated citations increased hallucination in the reported benchmark, supporting citation-induced model susceptibility.
- `C0004-EXT-11`: human participants showed a small but reliable citation-induced belief effect.
- `C0004-EXT-14`: evaluators can be influenced by superficial form and can miss broken support relations, allowing treatment-aligned outputs to look better without better reasoning.
- The accepted authority-cue and evaluator-alignment hypotheses from C0003 fit this account.

### Evidence it struggles with

This account would struggle with evidence that readers:

1. benefit from neutrally framed relation content without validation language or citation prestige;
2. reject plausible, surface-matched corrupted links at substantially higher rates than correct links;
3. independently inspect the linked evidence and preserve its scope and qualifications rather than merely copying the relation;
4. show improved support attribution without increased trust or compliance measures; or
5. retain the benefit when evaluator format is blinded and relation identifiers are removed from the final output.

It also does not by itself explain why evidence ranking or relational compression can reduce search time when no authority claim is made.

### Predictions

- Correct and corrupted relation markers will both increase selection or citation of linked items relative to relation-absent packages.
- Labels implying validation will increase compliance more than neutral descriptive links.
- The effect will be larger when the underlying evidence is difficult to inspect, the reader is under resource pressure, or the relation marker resembles an evaluator-preferred format.
- Trust or confidence may change without a corresponding improvement in final factual support.
- Blinded evaluation and removal of relation IDs from final answers will reduce apparent gains caused by evaluator alignment.

## Additional Alternative or Null Explanation

### C0004-ALT-03 — Apparatus-induced deliberation and selection account

- **Core claim:** Any observed benefit may be caused by the forced selected-subset checkpoint, stronger prompts, extra validation, repeated sampling, or better allocation of compute rather than relation information itself.
- **Status:** Evidence-backed apparatus explanation.

The selected-subset object is not passive measurement. `C0004-EXT-04` shows that selected evidence can causally change model and human answers. `C0004-EXT-01`, `C0004-EXT-03`, and `C0004-EXT-13` show that evidence presentation and curation affect outcomes, while correct selection does not guarantee correct final use. A forced selection step can make the reader review evidence, externalize a plan, reduce omission, or consume tokens that would otherwise be used for alternative generation. Stronger relation-seeking prompts can similarly add reasoning steps. Human or model validation can repair the package before the Alternative Theorist sees it. Extra candidate generation or selection can improve the best retained output without any role-separation effect.

This account predicts that the advantage will diminish when both relation-present and relation-absent conditions receive the same forced-selection procedure, prompt strength, candidate count, selector opportunity, validation, and end-to-end budget. It also predicts that a no-checkpoint condition may perform worse in both arms, showing that the checkpoint itself—not the relation—is the active intervention.

### C0004-ALT-04 — Reader-bottleneck or minimal null

- **Core claim:** After successful manipulation and full controls, explicit claim–support relations may have no stable average downstream benefit in this handoff.
- **Status:** Plausible null hypothesis, not established.

A null can arise because the underlying claims and evidence are already adjacent or obvious, the reader ignores the schema, the task lacks enough relation ambiguity, correct selection fails to improve complex generation, or positive and negative effects cancel across task and model strata. `C0004-EXT-09`, `C0004-EXT-12`, and `C0004-EXT-13` are compatible with this possibility. A reliable null would not prove that relations never matter; it would bound the effect for the tested reader, task set, relation density, package size, and resource rule.

A minimal null must be distinguished from treatment collapse. Equality is uninformative if readers cannot parse the schema, relation content is redundant, tasks are insensitive, annotation reliability is weak, or opposing subgroup effects are averaged together.

### Selection effects, reporting bias, and role-separation misattribution

The available evidence also permits a selection-and-reporting account. Positive systems may receive more calls, longer context, repeated sampling, better prompts, specialized models, human curation, deterministic validators, or a selector that reports the best candidate. Studies and branch narratives may emphasize successful workflows while underreporting failed prompts, schema repairs, discarded candidates, or coverage losses. None of these mechanisms establishes that fresh roles or role separation caused the gain. The same scaffolding may be implementable in a persistent single-model workflow.

## Hybrid Explanations

The strongest realistic account may be hybrid rather than exclusive.

1. **Relation information + geometry:** Correct links add useful information and simultaneously move evidence into a more usable arrangement. Both can contribute.
2. **Relation information + forced selection:** Links change which items are selected, while the checkpoint forces deliberation. The checkpoint may amplify a real but smaller relation effect.
3. **Geometry + authority cue:** Compact typed links can be easier to parse and appear more authoritative. Correctness may improve when the cue is right and deteriorate when it is wrong.
4. **Writer privilege + reader bottleneck:** Better curation creates a higher-quality package, but the reader still introduces unsupported extensions during complex generation.
5. **Task × model × representation:** Typed relations may help some readers and harm others; prose may be superior when format familiarity differs.
6. **Coverage–noise interaction:** Increasing correct relation coverage can recover dispersed support while additional or erroneous links increase clutter, false dependencies, and compliance risk.
7. **Verification bundle:** Explicit binding may become useful only when combined with deterministic identifier checks, qualification-preserving rules, and a competent final verifier, as suggested by `C0004-EXT-05`.

These combinations mean that a positive average result need not identify a single mechanism, and a null average can conceal offsetting benefits and harms.

## False Dichotomies or Framing Problems

- **“Relations help” versus “relations do not help.”** Effects may reverse by task ambiguity, reader model, relation density, evidence dispersion, and qualification burden.
- **Semantic relation versus formatting.** Availability, representation, geometry, prompts, parsing, and authority cues are separable but interacting factors.
- **Selection versus use.** A reader can select correct evidence and misuse it, ignore a supplied link and reconstruct support correctly, or cite an item without semantically relying on it.
- **Accurate versus unsupported output.** Lower unsupported-claim counts can reflect fewer claims, fewer alternatives, lower specificity, reduced coverage, or task failure.
- **Role separation versus single-agent prompting.** Structured generation, challenge, selection, validation, and integration can be implemented with or without fresh conversation boundaries. A package effect would not establish a fresh-role effect.
- **Human curation versus schema value.** A reference package can show an upper bound while bundling privileged information, correction, adjudication, and labor.
- **Null versus no mechanism.** A null can reflect genuine zero effect, weak manipulation, reader non-use, task insensitivity, low reliability, or offsetting subgroup effects.
- **Correct link versus corrupted link.** A corrupted-link test does not isolate authority cues unless plausibility, wording, geometry, density, and expected correctness are matched.
- **More context versus better context.** Full context may preserve dependencies while burying them; compact packages may foreground support while deleting qualifications.

## Discriminating Tests

1. **Manipulation validation before effectiveness testing.** Verify that the relation-present condition contains the intended direct-support information, readers can parse and restate it, relation-absent packages do not accidentally encode the same link, and semantic-equivalence judgments meet a predeclared reliability threshold.

2. **Separate availability and representation contrasts.** First compare relation absent versus neutrally stated correct relation content. Separately compare controlled prose versus typed fields carrying approximately equivalent content. Do not pool the two effects.

3. **Geometry-controlled comparison.** Match or record adjacency, order, token distance, delimiters, package length, visible evidence quantity, and stopping opportunity. Then perturb geometry while holding relation content fixed. A stable effect supports relation information; a geometry-sensitive effect supports `C0004-ALT-01`.

4. **Neutral versus authority-framed relations.** Compare a neutral descriptive link with an otherwise matched “validated” or endorsement-like link. Add plausible, surface-matched corrupted relations only after the minimal apparatus is reliable. Similar compliance with correct and corrupted links supports `C0004-ALT-02`.

5. **Checkpoint factorial.** Cross relation presence with forced selected-subset reporting. This estimates whether the checkpoint produces improvement independently or amplifies the relation. Cost the checkpoint and hold its schema constant.

6. **Selection-to-use lineage.** Record the reference inventory, written package, selected subset, final support attribution, unsupported extension, qualification preservation, and epistemic status. Distinguish selection recall and precision from correct final semantic use.

7. **Role-aligned outcome coding.** Score factual assertions and source-attribution claims separately from hypotheses, speculation, objections, and unresolved questions. Require correct epistemic typing, alternative coverage, factual coverage, omission severity, usefulness, and task completion.

8. **Prompt and sampling controls.** Equalize prompt strength, reasoning instructions, candidate count, retries, schema repairs, selector opportunities, and final integration. Reallocate any saved budget by a predeclared rule rather than allowing one condition to keep an unspent advantage.

9. **Writer and validator controls.** Use the same underlying claims and evidence, log all package-construction changes, and separate ordinary package generation from a separately costed validated reference package. Do not attribute reference-package gains to schema.

10. **Reader and task stratification.** Predeclare strata for relation ambiguity, evidence dispersion, qualification density, package length, and reader model. A true conditional relation effect should concentrate in tasks where reconstruction is nontrivial, not appear only in one post hoc subset.

11. **Blinded and format-robust evaluation.** Remove treatment identifiers from final outputs, blind evaluators, use multiple evaluator types where feasible, separately score schema compliance, and adjudicate disagreements. This tests evaluator-alignment explanations.

12. **Residual role-boundary test only later.** After the apparatus and resource accounting are reliable, hold package, prompts, access, candidates, selectors, and full resources constant while varying a genuinely defined boundary property. Until then, no result should be interpreted as evidence for fresh roles.

## Comparative Evidence Table

| Theory | Evidential status | Explains well | Struggles to explain | Key discriminator |
|---|---|---|---|---|
| Conditional relation-information benefit | Experimentally justified but unestimated hypothesis | Why explicit correct links may reduce reconstruction and improve support preservation | Trust-only effects, corrupted-cue susceptibility, residual generation errors, bundled compute | Benefit survives geometry, prompt, checkpoint, evaluator, and resource controls |
| Geometry and search-burden account (`C0004-ALT-01`) | Indirectly evidence-backed | Ranking, maps, compression, earlier evidence, model-dependent format effects | Correct-link-specific gains under matched geometry | Vary geometry while holding relation content fixed |
| Authority-cue compliance (`C0004-ALT-02`) | Evidence-backed risk mechanism | Citation-induced belief or hallucination, trust changes, evaluator format bias | Neutral-link benefits with active evidence verification | Plausibility-matched correct versus corrupted links; neutral versus validated framing |
| Apparatus-induced deliberation and selection (`C0004-ALT-03`) | Evidence-backed apparatus explanation | Benefits from forced selection, stronger prompts, curation, validation, extra calls or candidates | Relation effect that remains with identical apparatus and full budget matching | Relation × checkpoint factorial with full resource ledger |
| Reader-bottleneck or minimal null (`C0004-ALT-04`) | Plausible, unresolved null | No behavioral change, correct selection without correct use, complex-generation failures | Reliable positive effect after successful manipulation across readers and tasks | Manipulation-validated null with adequate power and predeclared strata |
| Hybrid account | Most plausible broad conceptual structure, not estimated | Mixed positive, null, and adverse findings across systems and readers | A clean single-mechanism effect | Multifactor sequence after minimum apparatus validation |

## Remaining Uncertainty

The central uncertainty is not merely whether explicit relations help. It is whether the branch can create a reliable object called a narrow direct-support relation, preserve claim and evidence identity, observe forced selection without confusing it with natural retrieval, distinguish final citation from semantic use, and evaluate Alternative Theorist outputs without penalizing legitimate hypotheses.

The allowed internal record does not establish that this handoff contains enough stable direct-support pairs for measurement. The external record contains no exact target contrast and no full resource match. It remains unknown whether claim–support is a better first relation than claim–qualification, whether controlled prose and typed fields can be made approximately equivalent, whether corrupted controls can be plausibility-matched, and whether any effect transfers beyond the tested reader, task set, package size, or stage.

No available theory is yet adequate as a sole explanation. The evidence most strongly supports treating relation information, geometry, authority cues, forced selection, reader capability, curation, validation, coverage, and compute as jointly active possibilities.

## Handoff to Integrator

Preserve the strongest current interpretation as a conditional hypothesis only. C0004 should authorize apparatus validation, not an effectiveness conclusion. The Integrator should retain at least four competing explanations: geometry/search reduction, authority-cue compliance, apparatus-induced deliberation and selection, and a reader-bottleneck null. It should explicitly state that more compute, longer or better-positioned context, stronger prompts, repeated sampling, curation, selector quality, validation, and reporting choices can mimic a role or relation benefit.

The next accepted direction should require: a narrow direct-support codebook; separate availability and representation estimands; a common costed selected-subset protocol; role-aligned epistemic scoring; coverage and usefulness gates; blinded evaluation; and a complete end-to-end resource ledger. A positive result should count as evidence for relation information only if it survives geometry, authority, checkpoint, prompt, sampling, selection, writer/validator, evaluator, and budget controls. A null should be interpreted only after manipulation uptake, reader parsing, task sensitivity, and annotation reliability are demonstrated. No C0004 result should be used to infer typed-package superiority, stage sensitivity, fresh-role value, or full-loop superiority.