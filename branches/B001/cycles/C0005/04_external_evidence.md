# External Evidence Researcher — C0005

## Research Scope

This report addresses the corrected C0005 frontier as a **method-design and measurability search**. It asks whether a prospective apparatus for the External Evidence Researcher → Alternative Theorist handoff can define, annotate, and audit narrowly bounded direct claim–support relations and observable downstream relation-preserving incorporation.

The report does not test whether relation metadata improves performance, whether typed representation is superior to controlled prose, whether the selected handoff is uniquely sensitive, or whether role separation or fresh invocation is beneficial. It also does not treat final-text correspondence, citation presence, recorded selection, or rationale generation as evidence of latent causal reliance.

Sixteen primary sources were retained. No retained source studies the exact B001 handoff, and no source supplies a branch-specific pass threshold.

## Search Questions

1. What operational rules have primary studies used to define atomic claims, direct support, refutation, insufficient evidence, and evidence-unit boundaries?
2. When do support decisions require sentence context, multiple sentences, multiple paragraphs, tables, or full-source access rather than a locator or source-level citation?
3. What designs separate annotation development, independent verification, adjudication, and held-out evaluation?
4. How can downstream relation-preserving incorporation be scored from observable output content, attribution, scope, qualification, and epistemic status without claiming causal use?
5. What methods preserve separate dimensions for content identity, split or merge structure, scope or qualification change, relation preservation, attribution, contradiction, synthesis, and epistemic-status transition?
6. How are overlapping and many-to-many relations represented without forcing them into one mutually exclusive label?
7. Which agreement statistics and uncertainty procedures are used for prevalence-sensitive, span-based, clustered, or complex structured annotations, and what do those statistics fail to establish?
8. What evidence bears on the tradeoff between a narrow reliable codebook and retained coverage or ecological validity in long-form synthesis?
9. What failures arise when the same data are used to choose a relation class, stratum, codebook, or threshold and then evaluate it?
10. How should a feasibility gate be tied to the intended next experiment rather than copied from conventional agreement cutoffs?

## Search Method and Source Hierarchy

Public web research was conducted on 2026-07-24. Searches emphasized ACL Anthology, original dataset and project pages, publisher pages, PubMed or PMC, OpenReview, and author preprints when a canonical publication page did not expose the necessary methods. Search terms combined concepts such as `claim evidence annotation`, `rationale minimal evidence`, `support refute not enough information`, `evidence span agreement`, `attribution annotation`, `content unit identity`, `paraphrase adversarial`, `overlapping relations`, `complex annotation agreement`, `held-out validation`, `double dipping`, `prevalence kappa`, and `pilot precision threshold`.

The source hierarchy was:

1. Peer-reviewed original dataset, annotation, evaluation, or methodological papers.
2. Original project documentation when it clarified released fields or annotation access.
3. Original preprints for papers whose publication metadata or full method was easier to inspect there.

Secondary summaries, forums, social media, and marketing pages were not used to confirm factual claims. Sources were retained only when they supplied operational procedures, empirical reliability or validity evidence, concrete failure modes, or a directly relevant methodological warning. System-performance claims were retained only when they discriminated identity or measurement assumptions; benchmark marketing language was not treated as proof.

For each retained source, the review extracted the annotation unit, sampling frame, source access, annotator expertise, codebook or task definition, independent verification or adjudication, agreement statistic, retained coverage where available, and transfer limitations.

## Evidence Supporting the Main Direction

### C0005-EXT-01 — A narrow direct-support object is operationally possible in bounded tasks

SciFact defines a claim as an atomic, verifiable scientific finding and assigns SUPPORTS, REFUTES, or NOINFO to an individual claim–abstract pair. Supporting or refuting pairs require a minimal collection of rationale sentences which, in the context of the abstract, a domain expert judges to imply the claim. Compound claims are supposed to be split. On 232 independently re-annotated pairs, label agreement was Cohen’s κ = 0.75 and sentence-rationale agreement was κ = 0.71. This is the closest direct precedent for the proposed primary object: one claim, one bounded source unit, one relation judgment, and explicit evidence spans. `C0005-SRC-01`.

FEVER likewise separates claim labels from necessary evidence sentences and used claim generation followed by verification without exposing the original sentence used to generate the claim. Five-way label agreement was Fleiss’ κ = 0.6841. A later super-annotator audit found high evidence precision but materially lower evidence recall, which makes FEVER useful both as a construction precedent and as a warning that an apparent gold evidence set can be incomplete. `C0005-SRC-02`.

**What this supports:** a prospective B001 apparatus can define a narrow primary relation if it fixes claim atomicity, evidence boundaries, relation labels, and source context. It does not show that enough such pairs exist in the target handoff.

### C0005-EXT-02 — Content-bearing evidence units and source context should be explicit fields

QASPER required answerers to inspect full research papers and select the minimal evidence snippets sufficient for an answer, including discontiguous paragraphs, tables, and figures. More than half of text answers used multi-paragraph evidence, and many questions had multiple acceptable answers. Evidence Inference 2.0 gave medical doctors full trial articles, required a finding label plus a supporting span, and found that 63.0% of evidence spans were outside the abstract and 13.6% crossed more than one sentence. `C0005-SRC-03`, `C0005-SRC-04`.

**What this supports:** a locator alone is not a sufficient evidence object. The proposed schema should distinguish source identity, locator, content-bearing excerpt or span, source context available to the annotator, and bounded multi-span membership. It should permit bounded many-to-many structure even if the primary reliability unit is narrower.

### C0005-EXT-03 — Independent staged annotation and verification are feasible, but they are resource interventions

Evidence Inference 2.0 divided eleven medical doctors into mutually exclusive prompt-generation, prompt-annotation, and verification groups. QASPER used separate question writers and answerers. FEVER separated claim construction from verification. SciFact required verifiers to assess claims they had not written. These designs reduce direct self-confirmation and provide concrete role-separation procedures inside annotation pipelines. `C0005-SRC-01` through `C0005-SRC-04`.

**What this supports:** development, primary coding, and audit should be conducted by genuinely separate annotators where reliability is claimed. An adjudicated audit set is methodologically defensible.

**What it does not support:** these studies do not establish a beneficial fresh-conversation or role-separation effect. They add expertise, source access, verification passes, and labor.

### C0005-EXT-04 — Observable downstream incorporation can be defined without claiming latent use

AIS first asks whether an output is intelligible enough to yield an explicit interpretation, then asks whether that interpretation is attributable to an identified source. Its judgments are about observable source support, not about whether the generator causally relied on that source. QAPyramid similarly asks whether a predicate–argument QA unit is present or implied in a system summary while allowing wording to differ and grounding the judgment in the reference summary. `C0005-SRC-05`, `C0005-SRC-10`.

A B001 endpoint can therefore be operationalized as **observable downstream relation-preserving incorporation** with separately scored dimensions:

- content correspondence;
- source attribution correspondence;
- scope and qualification preservation;
- relation polarity preservation;
- epistemic-status correspondence;
- split or merge structure;
- contradiction or unsupported extension.

This is a defensible output-coding endpoint. It cannot identify causal reliance, reconstruction, or post hoc rationalization.

### C0005-EXT-05 — Multidimensional and overlapping relation annotation is preferable to a flat identity label

PARC 3.0 annotates attribution as linked source, cue, content, and supplement spans, including nested attribution. BECauSE 2.0 annotates causality alongside seven frequently co-present semantic relations rather than forcing one primary semantic reading. Both report useful agreement when relation and span dimensions are scored separately. BECauSE’s overlap annotations achieved relation-type κ = 0.91, while causal relation types achieved κ = 0.70; span agreement was separately reported using exact match and Jaccard overlap. `C0005-SRC-07`, `C0005-SRC-08`.

**What this supports:** B001 should keep content identity, scope, qualification, relation type, attribution, and epistemic status as separate fields. Qualification can be a required attribute of a direct-support object without being silently pooled into the same relation label.

### C0005-EXT-06 — Systematic decomposition can improve reproducibility of output-content coding

The Pyramid method constructs clause-sized Summary Content Units from multiple references and achieved Krippendorff’s α = 0.81 in its reliability study. QAPyramid replaces loosely defined content units with QA-SRL predicate–argument units. On 50 CNN/DailyMail examples and ten systems, it collected 8,910 presence judgments; three annotators judged each unit and majority vote produced an average κ = 0.74. It also found that 21% of predicates were only partially represented, supporting finer-grained, multidimensional coding rather than all-or-none sentence identity. `C0005-SRC-09`, `C0005-SRC-10`.

**What this supports:** a frozen decomposition procedure can make downstream correspondence more inspectable and reproducible than unconstrained semantic-similarity scoring.

### C0005-EXT-07 — Development and audit separation has a strong general methodological basis

Kriegeskorte et al. demonstrate through analysis and simulation that selecting features or regions on a dataset and then evaluating the selected result on the same data can distort descriptive statistics and invalidate inference when selection and evaluation are not independent under the null. The domain is neuroscience, but the methodological structure directly applies to choosing easy relation classes, favorable strata, exclusions, or thresholds on the same corpus later used to declare an apparatus feasible. `C0005-SRC-14`.

**What this supports:** the C0005 Critic’s requirement for a development/calibration sample and a separately held-out audit sample is well grounded. The primary relation, codebook, exclusions, denominators, strata, thresholds, and failure actions should be frozen before audit inspection.

## Evidence Weakening the Main Direction

### C0005-EXT-08 — One-claim/one-evidence direct support is often not the natural unit

FEVER reports that 31.75% of claims with appropriate evidence have more than one evidence sentence, 16.82% require multi-sentence composition, and 12.15% require evidence from multiple pages. In QASPER, more than 55.5% of text answers use multi-paragraph evidence; 44% of questions have multiple answers, and the human evidence lower-bound F1 was 71.6 rather than near-perfect. Evidence Inference found multi-sentence evidence and substantial evidence outside abstracts. `C0005-SRC-02` through `C0005-SRC-04`.

**Weakening implication:** a one-to-one pair may be a useful primary reliability unit but can be sparse, incomplete, or unrepresentative in open-ended research synthesis. Pair counts must not be inflated by splitting one dependency into many nominal pairs.

### C0005-EXT-09 — Exact evidence boundaries can be unstable even when annotators agree on the general region

In the PICO span study, exact span F1 was low for experts and non-experts, while relaxed overlap agreement was much higher. Expert exact-span F1 ranged from 0.357 to 0.576 across PICO classes, whereas expert token-overlap F1 exceeded 0.71. PARC’s source, cue, and content spans were reliable, but its deliberately underspecified supplement span had much lower agreement. `C0005-SRC-07`, `C0005-SRC-12`.

**Weakening implication:** “stable evidence item” cannot be equated with exact character boundaries. B001 needs both strict and relaxed boundary measures, plus a substantive rule for when relaxed overlap still preserves the proposition and qualification. Relaxed overlap improves apparent agreement but can conceal scope differences.

### C0005-EXT-10 — High percentage agreement and a single chance-corrected statistic do not establish validity

FRANK obtained 91% majority agreement on sentence factuality but only Fleiss’ κ = 0.58; when annotators agreed a sentence was nonfactual, fine-grained error-type κ fell to 0.39 despite 73.9% majority agreement. AIS agreement varied by task and was weaker on long-form summarization; for CNN/DailyMail, interpretability α was 0.46 and AIS α was 0.69. Feinstein and Cicchetti show analytically that high observed binary agreement can coexist with low κ under marginal imbalance. Braylan et al. show that complex-annotation agreement depends strongly on the chosen distance function and that a universal α threshold is not interpretable across tasks. `C0005-SRC-05`, `C0005-SRC-06`, `C0005-SRC-13`, `C0005-SRC-15`.

**Weakening implication:** a B001 gate cannot rely on one pooled κ or percent agreement. It should report prevalence, class-specific agreement, exact and relaxed span scores, disagreement composition, annotator-level uncertainty, clustering, and retained coverage. Agreement alone does not establish construct validity or role relevance.

### C0005-EXT-11 — Claim identity under paraphrase cannot be inferred from lexical or embedding similarity alone

PAWS contains 108,463 paraphrase and non-paraphrase pairs with high lexical overlap. Models trained on standard paraphrase data scored below 40% on PAWS, while adding PAWS training raised strong-model accuracy to roughly 85%; bag-of-words models remained unable to capture the needed structural distinctions. `C0005-SRC-11`.

**Weakening implication:** high semantic or lexical similarity can conceal argument reversal, scope change, or changed relations. PAWS does not solve split, merge, qualification, or synthesis lineage, but it directly defeats a simple similarity-based identity rule. B001 requires explicit human-coded dimensions rather than a single similarity threshold.

### C0005-EXT-12 — Narrowing and filtering can create reliability by removing the difficult work

SciFact restricts claims to atomic findings verifiable from one source and uses abstracts rather than full papers partly because prior full-document annotation had low agreement. QAPyramid keeps QA pairs only when both verifiers accept them and reruns generation when a predicate yields fewer than two retained pairs. BECauSE explicitly notes that adjacent semantic domains may need to be excluded because an exhaustive overlap scheme can expand toward the whole language. `C0005-SRC-01`, `C0005-SRC-08`, `C0005-SRC-10`.

**Weakening implication:** a small reliable core can be real yet ecologically weak. The audit must report the denominator before filtering, every exclusion reason, retained coverage, qualification density, multi-source dependence, and the fraction of Alternative Theorist work to which the retained object is relevant. A high-agreement residue is not enough.

### C0005-EXT-13 — No observable endpoint in the retained literature identifies causal evidence use

AIS measures whether an interpreted output is attributable to an identified source. Pyramid and QAPyramid measure whether content is present. Fact-verification datasets record labels and rationales. None observes the counterfactual dependence of a final statement on a selected evidence item. `C0005-SRC-01` through `C0005-SRC-05`, `C0005-SRC-09`, `C0005-SRC-10`.

**Weakening implication:** the branch should prohibit labels such as “used,” “reconstructed,” or “post hoc rationalized” unless an independent intervention identifies them. The defensible categories are recorded selection with or without observable incorporation, and observable incorporation with or without recorded selection.

## Evidence About Alternative Explanations

### Annotator expertise and source-access privilege

SciFact uses scientific NLP experts and life-science students; Evidence Inference uses medical doctors; QASPER uses NLP practitioners with full papers; FEVER uses a later super-annotator audit. Their apparent reliability can be caused by domain expertise, complete source access, adjudication time, and privileged reference construction rather than by the relation schema itself. `C0005-SRC-01` through `C0005-SRC-04`.

### Decomposition and task formalization

QAPyramid’s gains in reproducibility may come from QA-SRL predicate–argument decomposition, qualification tests, and repeated verification rather than from relation annotation generally. Pyramid and QAPyramid show that changing the unit changes the object being measured. `C0005-SRC-09`, `C0005-SRC-10`.

### Metric and distance-function choice

PICO exact and relaxed scores tell opposite-looking stories about the same annotations. BECauSE reports relation κ, connective F1, exact span agreement, Jaccard overlap, and head agreement separately. Braylan et al. show that complex-annotation distance functions can themselves produce or obscure measured disagreement. `C0005-SRC-08`, `C0005-SRC-12`, `C0005-SRC-13`.

### Prevalence and class imbalance

FRANK’s majority agreement versus κ gap and Feinstein and Cicchetti’s kappa paradoxes show that apparent reliability can change with prevalence and marginal distributions. A sparse positive direct-support class could produce misleading omnibus statistics. `C0005-SRC-06`, `C0005-SRC-15`.

### Filtering and favorable-subset selection

SciFact’s single-source atomicity, QAPyramid’s dual-verifier retention rule, and BECauSE’s out-of-scope decisions can improve reliability while reducing retained coverage. Choosing a task stratum or relation class after observing such results would add circular selection. `C0005-SRC-01`, `C0005-SRC-08`, `C0005-SRC-10`, `C0005-SRC-14`.

### Output-content correspondence without evidence dependence

AIS and content-unit methods can establish that output content is source-supported or corresponds to a reference. The same output could have been produced independently, and selected evidence can influence unobserved reasoning without appearing in the final text. Observable correspondence is therefore a measurement endpoint, not a mechanism. `C0005-SRC-05`, `C0005-SRC-09`, `C0005-SRC-10`.

## Fixed-Compute Versus Added-Compute Evidence

None of the sixteen retained sources compares the B001 role-separated loop with repeated single-model prompting under matched full inference compute. None isolates a fresh-role or invocation-boundary effect.

The positive annotation precedents generally receive additional resources:

- separate claim writers, answerers, or prompt generators;
- domain experts or medical doctors;
- full-source access rather than excerpts;
- multiple independent judgments;
- verification or adjudication passes;
- qualification tests, retraining, or reannotation;
- manually constructed reference inventories;
- majority voting or super-annotator audits.

These are not “free” properties of a schema. Evidence Inference’s mutually exclusive doctor roles, FEVER’s super-annotator review, QASPER’s separate practitioners, FRANK’s training and qualification, and QAPyramid’s generation plus two-verifier filtering all add labor and decision opportunities. `C0005-SRC-02` through `C0005-SRC-04`, `C0005-SRC-06`, `C0005-SRC-10`.

The retained sources therefore support only the following resource conclusion: a defensible B001 measurability pilot must record and cost corpus construction, source retrieval, evidence excerpting, claim splitting, duplicate coding, qualification, adjudication, schema repair, selected-subset reporting, downstream coding, and uncertainty analysis. A later effectiveness comparison must hold the apparatus common or charge it explicitly. Retained-token matching would not equalize these costs.

Role-separation effects remain completely unisolated. The fact that different human roles were used in dataset creation supports independence of annotations, not superiority of a multi-role inference architecture.

## Conflicting or Inconclusive Findings

1. **Narrow formalization versus ecological validity.** SciFact and QAPyramid show that atomic or systematic units can achieve useful agreement; QASPER, FEVER, Evidence Inference, and BECauSE show that real evidence and semantics are often multi-unit, overlapping, or context dependent. Both findings can be true because the narrow units retain different fractions of the original work.

2. **Exact versus relaxed identity.** PICO span annotations look unreliable under exact boundaries and substantially more reliable under overlap criteria. The literature does not determine which tolerance preserves B001-relevant scope and qualification; that must be defined prospectively.

3. **Expertise versus scalable crowd annotation.** Evidence Inference and SciFact rely heavily on expertise, while QAPyramid reports high agreement from qualified crowd workers. The tasks differ in domain complexity, unit definition, filtering, and source access, so this is not evidence that expertise is unnecessary.

4. **High agreement versus difficult long-form coding.** QAPyramid reports κ = 0.74 for granular presence judgments, whereas AIS and FRANK show lower or task-dependent agreement in long-form source-supported output evaluation. The difference may reflect unit granularity, corpus, filtering, and judgment scope rather than one superior protocol.

5. **Single-source simplicity versus full-source necessity.** SciFact’s abstract-level, single-source restriction supports reliable direct support; QASPER and Evidence Inference show that full documents and multiple evidence units are frequently necessary. The target handoff’s distribution is unknown.

6. **Agreement thresholds.** The Pyramid paper cites a conventional α threshold, while Braylan et al. show that acceptable α varies with task and distance function. Sim and Lewis demonstrate in a different pilot-study domain that sample size should be tied to the precision and efficiency requirements of the intended main study. No source supplies a valid numeric B001 gate. `C0005-SRC-09`, `C0005-SRC-13`, `C0005-SRC-16`.

## Source Reliability and Independence

All sixteen retained sources are primary: peer-reviewed dataset papers, annotation-method papers, methodological studies, or journal articles by the original authors. Original project pages were consulted only to clarify released fields, not counted as additional sources.

The evidence is not sixteen independent validations of one apparatus. It clusters into partially dependent method families:

- **Claim verification and evidence rationales:** SciFact, FEVER, Evidence Inference.
- **Full-document evidence selection:** QASPER, Evidence Inference.
- **Output attribution and summarization content:** AIS, FRANK, Pyramid, QAPyramid.
- **Span and overlapping-relation annotation:** PARC, BECauSE, PICO.
- **Identity stress testing:** PAWS.
- **Agreement, circularity, and threshold methods:** Braylan et al., Kriegeskorte et al., Feinstein and Cicchetti, Sim and Lewis.

FEVER and SciFact differ in domain and construction but share fact-verification assumptions. Pyramid and QAPyramid are directly related method families. AIS and FRANK both use summarization settings. Evidence Inference and PICO are both biomedical and depend on domain-specific representations. The general-method sources are independent of those datasets but transfer only by analogy to B001.

The strongest sources for direct operational transfer are SciFact, QASPER, Evidence Inference, AIS, PARC, BECauSE, FRANK, and QAPyramid. PAWS, Kriegeskorte, Feinstein and Cicchetti, and Sim and Lewis are important but indirect: they support identity, circularity, metric, and feasibility principles rather than the exact claim–support handoff.

## Evidence Gaps

1. No source studies the External Evidence Researcher → Alternative Theorist handoff or an analogous source-research → alternative-hypothesis transition with item-level lineage.
2. No source estimates the prevalence of narrow direct-support pairs in the authorized B001 corpus.
3. No source validates B001’s proposed output-incorporation construct across content, attribution, scope, qualification, relation, and epistemic-status dimensions.
4. No source establishes that a selected-subset checkpoint observes natural retrieval; it remains an intervention.
5. No source identifies latent causal evidence use from output text, citations, rationales, or recorded selection.
6. No source supplies a complete codebook for paraphrase, split, merge, generalization, narrowing, qualification weakening, contradiction, support substitution, synthesis, and epistemic retyping together.
7. No source gives a fully general reliability statistic for clustered many-to-many claim–evidence lineage. Distance and matching rules remain task-specific.
8. No source establishes a branch-appropriate retained-coverage minimum or nontrivial pair count.
9. No source supplies a B001-specific development/audit split, power analysis, or false-passage cost.
10. No source separates relation-schema value from expertise, source access, reference construction, validation labor, and adjudication compute.
11. No source establishes whether direct support or qualification is the better primary relation for this handoff. A switch requires a new prospective validation.
12. No source shows that successful apparatus measurability predicts a later relation-availability effect, representation effect, role effect, or fresh-invocation effect.

## Source Ledger

### C0005-SRC-01

- **Title:** Fact or Fiction: Verifying Scientific Claims
- **Authors or organization:** David Wadden, Shanchuan Lin, Kyle Lo, Lucy Lu Wang, Madeleine van Zuylen, Arman Cohan, Hannaneh Hajishirzi
- **Date:** November 2020
- **URL or DOI:** https://aclanthology.org/2020.emnlp-main.609/ ; DOI 10.18653/v1/2020.emnlp-main.609
- **Source type:** Peer-reviewed original dataset and annotation paper
- **Study design and sample:** SciFact contains 1,409 claims and 5,183 scientific abstracts. Claims are intended to be atomic, verifiable findings from one source. Individual claim–abstract pairs receive SUPPORTS, REFUTES, or NOINFO; positive or negative pairs require minimal rationale sentences. Verifiers did not assess claims they wrote. A 232-pair independent reannotation yielded label κ = 0.75 and rationale κ = 0.71.
- **Claim supported or weakened:** Supports a narrow direct-support object, separate writers and verifiers, minimal evidence rationales, and pair-level relation coding. Weakens transfer to open synthesis because it restricts claims to one source and mostly abstract context.
- **Important limitations:** Biomedical/scientific domain; claims are deliberately atomic; abstracts replace full articles; rationale sets are at most three sentences and mutually exclusive; difficult full-document and multi-source cases are excluded.

### C0005-SRC-02

- **Title:** FEVER: a Large-scale Dataset for Fact Extraction and VERification
- **Authors or organization:** James Thorne, Andreas Vlachos, Christos Christodoulopoulos, Arpit Mittal
- **Date:** June 2018
- **URL or DOI:** https://aclanthology.org/N18-1074/ ; DOI 10.18653/v1/N18-1074
- **Source type:** Peer-reviewed original benchmark and dataset paper
- **Study design and sample:** 185,445 Wikipedia-derived claims were generated and later verified without showing annotators the source sentence used to construct each claim. Labels are SUPPORTED, REFUTED, or NOT ENOUGH INFO; supporting and refuting labels include necessary evidence sentences. Five-way label agreement was Fleiss’ κ = 0.6841. A super-annotator audit reported evidence precision of 95.42% but recall of 72.36%. Multi-sentence and multi-page evidence were common enough to be reported separately.
- **Claim supported or weakened:** Supports staged construction and verification, claim labels separate from evidence, and expert audit. Weakens any assumption that a gold evidence inventory is complete or that one evidence sentence is usually sufficient.
- **Important limitations:** Synthetic claims from Wikipedia; evidence search space and task differ from open research synthesis; super-annotator review adds privileged labor; evidence recall remained incomplete.

### C0005-SRC-03

- **Title:** A Dataset of Information-Seeking Questions and Answers Anchored in Research Papers
- **Authors or organization:** Pradeep Dasigi, Kyle Lo, Iz Beltagy, Arman Cohan, Noah A. Smith, Matt Gardner
- **Date:** June 2021
- **URL or DOI:** https://aclanthology.org/2021.naacl-main.365/ ; DOI 10.18653/v1/2021.naacl-main.365
- **Source type:** Peer-reviewed original dataset paper
- **Study design and sample:** QASPER contains 5,049 questions over 1,585 NLP papers. Question writers and answerers were separate NLP practitioners. Answerers saw full papers and selected minimal evidence snippets, including paragraphs, tables, and figures. More than 55.5% of text answers used multiple paragraphs; 44% of questions had multiple answers. The human evidence lower-bound F1 was 71.6.
- **Claim supported or weakened:** Supports full-source access, content-bearing evidence, multiple references, and separation of writers and answerers. Weakens a one-to-one evidence-pair model and a single-gold-evidence assumption.
- **Important limitations:** QA rather than alternative-theory generation; evidence is answer-oriented; NLP papers and practitioner annotators may not generalize; multiple acceptable answers complicate identity and completeness.

### C0005-SRC-04

- **Title:** Evidence Inference 2.0: More Data, Better Models
- **Authors or organization:** Jay DeYoung, Eric Lehman, Benjamin Nye, Iain J. Marshall, Byron C. Wallace
- **Date:** July 2020
- **URL or DOI:** https://aclanthology.org/2020.bionlp-1.13/ ; DOI 10.18653/v1/2020.bionlp-1.13
- **Source type:** Peer-reviewed original dataset-extension and annotation paper
- **Study design and sample:** The expanded corpus contains 12,616 intervention–comparator–outcome prompts from 3,346 randomized-trial articles. Eleven medical doctors were divided into mutually exclusive prompt-generation, prompt-annotation, and verification roles. Annotators supplied a relation label and supporting span from the full article. Of evidence spans, 63.0% were outside abstracts and 13.6% covered more than one sentence.
- **Claim supported or weakened:** Supports independent staged annotation, expert source access, a third-party verifier, and explicit evidence spans. Weakens excerpt-only or abstract-only adjudication and shows that the apparatus cost includes expert full-text reading.
- **Important limitations:** Highly structured clinical question; one doctor initially annotates each prompt; expert labor and verification are expensive; the source paper does not establish a general held-out codebook audit.

### C0005-SRC-05

- **Title:** Measuring Attribution in Natural Language Generation Models
- **Authors or organization:** Hannah Rashkin, Vitaly Nikolaev, Matthew Lamm, Lora Aroyo, Michael Collins, Dipanjan Das, Slav Petrov, Gaurav Singh Tomar, Iulia Turc, David Reitter
- **Date:** December 2023
- **URL or DOI:** https://aclanthology.org/2023.cl-4.2/ ; DOI 10.1162/coli_a_00486
- **Source type:** Peer-reviewed journal methods and human-evaluation paper
- **Study design and sample:** AIS was evaluated across two conversational QA settings, summarization, and table-to-text. The two-stage protocol first elicits an intelligible interpretation or explicature, then judges whether it is attributable to an identified source. The paper reports Krippendorff’s α, pairwise agreement, consensus F1, and expert comparisons; agreement varies by task and is lower on some long-form outputs.
- **Claim supported or weakened:** Supports an observable output-level source-support endpoint and separate interpretability screening. Weakens causal “use” language and universal reliability assumptions.
- **Important limitations:** Attribution is binary at the evaluated unit and does not identify causal dependence; task-specific source formats; long-form agreement is imperfect; it does not trace upstream pair identity through an agent handoff.

### C0005-SRC-06

- **Title:** Understanding Factuality in Abstractive Summarization with FRANK: A Benchmark for Factuality Metrics
- **Authors or organization:** Artidoro Pagnoni, Vidhisha Balachandran, Yulia Tsvetkov
- **Date:** June 2021
- **URL or DOI:** https://aclanthology.org/2021.naacl-main.383/ ; DOI 10.18653/v1/2021.naacl-main.383
- **Source type:** Peer-reviewed original benchmark and annotation study
- **Study design and sample:** 2,250 summaries from nine systems over CNN/DailyMail and XSum were annotated, with three independent judgments per summary. Annotators judged sentence factuality in summary context and then applied a multi-label error typology. Training, qualification, and continuing quality checks were used. Sentence factuality κ was 0.58; error-category κ was 0.39.
- **Claim supported or weakened:** Supports role-aligned output segmentation and multidimensional error coding. Strongly weakens the assumption that high majority agreement or a detailed codebook guarantees reliable fine-grained lineage.
- **Important limitations:** Summarization rather than claim–evidence transfer; crowd annotation with quality controls; factuality error types are not the same as direct-support, qualification, or epistemic-status lineage.

### C0005-SRC-07

- **Title:** PARC 3.0: A Corpus of Attribution Relations
- **Authors or organization:** Silvia Pareti
- **Date:** May 2016
- **URL or DOI:** https://aclanthology.org/L16-1619/ ; no DOI listed
- **Source type:** Peer-reviewed original corpus and annotation paper
- **Study design and sample:** Approximately 20,000 attribution relations are annotated with source, cue, content, and supplement spans, including nested relations. Trained linguists double-annotated a subset. Overall relation-identification agreement was about 0.79; span overlap was high for cue, source, and content but much lower for the underspecified supplement field.
- **Claim supported or weakened:** Supports linked multidimensional relation objects, nested relations, and separate relation and span metrics. Weakens broad or underspecified auxiliary fields.
- **Important limitations:** News attribution rather than evidential support; double-coded subset is limited; no downstream generation or identity transformation; supplement disagreement shows sensitivity to codebook precision.

### C0005-SRC-08

- **Title:** The BECauSE Corpus 2.0: Annotating Causality and Overlapping Relations
- **Authors or organization:** Jesse Dunietz, Lori Levin, Jaime Carbonell
- **Date:** April 2017
- **URL or DOI:** https://aclanthology.org/W17-0812/ ; DOI 10.18653/v1/W17-0812
- **Source type:** Peer-reviewed original corpus and annotation paper
- **Study design and sample:** The corpus contains 5,380 sentences, 1,803 causal-language instances, 587 causal instances with overlapping relations, and 583 non-causal overlapping-relation annotations. Two primary annotators double-coded 260 sentences containing 98 causal and 82 overlapping instances. Relation-type κ was 0.70 for causal and 0.91 for overlapping relations; exact and overlap-based span metrics were reported separately.
- **Claim supported or weakened:** Supports co-present relation labels, explicit linguistic tests, and multidimensional agreement. Weakens a mutually exclusive flat relation scheme and warns that exhaustive adjacent-domain annotation can become infeasible.
- **Important limitations:** Linguistic causality is not evidential support; only two primary annotators; some semantic domains were deliberately excluded; agreement is conditional on matching connectives for some metrics.

### C0005-SRC-09

- **Title:** Evaluating Content Selection in Summarization: The Pyramid Method
- **Authors or organization:** Ani Nenkova, Rebecca Passonneau
- **Date:** May 2004
- **URL or DOI:** https://aclanthology.org/N04-1019/ ; no DOI listed
- **Source type:** Peer-reviewed original evaluation-method paper
- **Study design and sample:** The method derives clause-sized Summary Content Units from multiple human summaries. The empirical study used three DUC 2003 document sets, four original human summaries per set, and six additional summaries per set. Two coders achieved Krippendorff’s α = 0.81 on an SCU inventory, and the resulting pyramid scores were robust across the two codings and consensus. The paper found at least five summaries were needed for score stability in that setting.
- **Claim supported or weakened:** Supports systematic content units, multiple references, and output-level incorporation scoring. Weakens single-reference evaluation and unconstrained percentage-overlap judgments.
- **Important limitations:** Content salience rather than evidential support; SCUs treat semantic dependencies as independent; the reliability study is small and uses the co-authors as coders; the numeric threshold and five-summary result are task-specific.

### C0005-SRC-10

- **Title:** QAPyramid: Fine-grained Evaluation of Content Selection for Text Summarization
- **Authors or organization:** Shiyue Zhang, David Wan, Arie Cattan, Ayal Klein, Ido Dagan, Mohit Bansal
- **Date:** July 2025
- **URL or DOI:** https://openreview.net/forum?id=dZRzInscvA ; preprint https://arxiv.org/abs/2412.07096
- **Source type:** Peer-reviewed original evaluation-method and dataset paper, COLM 2025
- **Study design and sample:** QA-SRL predicate–argument units were generated for 500 CNN/DailyMail reference summaries. On a random subset of 50 examples and ten systems, 8,910 QA-presence judgments were collected. Each presence judgment had three independent annotators and majority vote; average Krippendorff’s κ was 0.74. QA generation used qualification, two-verifier validation, continuing accuracy requirements, and retention only when both verifiers accepted the pair. Twenty-one percent of predicates had only some QA units present.
- **Claim supported or weakened:** Supports systematic fine-grained content identity and separate partial-presence dimensions. Weakens broad content units, but also exposes filtering and repeated-validation costs that can create an easy retained core.
- **Important limitations:** Only 50 evaluation examples; summarization presence rather than claim–evidence support; invalid or disputed QA units are filtered out; no held-out test of the frozen unit-generation policy against open-ended synthesis.

### C0005-SRC-11

- **Title:** PAWS: Paraphrase Adversaries from Word Scrambling
- **Authors or organization:** Yuan Zhang, Jason Baldridge, Luheng He
- **Date:** June 2019
- **URL or DOI:** https://aclanthology.org/N19-1131/ ; DOI 10.18653/v1/N19-1131
- **Source type:** Peer-reviewed original adversarial dataset and model study
- **Study design and sample:** 108,463 well-formed paraphrase and non-paraphrase pairs with high bag-of-words overlap were generated by controlled word swapping and back translation and judged by humans. Strong models trained on ordinary paraphrase data scored below 40% on PAWS; adding PAWS examples raised accuracy to about 85%, whereas bag-of-words models remained weak.
- **Claim supported or weakened:** Weakens lexical-overlap and ordinary semantic-similarity identity rules; supports explicit structural and relational identity checks.
- **Important limitations:** Pairwise sentence paraphrase, not evidence lineage; model performance rather than human split/merge coding; does not cover qualification, synthesis, attribution, or epistemic transition.

### C0005-SRC-12

- **Title:** A Study on Agreement in PICO Span Annotations
- **Authors or organization:** Grace E. Lee, Aixin Sun
- **Date:** July 2019
- **URL or DOI:** https://arxiv.org/abs/1904.09557 ; DOI 10.1145/3331184.3331352
- **Source type:** Peer-reviewed original annotation-agreement study
- **Study design and sample:** The analysis uses the EBM-PICO dataset of 5,000 biomedical abstracts, each annotated by at least three non-experts; 200 abstracts also have at least two medical-expert annotations. Agreement is reported using exact span, one-boundary overlap, and token-overlap F1. Exact agreement was low even among experts, while relaxed overlap agreement was much higher.
- **Claim supported or weakened:** Supports reporting strict and relaxed evidence-boundary agreement separately and examining expert/non-expert differences. Weakens exact-boundary identity as the sole reliability criterion.
- **Important limitations:** PICO entities rather than support relations; relaxed overlap can credit materially different spans; pairwise F1 is not a complete chance-corrected reliability measure; domain-specific verbose spans.

### C0005-SRC-13

- **Title:** Measuring Annotator Agreement Generally across Complex Structured, Multi-object, and Free-text Annotation Tasks
- **Authors or organization:** Alexander Braylan, Omar Alonso, Matthew Lease
- **Date:** April 2022
- **URL or DOI:** https://arxiv.org/abs/2212.09503 ; DOI 10.1145/3485447.3512242
- **Source type:** Peer-reviewed original methods and empirical comparison paper
- **Study design and sample:** Agreement methods are evaluated across seven diverse complex tasks, including bounding boxes, keypoints, sequence tagging, ranked lists, translations, numeric vectors, and syntax trees. The paper analyzes generalized Krippendorff α with task-specific distances and proposes distributional alternatives. It shows that interpretation and thresholds vary substantially with task and distance function.
- **Claim supported or weakened:** Supports explicit annotation-distance functions, multi-object matching, and distribution inspection. Weakens universal α cutoffs and any claim that one omnibus statistic establishes quality.
- **Important limitations:** No claim–evidence task; proposed statistics are not a validated B001 gate; choosing a distance function still encodes substantive assumptions.

### C0005-SRC-14

- **Title:** Circular Analysis in Systems Neuroscience: The Dangers of Double Dipping
- **Authors or organization:** Nikolaus Kriegeskorte, W. Kyle Simmons, Patrick S. F. Bellgowan, Chris I. Baker
- **Date:** April 2009
- **URL or DOI:** https://pmc.ncbi.nlm.nih.gov/articles/PMC2841687/ ; DOI 10.1038/nn.2303
- **Source type:** Peer-reviewed methodological perspective with original simulations and analyses
- **Study design and sample:** The paper analyzes and simulates selection followed by selective analysis on the same noisy data, showing distorted descriptive statistics and invalid inference when the result statistic is not independent of the selection criterion under the null.
- **Claim supported or weakened:** Supports a separate development/calibration sample and held-out audit, and weakens post hoc selection of easy relations, favorable strata, or thresholds.
- **Important limitations:** Neuroscience rather than annotation; does not prescribe a B001 sampling split or threshold; the transfer is methodological rather than direct empirical evidence about claim–support coding.

### C0005-SRC-15

- **Title:** High Agreement but Low Kappa: I. The Problems of Two Paradoxes
- **Authors or organization:** Alvan R. Feinstein, Domenic V. Cicchetti
- **Date:** 1990
- **URL or DOI:** https://pubmed.ncbi.nlm.nih.gov/2348207/ ; DOI 10.1016/0895-4356(90)90158-L
- **Source type:** Peer-reviewed original statistical methods paper
- **Study design and sample:** The paper analytically examines binary observer-agreement tables and shows how marginal imbalance can produce high observed agreement with much lower kappa, and how asymmetric prevalence can alter kappa in counterintuitive ways.
- **Claim supported or weakened:** Supports reporting class prevalence and positive/negative agreement rather than relying on one pooled κ. Weakens high-percent-agreement claims for sparse direct-support classes.
- **Important limitations:** Binary tables with two observers; no span, many-to-many, clustered, or multi-label structure; does not establish a preferred statistic for B001.

### C0005-SRC-16

- **Title:** The Size of a Pilot Study for a Clinical Trial Should Be Calculated in Relation to Considerations of Precision and Efficiency
- **Authors or organization:** Julius Sim, Martyn Lewis
- **Date:** March 2012
- **URL or DOI:** https://pubmed.ncbi.nlm.nih.gov/22169081/ ; DOI 10.1016/j.jclinepi.2011.07.011
- **Source type:** Peer-reviewed original statistical methods paper
- **Study design and sample:** The paper derives pilot-study sizes from confidence intervals for a standard deviation and from the precision and efficiency requirements of a planned main randomized trial. It evaluates how pilot uncertainty affects main-study power and total sample efficiency.
- **Claim supported or weakened:** Supports the principle that a feasibility sample and gate should be sized for the intended next experiment and false-passage cost rather than by a conventional fixed number.
- **Important limitations:** Clinical-trial variance estimation, not annotation reliability; it does not provide a numeric B001 pair-count or coder-count rule; transfer is methodological and requires a branch-specific uncertainty model.

## Handoff to Alternative Theorist and Integrator

The strongest support for the corrected direction is methodological: bounded tasks show that atomic claims, content-bearing evidence units, source context, independent verification, multidimensional relation fields, and an observable output-incorporation endpoint can be specified and reliability-tested.

The strongest adverse evidence is equally material: realistic evidence is frequently multi-sentence, multi-paragraph, multi-source, overlapping, or qualification dependent; exact spans and fine-grained error types can remain unreliable; a high-agreement retained core can be produced by filtering; and no observable output measure identifies causal evidence use.

The next roles should therefore consider at least these competing apparatus interpretations without selecting a winner here:

1. **Small-core feasibility:** a prospectively frozen atomic direct-support subset may be sufficiently common and role-relevant for a first pilot.
2. **Coverage-failure alternative:** the reliable subset may exclude too much qualification-rich and synthesis-heavy work to represent the handoff.
3. **Identity-bottleneck alternative:** direct support may be clear upstream while split, merge, scope, qualification, and epistemic transformations prevent stable downstream lineage.
4. **Source-access and expertise alternative:** apparent reliability may depend more on full-source access, expert annotators, and verification labor than on the relation schema.
5. **Metric-construction alternative:** pass or failure may be driven by boundary tolerance, distance function, prevalence, clustering, or filtering rather than by the underlying object.
6. **Role-fit alternative:** sparse factual incorporation may be legitimate because the Alternative Theorist’s function includes hypotheses, objections, and unresolved questions.

Any prospective apparatus should freeze the corpus and denominators, use a development/audit split, retain direct support as the primary relation for that audit, score qualification as a separate required attribute, use independent blinded duplicate coding and adjudication, report strict and relaxed identity measures plus retained coverage and exclusion composition, and label the endpoint as observable relation-preserving incorporation rather than causal use. Failure should trigger a predeclared action rather than a post hoc search for a favorable relation class or task stratum.
