# External Evidence Researcher — C0004

## Research Scope

This search addressed the narrowed C0004 frontier: methodological evidence relevant to validating a minimal claim–support handoff apparatus at the External Evidence Researcher → Alternative Theorist transition. The search did not ask whether metadata, knowledge graphs, retrieval-augmented generation, multi-agent systems, or structured packages help in general. It asked whether the located primary literature materially resolves the remaining C0004 questions:

1. whether the same claims and evidence have been compared with versus without explicit claim–evidence relations;
2. whether approximately equivalent relation content has been compared in controlled prose versus typed or structured form;
3. whether selection can be recorded before generation and separated from final evidence use;
4. whether correct relations have been compared with corrupted or merely authoritative-looking cues;
5. whether direct support, claim identity, scope, qualification, split/merge lineage, and evidence sufficiency can be annotated reliably;
6. whether relation construction, validation, parsing, selection, generation, and integration costs have been accounted for; and
7. whether any evidence transfers directly to open-ended multi-source synthesis and specifically to evidence-collection → alternative-explanation handoffs.

The main direction is the limited hypothesis that explicit, correct claim–support information can reduce downstream support-reconstruction error. “Supporting” evidence below means evidence consistent with that direction or useful for validating its apparatus. It does not mean that a fixed-compute claim–support effect has been established.

The search located no study that satisfies the full corrected C0004 contrast in the target handoff. The most relevant evidence instead falls into four classes: controlled human-interface studies, fact-verification and attribution studies with observable evidence-selection stages, structured-evidence systems with component ablations, and annotation or evaluation work for evidence relations and information change.

## Search Questions

1. Does any primary study hold claims and evidence constant while adding only explicit claim–support links?
2. Does any primary study compare controlled prose and typed edges while checking semantic, positional, geometric, and token equivalence?
3. Do explicit evidence organizations improve verification, attribution, comprehension, or long-form factual coverage?
4. Do explicit links change trust without changing behavior, or induce compliance with false or superficial authority cues?
5. Can selected evidence be observed before generation, and does good selection guarantee correct final attribution?
6. What existing codebooks distinguish direct support from partial support, qualification, contradiction, contextualization, exemplification, or missing information?
7. What methods track claim identity and information loss across paraphrase, scope changes, and omitted modifiers?
8. Which studies expose equal-token or end-to-end resource controls, and which merely add retrieval, agents, validators, planning, or repeated calls?
9. Is there direct evidence for open-ended multi-source research synthesis or the specific External Evidence Researcher → Alternative Theorist transition?
10. What findings count against the favored direction: null behavioral effects, cue susceptibility, selection–use dissociation, complexity-dependent failures, coverage losses, or evaluator bias?

## Search Method and Source Hierarchy

Searches were restricted to the specific C0004 apparatus questions and began from the accepted C0003 corrected-contrast gap. Priority was given to peer-reviewed conference and journal papers, original author preprints where peer-reviewed publication was unavailable, official benchmark or dataset pages, and original repositories. Search terms combined claim–evidence mapping, evidence attribution, evidence ranking, evidence sufficiency, structured evidence representation, citation bias, corrupted citations, claim identity, scientific paraphrase, long-form report logic, and evidence-tracked report generation.

Fifteen primary sources were retained. Thirteen are peer-reviewed conference or journal papers, one is a peer-reviewed workshop paper, and one is an original-author preprint. No forum, social-media, or secondary-source claim was used as factual confirmation.

Sources were downgraded from direct-effect evidence to apparatus guidance when any of the following held: underlying evidence content changed with the treatment; no relation-absent or equivalent-content comparison existed; selection was inferred only from final output; evaluator format was aligned with the treatment without counterchecks; validation, retrieval, tools, candidates, or compute were bundled; or the task did not distinguish factual assertions from hypotheses and opinions.

## Evidence Supporting the Main Direction

### C0004-EXT-01 — Explicit evidence organization can improve human verification efficiency, but this is not a pure relation-link effect

`C0004-SRC-03` compares incremental evidence ranking with fixed evidence selection in a controlled user study over 100 curated fact-verification claims. Five fluent English-speaking participants with computer-science backgrounds reached a verification decision successfully on 94% of ranked-evidence cases versus 74% of selected-evidence cases, read 2.48 versus 3.85 sentences on average, and were undecided on 5% versus 23%. This supports the narrower proposition that evidence organization and early presentation of complementary support can change evidence uptake and verification efficiency.

The treatment is not “same content without versus with claim–support edges.” Ranking leaves all evidence available sequentially, whereas selection supplies a fixed subset. Ordering, stopping control, visible evidence quantity, and user interaction differ. The study has only five users and short fact-verification claims. It therefore supports geometry, selection, and information-availability mechanisms more directly than an explicit-link mechanism.

### C0004-EXT-02 — Structured relational evidence can reduce comprehension time

`C0004-SRC-13` represents randomized-trial evidence as entities, propositions, and maps. In a small user evaluation using ten RCT abstracts and four domain experts, the EvidenceMap representation reduced comprehension time by 51.9% relative to raw abstracts. The broader corpus contains 229 disease-agnostic and 80 COVID-19 RCT abstracts, 12,725 entities, and 1,602 propositions; reported agreement for evidence-dependency annotation was 0.691.

This is useful apparatus evidence that relational representations can reduce human search burden and preserve many evidence assertions. It is not an equivalent-content prose-versus-typed causal test: the map is shorter, reorganized, visually structured, expert-created, and compared with raw text and other representations. Construction and validation effort are not included in the reading-time comparison.

### C0004-EXT-03 — Curated evidence selection improves attribution quality, showing that the selected-subset checkpoint is consequential

`C0004-SRC-04` uses 100 PolitiHop claims and explicitly separates evidence selection from explanation generation. Human-selected evidence is compared with evidence selected in one shot by GPT-4, GPT-3.5, or Llama-2-7B-chat; the same model family then generates inline-cited explanations. A citation-masking-and-recovery protocol evaluates whether explanation spans can be correctly reattached to evidence. Human-curated evidence produces better attribution, while even the strongest models still make inaccurate attributions.

This supports the C0004 requirement to log the selected subset before generation. It also shows that selection quality matters to final support attribution. However, human and model evidence sets differ in size and content, machine-selected sets tend to be larger, and the same LLM often performs both selection and generation. The study does not isolate an explicit relation marker, and human curation supplies privileged labor.

### C0004-EXT-04 — Evidence selection can causally influence answers and can generalize across readers

`C0004-SRC-06` trains evidence agents to choose passage sentences that most convince a pretrained question-answering model of a designated answer. The selected evidence also changes answer plausibility for other QA models and humans; humans can answer with about 20% of the original passage. This demonstrates that an explicit selected subset is not a passive measurement object. It is a behavioral intervention that changes effective evidence, salience, and reader decisions.

For C0004, this finding supports treating forced selected-subset reporting as a common, costed intervention. It weakens any interpretation of the checkpoint as natural latent retrieval. The study concerns passage QA, uses trained evidence agents and additional optimization, and does not compare relation-present and relation-absent handoffs.

### C0004-EXT-05 — Explicit evidence binding plus mechanized scrutiny can improve provenance-aware fact checking

`C0004-SRC-07` introduces an Evidence Contract requiring debaters to state atomic subclaims and bind each to explicit evidence units, followed by a neutral Scrutinizer that audits outputs and deterministically validates cited identifiers and quoted spans, and a Judge that selects a sufficient evidence set. On open-book FEVEROUS and HOVER, the system improves metrics jointly requiring correct labels and correct, complete evidence. Component ablations indicate that evidence binding and mechanized citation validation both contribute.

This is one of the closest system-level precedents for atomic claims, explicit evidence IDs, selected evidence, and downstream judgment. It supports apparatus feasibility and the potential value of binding when combined with validation. It does not isolate binding from debate roles, scrutiny, deterministic checks, judge selection, extra prompts, or added calls. It is therefore not fixed-compute evidence for a claim–support edge or a fresh-role handoff.

### C0004-EXT-06 — Evidence-tracked long-form generation can improve accuracy and coverage, but all key mechanisms are bundled

`C0004-SRC-08` evaluates EviReport on eight data-rich report topics. The workflow constructs compact traceable evidence units and a knowledge graph, retrieves subgraphs into packages, uses two-stage outlining, extracts facts before drafting, and issues gap-aware append queries. Relative to its reported baselines, it improves factual coverage by 2.16×, factual accuracy by 8.9 points, and visual-evidence integration by 34 points. Removing the knowledge graph reduces the overall coverage score from 0.3963 to 0.1800 and answerable ratio from 0.6100 to 0.3221; removing fact extraction reduces factual accuracy from 0.9687 to 0.8350 and verified fact count from 78.5 to 52.75.

This is direct transfer-relevant evidence that explicit evidence organization, retrieval, planning, and facts-first writing can matter in long-form synthesis. It also reinforces the need to evaluate accuracy and coverage separately. It does not isolate claim–support links, prose versus typed representation, or role boundaries. It adds knowledge-graph construction, retrieval, multiple models, planning, repeated generation, append queries, and multimodal tools. The positive result therefore supports a bundled evidence-workflow direction, not the C0004 estimand.

### C0004-EXT-07 — Semantic selection can add value beyond a token-budget control in a narrow knowledge-graph setting

`C0004-SRC-14` studies FACTKG with 108,675 claims. A reported token-budget comparison finds GPT-4.1-mini semantic filtering at 78.85% accuracy versus a lexical heuristic at 77.54%, while unfiltered truncation-dominated input achieves 52.70%. In a separate 300-claim comparison, explicit knowledge-graph grounding improves GPT-4o-mini and GPT-4.1-mini over claim-only memorization by 12.67 and 9.33 points.

The 1.31-point semantic-filtering advantage over a token-matched lexical heuristic is the closest located evidence that relevance-sensitive selection contributes beyond merely reducing context volume. It does not compare explicit support edges with equivalent unlinked content and does not include end-to-end package construction, validation, or generation accounting. The claim-only comparison adds evidence content and chain-of-thought, so it is not an equal-information relation test.

### C0004-EXT-08 — Evidence completeness and qualifications affect verification

`C0004-SRC-15` creates fluency-preserving constituent- and sentence-level evidence omissions across three fact-checking datasets and three Transformer architectures. Human annotations identify whether omitted content is important. Models detect missing evidence unevenly: reported accuracy is 21% when adverbial modifiers are omitted and 63% for omitted dates. Contrastive self-learning improves evidence-sufficiency prediction by up to 17.8 F1 and fact-checking performance by up to 2.6 F1.

This supports a narrow direct-support codebook that preserves scope and qualifications rather than treating all relevance as binary support. It also shows that apparently fluent evidence can be insufficient after small qualification losses. The intervention is evidence deletion, not explicit relation metadata, and the trained correction procedure adds training and compute.

## Evidence Weakening the Main Direction

### C0004-EXT-09 — A granular claim–evidence interface changed trust but not behavioral reliance

`C0004-SRC-01` is the closest located human-interface comparison to explicit claim–evidence mapping. PaperTrail presents granular claim-level mappings to supporting paper passages and compares them with a baseline using sentence- and source-level citations. In a preregistered within-subjects study, 26 researchers completed a multi-paper synthesis editing task and a devil’s-advocate review task. PaperTrail reduced trust relative to the baseline (`t(25)=2.61`, `p=.015`, `d=.44`), but did not significantly change behavioral reliance measured through normalized token-level edit distance (`p=.313`) or confidence (`p=.525`).

This is adverse evidence against assuming that visible claim–evidence links automatically improve downstream use. It is compatible with a reader-selection or reader-use bottleneck: users noticed or interpreted the richer provenance display without changing their editing behavior. It is not a clean relation-availability test because both conditions include attribution cues, and the mapping interface changes interaction, granularity, display, latency, and cognitive load. Twelve of 38 participants were excluded before analysis for low engagement, gibberish, or latency-related issues, and the final sample came from one research organization.

### C0004-EXT-10 — Citation-looking cues can increase hallucination even when citations are fabricated

`C0004-SRC-02` introduces AuthorityBench, a 220,564-prompt preprint benchmark with a balanced 2×2 design crossing claim veracity and citation veracity across general knowledge, science, law, and medicine, with seven models and forty templates. The authors report that citation presence, including fabricated citations, consistently increases hallucination relative to no citation; fabricated citations attached to true claims increase hallucination by 3–22 percentage points, with larger effects in general knowledge.

This is strong adverse evidence for the authority-cue hypothesis. A relation marker or source ID can act as an endorsement cue rather than a neutral description of support. It does not test claim–support edges, selected evidence, or long-form synthesis, and it is a preprint published in June 2026 rather than peer-reviewed evidence. Citation strings also add tokens and surface form.

### C0004-EXT-11 — Human readers exhibit a small citation-induced belief effect

`C0004-SRC-12` conducts six experiments in which participants rate true and false trivia claims presented with or without in-text citations. A mini meta-analysis reports a small but reliable increase in belief for cited claims (`d=0.13`, 95% CI `[0.06, 0.20]`).

This independently supports the authority-cue mechanism in human readers. It weakens the assumption that an explicit relation or citation is interpreted only after evidence verification. The study concerns trivia judgments, not evidence-rich research synthesis, and the citations do not provide a controlled linked evidence passage. It therefore supports cue susceptibility, not a direct estimate of corrupted claim–support links.

### C0004-EXT-12 — Evidence quality does not reliably predict response quality for complex outputs

`C0004-SRC-05` evaluates attribution on six long-document tasks and five LLMs. Citation generated jointly with the response performs best for large or fine-tuned models, while added retrieval can help smaller prompted models. Evidence quality predicts response quality for simple-response datasets but not for complex responses, where models struggle to provide evidence for complex claims.

This weakens a simple “correct selection leads to correct use” model. Even good evidence may not yield correct complex generation, and the best attribution method depends on model size and tuning. It supports separate selection, final attribution, unsupported extension, and qualification-preservation outcomes. The compared attribution procedures use different process structures and compute, and the tasks are long-document assistance rather than open-ended alternative generation.

### C0004-EXT-13 — Correct selection and explicit citations do not guarantee accurate attribution

`C0004-SRC-04` also supplies direct adverse evidence: even with evidence supplied and inline citation requirements, the strongest tested LLMs produce explanations with inaccurate attributions. Human-curated evidence improves results but does not collapse the remaining generation error. This shows that “selected” and “used correctly” are distinct checkpoints and that final citations are not sufficient evidence of semantic reliance.

### C0004-EXT-14 — Superficial form can mislead evaluators of claim–support quality

`C0004-SRC-09` develops ReportLogic for open-ended deep-research reports, with separate Macro-, Expositional-, and Structural-Logic dimensions. Structural Logic explicitly assesses whether claims have relevant evidence, explicit warrants, and appropriate qualifiers. Its adversarial evaluation finds that off-the-shelf LLM judges are influenced by superficial cues such as verbosity and that reasoning-oriented judges can mask broken support relations.

This weakens any result that relies on one unblinded LLM judge or a format-aligned rubric. A typed relation condition may be easier for an evaluator to parse and can appear better even when support is broken. ReportLogic supplies an evaluation precedent, not an intervention test, and its trained LogicJudge uses synthetic supervision from frontier-model ensembles in addition to human-annotated preference data.

## Evidence About Alternative Explanations

### Relation information versus representation

No retained source directly compares relation-absent content with correct relations while otherwise holding claims, evidence, order, adjacency, prompts, and resources fixed. No source directly compares approximately equivalent relation content in controlled prose and typed edges with semantic-equivalence and residual-format checks. Positive structured-system results therefore remain compatible with added relation information, shorter representations, parsing affordances, or changed reader instructions.

`C0004-SRC-13` and `C0004-SRC-14` indicate that structured or semantically selected evidence can improve efficiency or accuracy, but both change information geometry and processing. `C0004-SRC-05` finds model-dependent preferences among attribution procedures, which argues against a universal representation advantage.

### Geometry, salience, and search burden

`C0004-SRC-03` shows that ordering evidence so sufficient complementary information appears early changes verification success and reading effort. `C0004-SRC-13` shows that maps reduce comprehension time relative to raw abstracts. Both are more directly explained by reduced search burden, adjacency, and compression than by a distinct epistemic interpretation of a support edge.

A C0004 pilot should record position, order, token distance, evidence density, delimiters, visible package length, and stopping opportunity. Merely matching claims and evidence items is insufficient if explicit links move the evidence closer or reduce the search space.

### Authority and validation cues

`C0004-SRC-02` and `C0004-SRC-12` independently show that citation cues can alter model hallucination and human belief. `C0004-SRC-01` shows that provenance granularity can change reported trust without changing behavioral reliance. Together these findings support separating relation correctness from relation appearance and separating perceived validation from verified support use.

A later corrupted-link diagnostic should surface-match plausibility, wording, position, density, and expected correctness. A label such as “validated” would be a distinct intervention unless the validation process and its information are controlled.

### Forced selection as an intervention

`C0004-SRC-06` demonstrates that selected evidence can persuade models and humans. `C0004-SRC-03` demonstrates that a sequential evidence interface changes stopping and verification. `C0004-SRC-04` demonstrates that curated versus model-selected sets change attribution. These sources jointly support the Critic’s correction: requiring a selected-subset object is not passive observation. It can force deliberation, change evidence exposure, and consume resources.

The forced-selection checkpoint should be identical across C0004 conditions, separately costed, and described as observed selection under a forced protocol. A later no-checkpoint comparison would be needed to estimate the checkpoint’s own effect.

### Writer and validator privilege

`C0004-SRC-04` finds an advantage for human-curated evidence. `C0004-SRC-07` adds deterministic citation validation and a neutral scrutinizer. `C0004-SRC-08` adds graph construction, planning, fact extraction, and append-query loops. Positive results from these systems can be caused by privileged correction and validation labor rather than relation representation.

A reference package can remain a separately costed diagnostic upper bound, but gains over ordinary packages cannot be attributed to schema unless writer and validator information, labor, and compute are controlled.

### Reader capability and task complexity

`C0004-SRC-05` finds that attribution approach depends on model scale and fine-tuning, and evidence quality loses predictive power for complex responses. `C0004-SRC-01` finds a trust effect without a behavioral-reliance effect in researchers. `C0004-SRC-04` finds residual attribution errors despite selected evidence. These support a reader-use bottleneck and task × model interaction.

The C0004 apparatus should not infer that a relation was ineffective until it verifies schema parsing, relation recognition, selected-subset validity, and sufficient task ambiguity. A null can reflect treatment collapse, a reader that ignores the format, or a task with relations already obvious from adjacency.

### Coverage, sufficiency, and qualification

`C0004-SRC-08` shows accuracy–coverage tradeoffs among long-form systems and large coverage losses when structured retrieval is removed. `C0004-SRC-15` shows that omission of modifiers can make evidence insufficient while remaining fluent. `C0004-SRC-03` shows that fixed evidence selection can leave users undecided when complementary evidence is missing.

These findings support separate measures for relation-selection recall and precision, final support attribution, factual extensions, scope and qualification preservation, factual coverage, alternative coverage, omission severity, task completion, and usefulness. Lower unsupported-claim counts without these gates remain uninterpretable.

### Evaluator alignment

`C0004-SRC-09` directly shows judge sensitivity to superficial verbosity and broken support relations. `C0004-SRC-04` reports only moderate human–LLM agreement for citation attribution, with evaluator performance varying by generator. Structured output and structured evaluation can share format biases.

The C0004 pilot should use blinded evaluation, separately score schema validity, use more than one evaluator type where feasible, and adjudicate disagreements. A condition should not receive credit merely for reproducing supplied relation IDs.

## Fixed-Compute Versus Added-Compute Evidence

No retained source fully accounts for relation construction, human or model validation, serialization, prompt and context processing, parsing, forced selection, candidate generation, selector opportunities, final generation, evaluation, and saved-budget reallocation while varying only claim–support metadata.

The closest partial resource control is `C0004-SRC-14`, where semantic filtering is compared with a lexical heuristic under a reported token-budget control. The 1.31-point advantage indicates that relevance-sensitive selection can add value beyond equalized retained-token quantity in that FACTKG training setting. It does not account for the filtering model’s inference or construction cost and does not compare linked versus unlinked equivalent content.

`C0004-SRC-01` uses a within-subjects interface comparison, which controls participants and task materials better than cross-system comparisons, but PaperTrail’s preprocessing pipeline, interaction latency, claim extraction, and display complexity differ. Human task time and system inference cost are not an end-to-end matched budget.

`C0004-SRC-03` compares evidence ranking and selection in one interface study, but the ranking and selection algorithms create different evidence exposure and stopping opportunities. LLM ranking, evidence-set construction, and human reading effort are not one equalized compute ledger.

`C0004-SRC-04` explicitly separates selection and generation but changes evidence-set content and size and adds human curation in one condition. `C0004-SRC-06` trains evidence agents. `C0004-SRC-07` adds debate, scrutiny, deterministic validation, and judging. `C0004-SRC-08` adds graph construction, retrieval, two-stage planning, fact extraction, repeated drafting, append queries, and multimodal retrieval. These are added- or differently allocated-compute systems.

`C0004-SRC-13` reports user reading-time savings but does not charge expert annotation, map construction, or pipeline computation against that saving. `C0004-SRC-15` adds contrastive training and tri-training. `C0004-SRC-02` and `C0004-SRC-12` are useful cue controls, but citation-present prompts contain additional surface tokens and do not model package construction.

Consequently, the reviewed evidence supports a resource ledger rather than any fixed-compute superiority claim. A C0004 pilot needs a primary end-to-end budget, tolerance, and saved-budget rule. It should record package construction, relation adjudication, validation, prompt and context tokens, selection output, retries and schema repairs, candidates, final generation, and human evaluation effort by condition.

## Conflicting or Inconclusive Findings

1. **Structured evidence can help, but visible links can fail to change use.** Evidence ranking and EvidenceMap improve verification or comprehension efficiency (`C0004-SRC-03`, `C0004-SRC-13`), while PaperTrail changes trust without significant behavioral reliance (`C0004-SRC-01`).
2. **Evidence binding can improve provenance metrics, but citations can also induce error.** GAVEL reports gains from evidence contracts and mechanized checking (`C0004-SRC-07`), while AuthorityBench and the citation-effect experiments show susceptibility to citation cues (`C0004-SRC-02`, `C0004-SRC-12`).
3. **Selection matters, but correct selection is not sufficient.** Human-curated evidence improves attribution (`C0004-SRC-04`), yet the same study finds inaccurate final attribution, and `C0004-SRC-05` finds weak evidence-quality prediction for complex outputs.
4. **Long-form evidence workflows improve coverage and accuracy, but the causal component is unresolved.** EviReport has strong long-form gains and component ablations (`C0004-SRC-08`), but graph retrieval, planning, facts-first writing, repeated queries, and model specialization remain bundled.
5. **Representation effects are model-dependent.** `C0004-SRC-05` finds citation best for large or fine-tuned models and retrieval useful for smaller prompted models. No universal prose-versus-typed preference is established.
6. **Evaluation feasibility coexists with evaluator fragility.** ReportLogic operationalizes explicit claims, evidence, warrants, and qualifiers (`C0004-SRC-09`), but also finds that ordinary LLM judges can reward superficial form or miss broken support.
7. **Relational schemas can encode qualifications, but annotation remains nontrivial.** SciClaim and EvidenceMap provide relational schemas (`C0004-SRC-10`, `C0004-SRC-13`), while SPICED and insufficient-evidence work show that paraphrase, scope, and small omissions can materially alter meaning (`C0004-SRC-11`, `C0004-SRC-15`).

The combined record is consistent with a conditional relation benefit, a geometry/search benefit, a forced-selection effect, an authority-cue effect, a writer/validator privilege effect, and a reader bottleneck. It does not identify one dominant mechanism.

## Source Reliability and Independence

All fifteen retained items are original research sources. Fourteen have peer-reviewed publication records; `C0004-SRC-02` is an original-author preprint and should be treated as provisional. The strongest human-interface evidence comes from `C0004-SRC-01`, `C0004-SRC-03`, `C0004-SRC-12`, and `C0004-SRC-13`, but their samples and tasks differ substantially. PaperTrail analyzes 26 researchers at one organization; the evidence-ranking study uses five technically trained participants; EvidenceMap uses four domain experts and ten abstracts; the citation-effect paper spans six experiments but uses trivia judgments rather than linked evidence inspection.

The fact-verification system sources are not fully independent replications of a claim–support effect. `C0004-SRC-04`, `C0004-SRC-07`, `C0004-SRC-14`, and `C0004-SRC-15` use related fact-verification problem families and, in some cases, benchmark families such as PolitiHop, FEVEROUS, HOVER, FACTKG, and standard fact-checking datasets. They test different components, but repeated success on related verification benchmarks should not be counted as independent confirmation of a B001 handoff effect.

`C0004-SRC-08` and `C0004-SRC-09` are independently relevant to open-ended long-form reports: one evaluates generation, the other evaluation. Neither manipulates claim–support metadata in isolation. `C0004-SRC-10` and `C0004-SRC-11` are dataset and annotation precedents, not effect estimates. `C0004-SRC-06` is a QA-selection intervention rather than a synthesis handoff. `C0004-SRC-12` supplies an independent cognitive-cue precedent.

The source count is therefore not an independence count. The evidence base is strongest for apparatus requirements and competing mechanisms, weaker for transfer to open-ended synthesis, and absent for the exact corrected C0004 estimand.

## Evidence Gaps

1. No located study holds the same atomic claims, evidence excerpts, source IDs, order, surrounding context, prompts, readers, candidates, selectors, and full resources constant while adding only correct claim–support relations.
2. No located study compares approximately equivalent relation content in controlled prose and typed fields or edges while reporting semantic-equivalence checks and residual differences in tokens, adjacency, position, delimiters, parser affordance, and salience.
3. No located study tests the External Evidence Researcher → Alternative Theorist handoff or an equivalent evidence-collection → alternative-explanation handoff.
4. No located open-ended synthesis study separates factual assertions and source interpretations from hypotheses, objections, speculation, and unresolved questions in its primary unsupported-claim outcome.
5. No located study validates a forced selected-subset object while also estimating the checkpoint’s own behavioral effect against a no-checkpoint condition.
6. No located study jointly records the reference inventory, written package, selected subset, final support attribution, unsupported extension, qualification preservation, and multi-cause lineage through split and merge events.
7. No located study supplies a fully validated direct-support codebook that cleanly excludes partial support, contextualization, exemplification, qualification, contradiction, motivation, and ambiguous many-to-many relations for this handoff.
8. No located correct-versus-corrupted link study surface-matches claim–evidence plausibility, relation density, geometry, wording, expected correctness, and validation framing in an open-ended synthesis task.
9. No located study fully accounts for relation construction, adjudication, validation, parsing, forced selection, candidate generation, final generation, integration, human evaluation, and saved-budget reallocation.
10. No located study shows that a positive metadata effect survives equivalent relation content, neutral framing, blinded evaluation, equal candidates and selectors, coverage and usefulness gates, and full resource accounting.
11. No located study establishes that the selected B001 transition is more sensitive or representative than another stage transition.
12. No located source establishes a residual role-separation or fresh-invocation effect. Even a future claim–support result would not answer that question.

## Source Ledger

### C0004-SRC-01

- **Title:** PaperTrail: A Claim-Evidence Interface for Grounding Provenance in LLM-based Scholarly Q&A
- **Authors or organization:** Anna Martin-Boyle, Cara A. C. Leckey, Martha C. Brown, Harmanpreet Kaur
- **Date:** 2026
- **URL or DOI:** https://doi.org/10.1145/3772318.3791101 ; https://arxiv.org/abs/2602.21045
- **Source type:** Peer-reviewed CHI 2026 human-computer interaction paper; preregistered within-subjects user study
- **Claim supported or weakened:** Supports that granular claim–evidence mapping changes epistemic response; weakens the claim that links automatically improve downstream use because trust decreased but behavioral reliance and confidence did not significantly change.
- **Study design and sample:** 26 analyzed researchers from one research organization; multi-paper synthesis editing and devil’s-advocate review tasks; PaperTrail compared with sentence/source citation baseline; interface order counterbalanced.
- **Important limitations:** Twelve of 38 participants excluded before analysis; single organization and session; time pressure, latency, and interface complexity; both conditions contain attribution; preprocessing and display changes are bundled; no fixed-compute ledger.

### C0004-SRC-02

- **Title:** Authority, Truth, and Citation Bias: A Large-Scale Multi-Domain Benchmark for Studying Epistemic Susceptibility in Large Language Models
- **Authors or organization:** Aryan Khurana, Aravind Ramana RN, Dhruv Kumar
- **Date:** 11 June 2026
- **URL or DOI:** https://arxiv.org/abs/2606.13104
- **Source type:** Original-author preprint and benchmark paper
- **Claim supported or weakened:** Strongly supports the authority-cue alternative and weakens a benign interpretation of citation or relation markers; fabricated citation cues can increase hallucination.
- **Study design and sample:** 220,564 prompts; balanced 2×2 claim-veracity × citation-veracity design; seven models, forty prompt templates, four domains, and prestige/demographic variations.
- **Important limitations:** Not peer reviewed; citation strings are not linked evidence passages or claim–support edges; prompt lengths differ; no long-form synthesis or selected-subset stage.

### C0004-SRC-03

- **Title:** User-Centric Evidence Ranking for Attribution and Fact Verification
- **Authors or organization:** Guy Alt, Eran Hirsch, Serwar Basch, Ido Dagan, Oren Glickman
- **Date:** March 2026
- **URL or DOI:** https://aclanthology.org/2026.eacl-long.340/ ; https://doi.org/10.18653/v1/2026.eacl-long.340
- **Source type:** Peer-reviewed EACL 2026 paper with benchmark and controlled user study
- **Claim supported or weakened:** Supports that evidence ordering, complementary coverage, and user-controlled stopping improve verification and reduce reading effort; also supports geometry and selection as alternatives to relation semantics.
- **Study design and sample:** Unified benchmark aggregated from existing fact-verification datasets; user study with five fluent English-speaking participants with computer-science backgrounds over 100 curated claims; incremental LLM evidence ranking compared with LLM evidence selection.
- **Important limitations:** Very small user sample; short verification claims; ranking and selection expose different amounts and order of evidence; not a link-present comparison; algorithm and reading costs are not an equal end-to-end budget.

### C0004-SRC-04

- **Title:** Evaluating Evidence Attribution in Generated Fact Checking Explanations
- **Authors or organization:** Rui Xing, Timothy Baldwin, Jey Han Lau
- **Date:** April 2025
- **URL or DOI:** https://aclanthology.org/2025.naacl-long.282/ ; https://doi.org/10.18653/v1/2025.naacl-long.282
- **Source type:** Peer-reviewed NAACL 2025 paper
- **Claim supported or weakened:** Supports separate selected-evidence and final-attribution checkpoints; supports human-curated selection; weakens the claim that selection or citation presence guarantees correct semantic use.
- **Study design and sample:** 100 PolitiHop claims; human-selected versus one-shot model-selected evidence; GPT-4-0613, GPT-3.5-turbo, and Llama-2-7B-chat selection and generation conditions; citation masking and recovery with human and automatic evaluation.
- **Important limitations:** Evidence-set content and size differ; machine sets tend to be larger; same model can select and generate; human curation adds privilege; only attribution, not complete factuality, is measured; no fixed-compute relation contrast.

### C0004-SRC-05

- **Title:** Attribute or Abstain: Large Language Models as Long Document Assistants
- **Authors or organization:** Jan Buchmann, Xiao Liu, Iryna Gurevych
- **Date:** November 2024
- **URL or DOI:** https://aclanthology.org/2024.emnlp-main.463/ ; https://doi.org/10.18653/v1/2024.emnlp-main.463
- **Source type:** Peer-reviewed EMNLP 2024 paper and LAB benchmark
- **Claim supported or weakened:** Supports attribution as a distinct measurable outcome and model-dependent process; weakens a simple selection→correct-use assumption for complex claims.
- **Study design and sample:** Six long-document tasks; five LLMs of different sizes; compares post-hoc attribution, retrieve-then-read, and joint citation approaches.
- **Important limitations:** Procedures use different calls and compute; no equivalent prose-versus-typed test; complex task family is not alternative-theory generation; evidence quality is not a complete measure of final factuality.

### C0004-SRC-06

- **Title:** Finding Generalizable Evidence by Learning to Convince Q&A Models
- **Authors or organization:** Ethan Perez, Siddharth Karamcheti, Rob Fergus, Jason Weston, Douwe Kiela, Kyunghyun Cho
- **Date:** November 2019
- **URL or DOI:** https://aclanthology.org/D19-1244/ ; https://doi.org/10.18653/v1/D19-1244
- **Source type:** Peer-reviewed EMNLP-IJCNLP 2019 paper
- **Claim supported or weakened:** Supports that selected evidence changes model and human decisions and can generalize across readers; establishes that selection is an intervention, not neutral logging.
- **Study design and sample:** Trained evidence agents select passage sentences to support designated QA answers; transfer evaluated with other QA models and humans.
- **Important limitations:** Passage QA rather than synthesis; selection is optimized to persuade; additional training and inference; no claim–support metadata or fixed handoff.

### C0004-SRC-07

- **Title:** GAVEL: Evidence-Contract Debate with Mechanized Scrutiny for Provenance-Grounded Fact-Checking
- **Authors or organization:** Ruoyu Xu, Gaoxiang Li, Victor S. Sheng
- **Date:** July 2026
- **URL or DOI:** https://aclanthology.org/2026.findings-acl.1789/ ; https://doi.org/10.18653/v1/2026.findings-acl.1789
- **Source type:** Peer-reviewed Findings of ACL 2026 paper
- **Claim supported or weakened:** Supports feasibility and possible value of atomic subclaim–evidence binding plus explicit selected evidence and validation.
- **Study design and sample:** Open-book FEVEROUS and HOVER; multi-agent debaters, Evidence Contract, neutral Scrutinizer with deterministic identifier/span checks, and Judge; component ablations.
- **Important limitations:** Evidence binding is bundled with debate, scrutiny, deterministic validation, and judging; added calls and roles; benchmark-family transfer limits; no equal-compute typed-link estimate.

### C0004-SRC-08

- **Title:** EviReport: From Reasoned Outlines to Evidence Tracked Long-Form Reports
- **Authors or organization:** Zihan Liu, Jianhui Li, Zexing Wang, Fei Sun, Jingjing Li, Zheyuan Li, Ke Xiang, Hang Cui, Houhua Gong, Changhua Pei, Gaogang Xie
- **Date:** July 2026
- **URL or DOI:** https://aclanthology.org/2026.findings-acl.1397/ ; https://doi.org/10.18653/v1/2026.findings-acl.1397
- **Source type:** Peer-reviewed Findings of ACL 2026 long-form generation paper
- **Claim supported or weakened:** Supports transfer relevance of evidence packaging, facts-first writing, and separate accuracy/coverage outcomes; does not isolate claim–support links.
- **Study design and sample:** Eight data-rich indicator-report topics; knowledge-graph evidence organization, subgraph retrieval, two-stage outlining, fact extraction, drafting, append queries, and multimodal retrieval; component ablations.
- **Important limitations:** Small topic count; SDG-style report domain; many bundled components and models; substantial added compute; proprietary/heterogeneous baselines for some comparisons; no equivalent-content relation test.

### C0004-SRC-09

- **Title:** ReportLogic: Evaluating Logical Quality in Deep Research Reports
- **Authors or organization:** Jujia Zhao, Zhaoxin Huan, Zihan Wang, Xiaolu Zhang, Jun Zhou, Suzan Verberne, Zhaochun Ren
- **Date:** July 2026
- **URL or DOI:** https://aclanthology.org/2026.acl-long.384/ ; https://doi.org/10.18653/v1/2026.acl-long.384
- **Source type:** Peer-reviewed ACL 2026 benchmark and evaluator paper
- **Claim supported or weakened:** Supports explicit claim–support, warrant, and qualifier scoring for long-form reports; weakens reliance on unblinded LLM judging because superficial form can mask broken support.
- **Study design and sample:** Deep-research, Zhihu, and Quora report-pair sources; human rubric-guided preferences; sixteen frontier LLM judges; trained LogicJudge; adversarial logical and surface-cue perturbations.
- **Important limitations:** Evaluates report logic rather than generation intervention; human and distilled supervision are mixed; some query sources are community platforms; does not validate C0004 claim identity or lineage codebook.

### C0004-SRC-10

- **Title:** Extracting Fine-Grained Knowledge Graphs of Scientific Claims: Dataset and Transformer-Based Results
- **Authors or organization:** Ian Magnusson, Scott Friedman
- **Date:** November 2021
- **URL or DOI:** https://aclanthology.org/2021.emnlp-main.381/ ; https://doi.org/10.18653/v1/2021.emnlp-main.381
- **Source type:** Peer-reviewed EMNLP 2021 dataset and extraction paper
- **Claim supported or weakened:** Supports feasibility of a relation codebook that includes causal, comparative, predictive, statistical, and proportional relations with qualifications, subtypes, and evidence.
- **Study design and sample:** SciClaim corpus drawn from social and behavioral science, PubMed, and CORD-19 papers; 12,738 labels; joint entity and relation extraction experiments.
- **Important limitations:** Scientific-claim extraction rather than direct claim–support handoff; schema is broader than a narrow direct-support relation; no downstream relation-use or fixed-compute effect.

### C0004-SRC-11

- **Title:** Modeling Information Change in Science Communication with Semantically Matched Paraphrases
- **Authors or organization:** Dustin Wright, Jiaxin Pei, David Jurgens, Isabelle Augenstein
- **Date:** December 2022
- **URL or DOI:** https://aclanthology.org/2022.emnlp-main.117/ ; https://doi.org/10.18653/v1/2022.emnlp-main.117
- **Source type:** Peer-reviewed EMNLP 2022 dataset and modeling paper
- **Claim supported or weakened:** Supports annotation of claim identity and degree of information change across paraphrase; relevant to scope change, qualification weakening, and derived reformulation.
- **Study design and sample:** SPICED contains 6,000 scientific-finding pairs from full papers, news, and social-media discussions; models evaluated for information-change prediction and downstream evidence retrieval.
- **Important limitations:** Does not track complete split/merge lineage or direct support edges; cross-medium communication differs from staged research handoffs; downstream retrieval gains are not a relation-metadata effect.

### C0004-SRC-12

- **Title:** The Citation Effect: In-Text Citations Moderately Increase Belief in Trivia Claims
- **Authors or organization:** Matt S. McGlone, Kevin A. Bell, Jessica Zaitchik
- **Date:** 2017
- **URL or DOI:** https://doi.org/10.1016/j.actpsy.2017.07.010
- **Source type:** Peer-reviewed Acta Psychologica paper; six human experiments
- **Claim supported or weakened:** Supports authority-cue compliance and weakens the assumption that citations are neutral pointers evaluated only through their evidence.
- **Study design and sample:** Participants rated true and false trivia claims presented with versus without in-text citations; six experiments; mini meta-analysis reports `d=0.13`.
- **Important limitations:** Trivia belief rather than evidence-rich verification; citations are not explicit linked excerpts; human rather than model readers; does not distinguish accurate and corrupted claim–support relations.

### C0004-SRC-13

- **Title:** EvidenceMap: A Three-Level Knowledge Representation for Medical Evidence Computation and Comprehension
- **Authors or organization:** Tian Kang, Yingcheng Sun, Jae Hyun Kim, Casey Ta, Nicholas M. Volpe, Matthew White, Adler Perotte, Yifan Peng, Chunhua Weng
- **Date:** 15 March 2023
- **URL or DOI:** https://doi.org/10.1093/jamia/ocad036
- **Source type:** Peer-reviewed Journal of the American Medical Informatics Association paper
- **Claim supported or weakened:** Supports relational evidence representation and reduced comprehension time; supports explicit dependency annotation as apparatus precedent.
- **Study design and sample:** 229 general and 80 COVID-19 RCT abstracts; 12,725 entities and 1,602 propositions; four-domain-expert user evaluation on ten abstracts; dependency agreement 0.691.
- **Important limitations:** Tiny user study; expert-created maps; raw text and maps differ in compression, layout, and geometry; construction cost omitted from reading-time comparison; medical RCT evidence may not transfer.

### C0004-SRC-14

- **Title:** Evidence Grounding vs. Memorization: Why Neural Semantics Matter for Knowledge Graph Fact Verification
- **Authors or organization:** Ankit Kumar Upadhyay, John S. Erickson, Deborah L. McGuinness
- **Date:** March 2026
- **URL or DOI:** https://aclanthology.org/2026.fever-1.3/ ; https://doi.org/10.18653/v1/2026.fever-1.3
- **Source type:** Peer-reviewed FEVER 2026 workshop paper
- **Claim supported or weakened:** Supports semantic evidence selection beyond retained-token quantity in one budget-matched comparison and supports explicit KG grounding over claim-only memorization.
- **Study design and sample:** FACTKG with 108,675 claims; symbolic, neural, and LLM comparisons; GPT-4.1-mini semantic filtering versus lexical token-budget heuristic; 300-claim grounded-versus-claim-only LLM test.
- **Important limitations:** Workshop evidence; filter construction cost not fully accounted; lexical and semantic inputs are not equivalent relation representations; claim-only comparison adds evidence and chain-of-thought; no long-form handoff.

### C0004-SRC-15

- **Title:** Fact Checking with Insufficient Evidence
- **Authors or organization:** Pepa Atanasova, Jakob Grue Simonsen, Christina Lioma, Isabelle Augenstein
- **Date:** 27 July 2022
- **URL or DOI:** https://aclanthology.org/2022.tacl-1.43/ ; https://doi.org/10.1162/tacl_a_00486
- **Source type:** Peer-reviewed Transactions of the Association for Computational Linguistics paper
- **Claim supported or weakened:** Supports evidence-sufficiency and qualification-preservation measurement; shows that small omissions can leave fluent but insufficient evidence.
- **Study design and sample:** Three Transformer architectures and three fact-checking datasets; constituent- and sentence-level fluency-preserving omissions; human importance annotations; contrastive self-learning and tri-training.
- **Important limitations:** Evidence deletion rather than explicit support links; trained intervention changes model and compute; fact-verification classification rather than alternative-explanation generation; no complete split/merge lineage.

## Handoff to Alternative Theorist and Integrator

1. The corrected C0003 direct-evidence gap persists. No located source estimates the C0004 relation-availability or representation contrast in the target handoff under matched full resources.
2. The strongest support is indirect and mechanism-bundled: evidence ranking, structured maps, curated selection, evidence contracts, knowledge-graph retrieval, and facts-first long-form generation can improve verification, comprehension, attribution, coverage, or accuracy in their own settings.
3. The strongest adverse evidence is that claim-level provenance may change trust without changing behavioral reliance, citations can induce belief or model hallucination, and selected evidence does not guarantee correct final attribution.
4. The forced selected-subset checkpoint should remain a common, costed intervention. The literature shows that selection and evidence presentation alter behavior; it is not neutral measurement.
5. Apparatus validation should prioritize a narrow direct-support codebook, claim and evidence identity, manipulation uptake, semantic-equivalence checks, geometry recording, selected-subset validity, final support attribution, qualification preservation, epistemic typing, coverage, omission, evaluator reliability, and a complete resource ledger.
6. A first pilot should not authorize claims about typed-field superiority, stage sensitivity, fresh roles, or the full loop. A reliable null or harm after a successful manipulation, prose matching typed form, correct selection without improved final attribution, reduced coverage or usefulness, or cue susceptibility should count as evidence against the favored interpretation.
7. The Alternative Theorist should treat geometry/search reduction, authority cues, forced deliberation, writer/validator privilege, reader capability, task complexity, evidence sufficiency, and evaluator alignment as live explanations. The Integrator should preserve the distinction between direct effect evidence, transfer-relevant system evidence, and apparatus guidance.
