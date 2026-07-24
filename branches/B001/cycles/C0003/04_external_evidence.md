# External Evidence Researcher — C0003

## Research Scope

This report investigates the corrected C0003 frontier rather than the broad question of whether structured memory, graph memory, multi-agent systems, or long context generally improve performance. The primary target is the smallest defensible metadata intervention identified by the Critic and Internal Evidence Researcher:

> Under a declared end-to-end budget, what changes when one predeclared metadata type—preferably a claim–support or qualification relation—is made explicitly available in an otherwise fixed base package, with coverage, task completion, position, downstream instructions, model settings, and evaluation held constant as far as feasible?

A separate representation question asks whether approximately equivalent relational content produces different outcomes when expressed as controlled prose versus a typed field, table, triple, or edge. Write–retrieve–use decomposition is treated as a diagnostic framework, not as a second causal treatment.

The search therefore prioritized evidence that directly or nearly directly addresses: explicit relation availability; equivalent-content representation; observable writing, retrieval, and use checkpoints; claim–evidence and epistemic annotation reliability; information-geometry confounds; complete resource accounting; and transfer to open-ended multi-source research writing. Broad structured-memory and long-context findings already represented in C0002 were not treated as new independent confirmation.

The main search-bounded result is negative but informative: **no located primary study implements the corrected claim–support or qualification metadata contrast while approximately holding base semantic content, task, reader prompt, model settings, information position, coverage, and full end-to-end inference resources constant.** The closest evidence establishes that relational representation and metadata can materially change model behavior, that claim–evidence links can be annotated and scored, and that retrieval and generation errors can be separated diagnostically. It does not establish that adding one explicit relation field improves B001-style research synthesis under fixed compute.

## Search Questions

1. Are there controlled primary studies that vary one explicit metadata type, especially claim–support or qualification metadata, while holding the base claim content and downstream task approximately constant?
2. Are there studies comparing approximately equivalent relational content expressed in prose versus typed triples, tables, graphs, or links?
3. Are there primary methods that separately observe package or memory writing, explicit retrieval or selection, and downstream use?
4. Are there validated annotation or evaluation methods for claim–support relations, evidence rationales, epistemic labels, omissions, mutations, or other lineage-relevant objects?
5. What controlled evidence shows that ordering, grouping, format, irrelevant context, or non-semantic metadata can alter use of the same base information?
6. Do any direct studies report enough end-to-end cost detail to distinguish metadata effects from added writer, verifier, retrieval, candidate, selector, or training resources?
7. Do any qualifying studies test the corrected contrast in open-ended multi-source research synthesis?
8. Which sources share task, dataset, author, or mechanism families and therefore should not be counted as fully independent evidence?

## Search Method and Source Hierarchy

Searches combined targeted scholarly queries for claim–evidence linking, scientific claim verification, structured versus natural-language representations, table serialization, RAG diagnostics, epistemic markers, uncertainty alignment, and knowledge-intensive long-form writing. Candidate sources were checked through canonical publisher, proceedings, anthology, author-project, or repository pages. Primary papers were preferred over summaries. Source details were taken from the paper or official proceedings record; marketing language was not treated as evidence.

The source hierarchy used was:

1. Peer-reviewed original research papers and benchmark papers.
2. Original author preprints when the peer-reviewed version or full experimental details were not otherwise accessible.
3. Official project or repository documentation accompanying a primary paper.
4. Secondary material only for discovery; no factual conclusion below depends on forum, social-media, or promotional claims.

Each source was classified by the factor it actually manipulates or measures: metadata availability, metadata representation, information geometry, uncertainty labeling, retrieval, downstream use, writer quality, verifier quality, or open-ended synthesis. A study was not considered fixed-compute merely because it used the same model, a fixed context window, a fixed output cap, or the same number of benchmark items.

Fourteen primary sources are used in the ledger. They are not fourteen independent demonstrations of one mechanism: several belong to overlapping fact-verification, uncertainty, structured-input, or long-form-writing families.

## Evidence Supporting the Main Direction

### C0003-EXT-01 — Approximately equivalent relational content can produce different outcomes under different representations

The closest representation evidence is `C0003-SRC-03`. Dai et al. compare knowledge-graph relations represented as linearized triples, meta-paths, rule-generated natural language, and model-generated natural language. Their complementary Text-to-Triple setup begins with human-written documents and manually annotated relation triples, reducing the concern that poor generated prose alone explains the difference. Across fact-intensive and multi-hop QA settings, linearized triples generally outperform fluent natural-language representations, while preferred organization varies by model. This supports the narrow proposition that **representation is an active intervention even when the underlying entities and relations are intended to be equivalent**.

The evidence is near-direct rather than direct to B001. The represented relations are entity-relation-entity facts, not claim–support or qualification links. Different serializations change token count, redundancy, wording, adjacency, and information density; semantic equivalence is intended but not proven item by item. The study does not report a complete end-to-end compute ledger, and its outcomes are short-answer QA rather than research synthesis.

`C0003-SRC-04` independently shows that table serialization format, content order, partition marks, and prompt choices materially affect GPT-3.5/GPT-4 performance on seven structural-understanding tasks and several downstream table tasks. This is useful as a manipulation-check warning: a typed-field experiment can be confounded by serialization, order, and delimiters even when table cells are unchanged. It is not evidence that claim–support edges help; some downstream gains also use self-augmentation and additional prompt work.

### C0003-EXT-02 — Metadata can causally influence which conflicting evidence a model follows

`C0003-SRC-02` holds the two conflicting webpage texts fixed and swaps publication-time, source, or visual-appearance metadata between them. On 355 real controversial questions and 125 synthetic unknown-entity questions, publication time changes answers for most tested models, source has a smaller effect, and visual appearance has a strong causal effect for Claude-3 in the tested setup. This is unusually direct evidence that **metadata is not a neutral wrapper** and can alter downstream evidence use without changing the core conflicting text.

This finding supports the branch’s requirement to treat metadata availability and representation as explicit treatments and to include placebo and salience checks. It does not show that the effect is epistemically beneficial: the metadata can act as a superficial authority or recency cue and can redirect an answer independently of textual evidential quality. It also does not test claim–support links, qualifications, or research synthesis.

### C0003-EXT-03 — Full-paper claim–evidence relations are annotatable and models remain weak at recovering them

`C0003-SRC-01` is the most direct source for the scientific-research domain. CLAIM-BENCH contains 346 annotations linking 331 claims to 335 evidence passages in 100 full AI/ML papers. Four PhD researchers created the data, and a separate group re-annotated 30 papers with reported moderate-to-substantial agreement. Six LLMs with at least 128K context windows were evaluated under common prompt templates, output schema, deterministic decoding, and matching rules.

Even the best claim-identification F1 was only 0.59. Long-range claim–evidence linking was difficult, and decomposed three-pass or per-claim prompting retrieved more than four times as many pairs as the single-pass baseline, raising recall but also false-positive risk and computational cost. This supports three branch design needs: predeclared claim–support inventories, explicit link scoring rather than citation presence, and separate precision and coverage reporting. It also weakens any assumption that a downstream reader can reliably reconstruct dispersed support relations from raw text.

The study does not test whether supplying gold claim–support metadata improves downstream conclusions. Its improved strategies add calls and processing, so they do not establish fixed-compute superiority of staged extraction or explicit relation packages.

### C0003-EXT-04 — Claim–evidence inventories and rationale-sensitive scoring are feasible

`C0003-SRC-06`, `C0003-SRC-07`, and `C0003-SRC-08` provide primary benchmark evidence that claim labels should be coupled to evidence objects rather than scored as label-only predictions.

- FEVER (`C0003-SRC-06`) contains 185,445 claims labeled Supported, Refuted, or NotEnoughInfo, with evidence sets for supported or refuted claims. Five-way annotation on 7,506 claims produced Fleiss κ = 0.6841. Evidence retrieval achieved 95.42% precision and 72.36% recall; 16.82% of claims required multiple sentences and 12.15% required evidence from multiple pages.
- SciFact (`C0003-SRC-07`) contains 1,409 scientific claims and 5,183 abstracts. It separately scores abstract retrieval, rationale selection, and verdict prediction, including a stricter label-plus-rationale outcome. Its three-component baseline makes retrieval, rationale selection, and verdict use observable rather than collapsing them into one score.
- AVeriTeC (`C0003-SRC-08`) contains 4,568 real-world claims from 50 fact-checking organizations, annotated with evidence-backed question–answer pairs and textual justifications for how evidence combines into a verdict. Its multi-round annotation reached κ = 0.619 on verdicts.

Together these sources support a reference inventory containing claims, labels, evidence sets, and intermediate reasoning objects. They also show that relational annotation is difficult but can reach moderate or substantial reliability. They do **not** provide a validated cross-stage lineage codebook for introduced, preserved, omitted, retyped, contradicted, corrected, mutated, or amplified claims, and none tests a package metadata intervention.

### C0003-EXT-05 — Retrieval and downstream generation can be diagnosed separately when selection is observable

RAGChecker (`C0003-SRC-05`) uses claim-level entailment to score overall answer precision/recall and to diagnose retriever claim recall/context precision separately from generator context utilization, noise sensitivity, hallucination, self-knowledge, and faithfulness. It meta-evaluates its metrics against human judgments and applies them to eight RAG systems across ten domains.

This supports the Critic’s correction that retrieval must be represented by an observed selected context or retrieval output, not inferred from mere presence in a larger context. It also supports separate checkpoint rates: relevant information retrieved, retrieved information used, irrelevant information followed, and unsupported content generated.

RAGChecker begins after a knowledge base already exists; it does not observe package writing or transformation into memory. Its claim extraction and entailment checks introduce evaluator-model assumptions. It therefore supports the retrieve–use portion of the diagnostic, not a full write–retrieve–use causal decomposition.

### C0003-EXT-06 — Explicit uncertainty representations can be learned and used, but benefits require substantial additional machinery

`C0003-SRC-09` shows that a fine-tuned GPT-3 can produce verbal or numerical confidence that is calibrated on CalibratedMath and remains moderately calibrated under distribution shift. This establishes the feasibility of carrying explicit uncertainty metadata in natural language.

`C0003-SRC-11` reports improved known-answer versus refuse-unknown behavior when confidence and semantic-entropy features are incorporated into UAlign. However, UAlign samples multiple responses, trains uncertainty estimators, trains a reward model, and performs PPO optimization. Its positive result supports uncertainty-aware alignment as a system intervention, not the independent value of an attached status field under fixed inference compute.

The uncertainty evidence therefore supports keeping epistemic-status metadata as a separately testable factor, but it does not justify bundling status labels with claim–support relations in the first pilot.

### C0003-EXT-07 — Open-ended research writing exhibits the exact transfer failures the package is meant to detect

STORM (`C0003-SRC-12`) and KIWI (`C0003-SRC-13`) are the closest sources to open-ended research synthesis.

STORM performs retrieval, multi-perspective question asking, simulated writer–expert conversations, information curation, outlining, and article generation. On 100 FreshWiki topics, expert Wikipedia editors rated STORM articles 25 percentage points more often organized and 10 points more often broad in coverage than an outline-driven RAG baseline. The same evaluation identified source-bias transfer and fabricated or over-associated connections between unrelated facts. This supports relation and provenance checks as relevant failure diagnostics in long-form synthesis.

KIWI contains 1,260 interaction turns from 234 expert-guided scientific writing sessions using three LLMs. Models struggled to incorporate new information into an existing answer and to execute precise edits; model self-judgment was at least ten points below human agreement. This directly supports the need to trace whether a qualification, evidence item, or requested correction was preserved or mutated across revisions.

Neither source isolates metadata availability or representation. STORM bundles multiple roles, retrieval stages, calls, and curation; KIWI is an observational instruction-following dataset rather than a randomized package experiment.

## Evidence Weakening the Main Direction

### C0003-EXT-08 — No direct qualifying metadata experiment was located

No source in this search compares:

1. identical or predeclared base claims;
2. one claim–support or qualification metadata type absent versus explicitly available;
3. or the same relation content in controlled prose versus a typed edge;
4. while approximately matching position, adjacency, surrounding context, reader instructions, model/settings, tools, candidates, selectors, final integration, coverage, and full end-to-end inference resources.

This is a search-bounded gap, not proof that no such study exists. It substantially weakens any claim that external evidence already validates the proposed package treatment.

### C0003-EXT-09 — Explicit metadata may operate as a misleading cue rather than preserved epistemic structure

The causal effects in `C0003-SRC-02` are not uniformly desirable. Publication time and visual appearance can change answers while the conflicting textual evidence remains the same. A typed support edge could similarly work by attention capture, perceived authority, formatting familiarity, or evaluator alignment rather than by improving evidence reasoning. Therefore a positive treatment effect would require controls such as inert but similarly formatted metadata, incorrect-link corruption, and equivalent-content prose conditions.

### C0003-EXT-10 — Epistemic markers are not stable ground truth for uncertainty

`C0003-SRC-10` defines marker confidence as empirical accuracy conditional on a model using a particular epistemic marker. Across models and multiple QA datasets, marker confidence and marker rankings are more stable within similar distributions and deteriorate under out-of-distribution changes; even strong models show dataset-dependent values. This weakens the idea that labels such as “likely,” “uncertain,” or “hypothesis” can be assumed to carry a fixed quantitative meaning across tasks or stages.

The source studies model-generated confidence markers, not externally assigned protocol categories such as sourced fact or objection. Still, it shows that an epistemic label’s interpretation must be validated rather than presumed.

### C0003-EXT-11 — Annotation reliability is adequate for benchmarking but not sufficient for a fine-grained lineage ontology

FEVER’s κ = 0.6841, AVeriTeC’s κ = 0.619, and CLAIM-BENCH’s moderate-to-substantial re-annotation agreement support feasibility but also reveal nontrivial judgment variance. `C0003-SRC-14` further shows that agreement for structured, multi-object, and free-text annotations depends on the chosen annotation-distance function and can be hard to interpret. A lineage object involving paraphrase, split/merge, scope change, qualification weakening, relation break, and status transition is more complex than a categorical verdict.

No located source validates the exact C0003 transition set or reports reliability for the complete chain from source inventory to package to selected subset to final claim. This weakens any plan to treat an unvalidated lineage codebook as a precise causal outcome.

### C0003-EXT-12 — Better coverage often trades off against false links, noise, or misuse

CLAIM-BENCH reports recall gains from iterative extraction alongside reduced precision and much greater computation. RAGChecker reports that increasing retriever claim recall can improve faithfulness while also increasing generator sensitivity to noise. STORM improves breadth but still exhibits source-bias transfer and over-association of unrelated facts.

These results weaken a monotonic relation-preservation theory. More explicit links or more retained material can improve coverage while increasing false support, spurious dependency, distraction, or confidence in incorrect relations. Relation correctness and coverage must therefore be scored separately.

### C0003-EXT-13 — Closest open-ended systems bundle the hypothesized mechanism with more inference

STORM’s gains cannot be assigned to structured handoffs, relation preservation, multi-perspective questioning, retrieval, outline quality, or extra computation individually. UAlign’s gains cannot be assigned to uncertainty labels independently of sampling, supervised training, reward-model training, and PPO. CLAIM-BENCH’s iterative improvements add multiple calls. Table self-augmentation adds prompt stages. None supplies fixed-compute support for the primary estimand.

## Evidence About Alternative Explanations

### Attention and salience rather than relational reasoning

`C0003-SRC-02`, `C0003-SRC-03`, and `C0003-SRC-04` show that metadata, serialization, order, delimiters, visual appearance, and structural familiarity change outputs. A typed edge may help because it places related items adjacently, shortens a reasoning path, or uses a familiar syntax. A representation experiment must measure position, adjacency, token length, redundancy, and surrounding context, and should include an equivalent controlled-prose relation condition.

### Added information rather than representation

A relation-present package contains information absent from a relation-absent package. FEVER, SciFact, AVeriTeC, and CLAIM-BENCH show that evidence links and rationales are substantive information objects. A positive relation-present result would estimate the value of supplying that information, not a pure formatting benefit. A separate representation comparison is needed to estimate typed edge versus prose.

### Verifier or reference-package privilege

Gold evidence sets in benchmark papers are produced through expert annotation, adjudication, or multi-round validation. Their downstream use is an upper-bound diagnostic and includes human labor and privileged correction. Comparing an agent-written package with such a reference package estimates the combined value of better writing, validation, and corrected metadata unless those costs and inputs are explicitly separated.

### Model-specific format familiarity

Dai et al. report model-specific preferences among graph organizations, and Table Meets LLM reports persistent format effects even for GPT-4. A package schema that helps one reader may harm another. Results should be stratified by reader model and should not be generalized as a universal schema effect.

### Retrieval quality and noise exposure

RAGChecker demonstrates that retrieving more useful claims often retrieves more noise. A typed package may improve final performance because it filters retrieval, or may harm performance by encouraging blind trust in selected context. Observing the selected subset and linking each final claim to used items is necessary to distinguish these mechanisms.

### Task and dependency structure

FEVER, SciFact, AVeriTeC, table tasks, KGQA, and scientific long-form writing impose different dependency structures. Multi-sentence and multi-page evidence is common enough to matter, but no source estimates how a metadata treatment interacts with a predeclared dependency-density measure. Short-answer QA effects should not be assumed to transfer to open-ended synthesis.

### Evaluator-format alignment

Claim-level and structured-schema evaluators may favor outputs that mirror their extraction or entailment format. RAGChecker and CLAIM-BENCH are valuable diagnostics, but their model-based extraction and matching rules can share biases with structured outputs. Human adjudication and format-blinded evaluation remain necessary for key outcomes.

## Fixed-Compute Versus Added-Compute Evidence

No source reports all resources required by the accepted B001 causal gate: package generation, package validation, prompt and context processing, completion tokens, retrieval, tools, candidates, selectors, orchestration, final integration, and saved-budget treatment.

The evidence divides into four categories:

1. **Closest to a matched-call metadata manipulation:** `C0003-SRC-02` swaps publication-time, source, or visual metadata while holding conflicting webpage text and question fixed. This is the strongest near-controlled evidence that metadata changes behavior. It does not report a full token, visual-processing, latency, or monetary-cost ledger, and different visual conditions may induce different effective processing.

2. **Same-call representation comparisons with unequal input geometry:** `C0003-SRC-03` and `C0003-SRC-04` generally use the same model and task while changing representation, but serializations differ in token length, wording, order, density, and sometimes prompt content. These studies isolate representation better than end-to-end systems but do not match total inference resources.

3. **Diagnostics rather than performance interventions:** FEVER, SciFact, AVeriTeC, RAGChecker, CLAIM-BENCH’s benchmark construction, and Braylan et al.’s agreement methods define measurable objects. They do not establish a compute-matched treatment effect.

4. **Explicitly added-compute positive systems:** CLAIM-BENCH’s three-pass and one-by-one strategies add calls; UAlign adds sampling, uncertainty-model training, reward-model training, and PPO; STORM adds retrieval, perspective generation, simulated conversations, curation, and outlining; Table Meets LLM’s self-augmentation adds prompting work. These findings cannot confirm equal-compute superiority of typed packages.

A future C0003 pilot should therefore report at least two estimands if a reference package is used: production performance under the primary budget, and diagnostic upper-bound performance with reference construction and validation cost reported separately. Freed or saved budget must be left unused or reallocated under a predeclared rule.

## Conflicting or Inconclusive Findings

1. **Structured representation can help, but superficial metadata can mislead.** Linearized triples often outperform fluent prose in `C0003-SRC-03`, while publication time and visual appearance in `C0003-SRC-02` can redirect answers without improving textual evidence. Both support treating metadata as active; they conflict on whether the effect should be interpreted as better reasoning.

2. **Explicit uncertainty is feasible, but its meaning is unstable.** `C0003-SRC-09` demonstrates calibrated verbalized probabilities after fine-tuning, and `C0003-SRC-11` reports gains from an uncertainty-alignment pipeline. `C0003-SRC-10` finds epistemic-marker confidence degrades across distributions. The combined evidence supports validation of status metadata, not a universal benefit.

3. **Decomposition improves recall, but not under fixed compute and not without precision costs.** CLAIM-BENCH’s iterative prompting retrieves many more claim–evidence pairs but adds calls and false positives. This is compatible with a write-stage bottleneck, a reader-attention bottleneck, or merely more sampling opportunities.

4. **More retrieval improves information access and worsens noise exposure.** RAGChecker finds higher claim recall associated with greater faithfulness and greater noise sensitivity. A larger or more richly linked package can therefore improve and harm different outcomes simultaneously.

5. **Structured prewriting improves organization and breadth, but can fabricate relations.** STORM’s expert evaluation reports better organization and coverage than its baseline while also identifying source-bias transfer and over-association of unrelated facts. This directly warns against treating a graph or outline as automatically trustworthy.

6. **Benchmark annotations support relation-aware evaluation, but no benchmark supplies full lineage.** FEVER, SciFact, AVeriTeC, and CLAIM-BENCH provide evidence relations and reliability checks. None validates identity across paraphrase, split, merge, compression, retyping, and amplification over multiple stages.

## Source Reliability and Independence

All fourteen ledger entries are primary research sources. Thirteen are peer-reviewed conference, workshop, or journal papers; `C0003-SRC-09` is a TMLR paper with an official author-organization page and OpenReview/arXiv record. Source reliability is generally high for the reported study designs and benchmark facts, but causal transfer is limited by task mismatch and bundled interventions.

Independence constraints:

- FEVER, SciFact, AVeriTeC, and CLAIM-BENCH are separate datasets but share the broad claim-verification and evidence-rationale paradigm. They should not be counted as four independent demonstrations that explicit metadata improves downstream reasoning; they primarily demonstrate measurement feasibility and difficulty.
- CLAIM-BENCH positions itself partly against SciFact’s abstract-level setting. Its full-paper data are new, but the two sources are methodologically related.
- Table Meets LLM evaluates FEVEROUS among its downstream tasks, so that result is not independent of the broader FEVER benchmark family.
- RAGChecker repurposes public datasets across ten domains and evaluates existing RAG systems. Its diagnostic framework is a distinct contribution, but system-level patterns may share data and model families with other RAG studies.
- Teaching Models to Express Their Uncertainty, Revisiting Epistemic Markers, and UAlign form an uncertainty-expression family. UAlign’s positive result is not an independent label-only replication because it uses sampled uncertainty estimates and a trained alignment pipeline.
- Dai et al. and Table Meets LLM both support representation sensitivity, but on different structured data and tasks. They are partially independent evidence for the geometry confound, not direct replications of a claim–support representation effect.
- STORM and KIWI both concern long-form knowledge-intensive writing but use different designs: system comparison with expert article evaluation versus expert-guided revision interactions. They jointly strengthen transfer relevance while leaving the corrected metadata contrast untested.
- Braylan et al. address agreement measurement across general complex annotation types, not claim lineage specifically. It is methodological support, not independent evidence that a C0003 codebook will be reliable.

## Evidence Gaps

1. No located primary study tests one claim–support or qualification metadata type under the corrected metadata-availability contrast with full manipulation and compute controls.
2. No located study compares approximately equivalent claim–support content in controlled prose versus a typed edge while matching position, adjacency, token budget, and reader conditions.
3. No located study performs immutable exact-package replay together with an explicitly logged selected subset and item-level final-use lineage in open-ended research synthesis.
4. No validated annotation scheme was found for the complete C0003 transition set: introduced, preserved, omitted, retyped, contradicted, corrected, mutated, and amplified, including claim split/merge and scope or qualification change.
5. No source identifies package writing as the dominant bottleneck using a predeclared denominator and matched counterfactual packages. Existing evidence only shows that writing, retrieval, and use are all plausible failure points.
6. No source fully accounts for writer and validator effort, prompt and context processing, retrieval, tools, candidates, selectors, final integration, and saved-budget policy.
7. No source tests the corrected contrast specifically in open-ended multi-source research synthesis. STORM and KIWI are transfer-relevant but bundle or observe many other factors.
8. No source establishes a universal minimal package, a universal relation schema, or a model-independent preferred serialization.
9. No source shows that unresolved-question links independently reduce premature closure.
10. No external result isolates role separation or fresh invocation boundaries from the metadata, representation, access, geometry, retrieval, verifier, and compute factors studied here.

## Source Ledger

### C0003-SRC-01

- **Source ID:** C0003-SRC-01
- **Title:** Can AI Validate Science? Benchmarking LLMs on Claim → Evidence Reasoning in AI Papers
- **Authors or organization:** Shashidhar Reddy Javaji, Yupeng Cao, Haohang Li, Yangyang Yu, Nikhil Muralidhar, Zining Zhu
- **Date:** December 2025
- **URL or DOI:** https://aclanthology.org/2025.ijcnlp-long.127/ ; DOI: 10.18653/v1/2025.ijcnlp-long.127
- **Source type:** Peer-reviewed primary benchmark paper, IJCNLP-AACL 2025
- **Claim supported or weakened:** Supports explicit scientific claim–evidence inventories, long-range link scoring, precision/coverage separation, and the difficulty of reconstructing support relations. Weakens fixed-compute claims because three-pass and one-by-one gains add calls and computational cost.
- **Study design and sample:** 346 annotations, 100 AI/ML papers from 2024, 331 unique claims, 335 evidence passages; four PhD annotators, with a separate group re-annotating 30 papers. Six LLMs with ≥128K context, common prompt templates, output schema, matching rules, and deterministic decoding; single-pass, three-pass, and per-claim strategies.
- **Important limitations:** No treatment supplies claim–support metadata to a downstream synthesizer; best claim-identification F1 is 0.59; iterative gains trade precision for recall and are not compute matched; AI-paper domain and under-20-page selection limit transfer.

### C0003-SRC-02

- **Source ID:** C0003-SRC-02
- **Title:** Do Metadata and Appearance of the Retrieved Webpages Affect LLM’s Reasoning in Retrieval-Augmented Generation?
- **Authors or organization:** Cheng-Han Chiang, Hung-yi Lee
- **Date:** November 2024
- **URL or DOI:** https://aclanthology.org/2024.blackboxnlp-1.24/ ; DOI: 10.18653/v1/2024.blackboxnlp-1.24
- **Source type:** Peer-reviewed primary controlled study, BlackboxNLP 2024
- **Claim supported or weakened:** Supports metadata as a causal, active intervention over fixed conflicting text. Weakens the assumption that metadata effects are necessarily epistemically beneficial.
- **Study design and sample:** 355 real controversial yes/no questions with opposed webpages plus 125 GPT-4-generated unknown-entity questions manually examined by an author; ten open and proprietary LLMs. Publication time, source, and visual appearance are swapped between conflicting pages.
- **Important limitations:** Tests non-textual webpage metadata rather than claim–support or qualification links; only three metadata types studied independently; visual conditions can change effective multimodal processing; no full resource ledger.

### C0003-SRC-03

- **Source ID:** C0003-SRC-03
- **Title:** Large Language Models Can Better Understand Knowledge Graphs Than We Thought
- **Authors or organization:** Xinbang Dai, Yuncheng Hua, Tongtong Wu, Yang Sheng, Qiu Ji, Guilin Qi
- **Date:** March 15, 2025
- **URL or DOI:** https://doi.org/10.1016/j.knosys.2025.113060 ; author preprint: https://arxiv.org/abs/2402.11541
- **Source type:** Peer-reviewed primary journal study, Knowledge-Based Systems 312, 113060
- **Claim supported or weakened:** Supports representation sensitivity when relational content is expressed as triples, paths, or natural language; supports noise and incompleteness checks. Does not support claim–support metadata specifically.
- **Study design and sample:** Triple-to-Text experiments on filtered QALD-7 and random 2,000-question samples from LC-QuAD 2.0 and KQAPro, using ChatGPT and Vicuna 7B/13B under fixed model parameters; Text-to-Triple experiments use human-written DocRED documents with manual relation annotations and biologist-curated ChemDisGene abstracts, including multi-hop generated questions.
- **Important limitations:** Serializations differ in length, wording, redundancy, and adjacency; some questions are template-generated or paraphrased by ChatGPT; entity relations are not evidential relations; no full compute accounting; short-answer QA rather than research synthesis.

### C0003-SRC-04

- **Source ID:** C0003-SRC-04
- **Title:** Table Meets LLM: Can Large Language Models Understand Structured Table Data? A Benchmark and Empirical Study
- **Authors or organization:** Yuan Sui, Mengyu Zhou, Mingjie Zhou, Shi Han, Dongmei Zhang
- **Date:** March 2024
- **URL or DOI:** https://doi.org/10.1145/3616855.3635752 ; author PDF: https://www.microsoft.com/en-us/research/uploads/prod/2023/12/wsdm24-SUC.pdf
- **Source type:** Peer-reviewed primary benchmark and empirical study, WSDM 2024
- **Claim supported or weakened:** Supports format, order, delimiter, and prompt effects as confounds in structured-package tests. Self-augmentation results do not isolate representation from added prompting.
- **Study design and sample:** Seven structural-understanding tasks, GPT-3/text-davinci-003 with temperature 0, top_p 1, n = 1; GPT-4 evaluated on random 300-example subsets per task due cost. Tests table formats, content order, role prompting, partition marks, format explanation, and downstream tabular tasks.
- **Important limitations:** Multiple input choices are sometimes combined; token lengths and information geometry are not matched; downstream gains include self-augmentation; FEVEROUS results overlap the FEVER family; no research-synthesis task.

### C0003-SRC-05

- **Source ID:** C0003-SRC-05
- **Title:** RAGChecker: A Fine-grained Framework for Diagnosing Retrieval-Augmented Generation
- **Authors or organization:** Dongyu Ru, Lin Qiu, Xiangkun Hu, Tianhang Zhang, Peng Shi, Shuaichen Chang, Cheng Jiayang, Cunxiang Wang, Shichao Sun, Huanyu Li, Zizhao Zhang, Binjie Wang, Jiarong Jiang, Tong He, Zhiguo Wang, Pengfei Liu, Yue Zhang, Zheng Zhang
- **Date:** 2024
- **URL or DOI:** https://proceedings.neurips.cc/paper_files/paper/2024/hash/27245589131d17368cccdfa990cbf16e-Abstract.html ; DOI: 10.52202/079017-0692 ; repository: https://github.com/amazon-science/RAGChecker
- **Source type:** Peer-reviewed primary evaluation framework, NeurIPS 2024 Datasets and Benchmarks
- **Claim supported or weakened:** Supports explicit separation of retrieval coverage/precision from generator use, noise sensitivity, hallucination, and faithfulness. Does not observe package writing.
- **Study design and sample:** Claim-level entailment metrics, human-judgment meta-evaluation, eight RAG systems across a benchmark spanning ten domains; diagnostic comparisons of retrievers, generators, chunk size, and top-k retrieval.
- **Important limitations:** Ground-truth answers and evaluator models are required; claim extraction and entailment can introduce model bias; benchmark datasets are repurposed; retrieval is observed but package write loss is outside scope.

### C0003-SRC-06

- **Source ID:** C0003-SRC-06
- **Title:** FEVER: a Large-scale Dataset for Fact Extraction and VERification
- **Authors or organization:** James Thorne, Andreas Vlachos, Christos Christodoulopoulos, Arpit Mittal
- **Date:** June 2018
- **URL or DOI:** https://aclanthology.org/N18-1074/ ; DOI: 10.18653/v1/N18-1074
- **Source type:** Peer-reviewed primary dataset and benchmark paper, NAACL 2018
- **Claim supported or weakened:** Supports claim labels tied to evidence sets, multi-sentence and multi-page dependency measurement, and reported annotation reliability.
- **Study design and sample:** 185,445 Wikipedia-derived claims; 4%/7,506 claims annotated by five annotators; Supported, Refuted, and NotEnoughInfo labels; evidence retrieval and label-plus-evidence benchmark scoring.
- **Important limitations:** Claims are generated by altering Wikipedia sentences; factoid setting; no cross-stage transformation or metadata treatment; moderate rather than near-perfect agreement.

### C0003-SRC-07

- **Source ID:** C0003-SRC-07
- **Title:** Fact or Fiction: Verifying Scientific Claims
- **Authors or organization:** David Wadden, Shanchuan Lin, Kyle Lo, Lucy Lu Wang, Madeleine van Zuylen, Arman Cohan, Hannaneh Hajishirzi
- **Date:** November 2020
- **URL or DOI:** https://aclanthology.org/2020.emnlp-main.609/ ; DOI: 10.18653/v1/2020.emnlp-main.609
- **Source type:** Peer-reviewed primary scientific fact-verification benchmark, EMNLP 2020
- **Claim supported or weakened:** Supports scientific claim–evidence rationale objects and separate retrieval, rationale-selection, and verdict-use checkpoints.
- **Study design and sample:** 1,409 expert-annotated scientific claims against 5,183 abstracts; label-only and label-plus-rationale metrics; VERISCI baseline with abstract retrieval, rationale selection, and label prediction.
- **Important limitations:** Claims are verified against abstracts rather than full papers or multiple open-web sources; no package writing stage; no structured-versus-prose intervention; pipeline components are trained rather than fixed-prompt readers.

### C0003-SRC-08

- **Source ID:** C0003-SRC-08
- **Title:** AVeriTeC: A Dataset for Real-world Claim Verification with Evidence from the Web
- **Authors or organization:** Michael Schlichtkrull, Zhijiang Guo, Andreas Vlachos
- **Date:** 2023
- **URL or DOI:** https://arxiv.org/abs/2305.13117 ; DOI: 10.52202/075280-2842
- **Source type:** Peer-reviewed primary real-world fact-verification dataset, NeurIPS 2023 Datasets and Benchmarks
- **Claim supported or weakened:** Supports predeclared intermediate questions, evidence-backed answers, and justifications connecting evidence to verdicts in a real-world web setting.
- **Study design and sample:** 4,568 real-world claims drawn from 50 fact-checking organizations; multi-round annotation; evidence available before the claim date; question–answer evidence and textual justifications; verdict agreement κ = 0.619.
- **Important limitations:** Fact-checking verdict task rather than open-ended research synthesis; QA decomposition may encode annotator reasoning choices; no metadata-format experiment or full lineage across generated stages.

### C0003-SRC-09

- **Source ID:** C0003-SRC-09
- **Title:** Teaching Models to Express Their Uncertainty in Words
- **Authors or organization:** Stephanie Lin, Jacob Hilton, Owain Evans
- **Date:** 2022
- **URL or DOI:** https://arxiv.org/abs/2205.14334 ; official overview: https://openai.com/index/teaching-models-to-express-their-uncertainty-in-words/
- **Source type:** Peer-reviewed primary journal paper, Transactions on Machine Learning Research
- **Claim supported or weakened:** Supports feasibility of verbalized and numeric confidence metadata after fine-tuning and evaluates calibration under distribution shift.
- **Study design and sample:** GPT-3 fine-tuning to output answers with confidence; CalibratedMath tasks; comparison of verbalized probabilities with logit-derived uncertainty; in-distribution and shifted evaluations.
- **Important limitations:** Confidence expression rather than protocol epistemic categories; fine-tuning intervention; no downstream reader receives the labels; no claim-support links or fixed inference-compute package comparison.

### C0003-SRC-10

- **Source ID:** C0003-SRC-10
- **Title:** Revisiting Epistemic Markers in Confidence Estimation: Can Markers Accurately Reflect Large Language Models’ Uncertainty?
- **Authors or organization:** Jiayu Liu, Qing Zong, Weiqi Wang, Yangqiu Song
- **Date:** July 2025
- **URL or DOI:** https://aclanthology.org/2025.acl-short.18/ ; DOI: 10.18653/v1/2025.acl-short.18
- **Source type:** Peer-reviewed primary empirical study, ACL 2025 Short Papers
- **Claim supported or weakened:** Weakens assumptions that verbal epistemic markers have stable meanings across datasets; supports explicit in-distribution and out-of-distribution validation of status labels.
- **Study design and sample:** Multiple QA datasets and open/proprietary models; defines marker confidence as accuracy conditional on marker use and introduces seven metrics for marker stability, ranking, and accuracy association.
- **Important limitations:** Model-generated markers rather than externally assigned claim types; QA rather than research synthesis; marker frequency and model style can affect estimates.

### C0003-SRC-11

- **Source ID:** C0003-SRC-11
- **Title:** UAlign: Leveraging Uncertainty Estimations for Factuality Alignment on Large Language Models
- **Authors or organization:** Boyang Xue, Fei Mi, Qi Zhu, Hongru Wang, Rui Wang, Sheng Wang, Erxin Yu, Xuming Hu, Kam-Fai Wong
- **Date:** July 2025
- **URL or DOI:** https://aclanthology.org/2025.acl-long.299/ ; DOI: 10.18653/v1/2025.acl-long.299
- **Source type:** Peer-reviewed primary method paper, ACL 2025
- **Claim supported or weakened:** Supports uncertainty representations as useful components in a trained factuality-alignment pipeline; weakens label-only interpretation because the intervention bundles sampling, estimator training, reward modeling, and PPO.
- **Study design and sample:** UAlign data include 76,523 TriviaQA training and 9,960 development QA examples plus other QA evaluations; multiple sampled responses estimate confidence and semantic entropy; uncertainty estimators, reward model, and Llama-3/Mistral policy models are trained, followed by PPO.
- **Important limitations:** Added training and inference resources; known/refuse-unknown QA outcome; ground-truth answers used in confidence construction; no isolated metadata field or research-synthesis handoff.

### C0003-SRC-12

- **Source ID:** C0003-SRC-12
- **Title:** Assisting in Writing Wikipedia-like Articles From Scratch with Large Language Models
- **Authors or organization:** Yijia Shao, Yucheng Jiang, Theodore Kanell, Peter Xu, Omar Khattab, Monica Lam
- **Date:** June 2024
- **URL or DOI:** https://aclanthology.org/2024.naacl-long.347/ ; DOI: 10.18653/v1/2024.naacl-long.347
- **Source type:** Peer-reviewed primary system and evaluation paper, NAACL 2024
- **Claim supported or weakened:** Supports structured prewriting, coverage-sensitive expert evaluation, and transfer relevance to multi-source long-form synthesis; reports source-bias transfer and fabricated connections that weaken naive graph/outline trust.
- **Study design and sample:** STORM performs perspective discovery, web retrieval, simulated writer–expert questioning, information curation, outline construction, and article generation; evaluated on 100 FreshWiki topics with experienced Wikipedia editors against an outline-driven RAG baseline.
- **Important limitations:** Components, roles, retrieval, prompts, and added calls are bundled; no fixed-compute comparison; no single metadata treatment; Wikipedia-like writing differs from branch research reports.

### C0003-SRC-13

- **Source ID:** C0003-SRC-13
- **Title:** KIWI: A Dataset of Knowledge-Intensive Writing Instructions for Answering Research Questions
- **Authors or organization:** Fangyuan Xu, Kyle Lo, Luca Soldaini, Bailey Kuehl, Eunsol Choi, David Wadden
- **Date:** August 2024
- **URL or DOI:** https://aclanthology.org/2024.findings-acl.770/ ; DOI: 10.18653/v1/2024.findings-acl.770
- **Source type:** Peer-reviewed primary dataset and observational study, Findings of ACL 2024
- **Claim supported or weakened:** Supports transfer relevance of new-information incorporation, precise-edit, and self-evaluation failures in scientific long-form writing.
- **Study design and sample:** 1,260 turns from 234 expert-guided sessions with GPT-4, GPT-3.5, and Llama-2-70B-chat; each turn includes instruction, model response, and human evaluation using relevant scientific papers.
- **Important limitations:** No randomized package conditions, explicit retrieval checkpoint, or claim-lineage annotation; iterative expert instructions differ across sessions; compute is not matched.

### C0003-SRC-14

- **Source ID:** C0003-SRC-14
- **Title:** Measuring Annotator Agreement Generally across Complex Structured, Multi-object, and Free-text Annotation Tasks
- **Authors or organization:** Alexander Braylan, Omar Alonso, Matthew Lease
- **Date:** April 2022
- **URL or DOI:** https://doi.org/10.1145/3485447.3512242
- **Source type:** Peer-reviewed primary methodological study, The Web Conference 2022
- **Claim supported or weakened:** Supports use of task-appropriate distance-based agreement methods for structured lineage objects and warns that agreement depends on annotation distance and interpretability choices.
- **Study design and sample:** Evaluates agreement measurement across seven task types, including text sequence tagging, ranked lists, free-text translations, numeric vectors, syntax trees, image boxes, and keypoints; compares generalized Krippendorff-style approaches and proposes two more interpretable measures.
- **Important limitations:** Does not define or validate claim lineage; task examples are not research-package transitions; choosing the distance function remains a substantive ontology decision.

## Handoff to Alternative Theorist and Integrator

The strongest defensible external conclusion is methodological, not a winning theory: explicit metadata and relational representation can materially alter model behavior, and claim–support relations can be annotated and evaluated, but the direction and mechanism of the effect are not established for a B001 package. Metadata can improve accessibility, act as an attention cue, add genuinely new relational information, or mislead through superficial authority and format effects.

The Alternative Theorist should therefore examine at least four live accounts:

1. **Relation-information account:** explicit claim–support or qualification metadata helps because it supplies information that a flat package lacks.
2. **Representation/geometry account:** typed fields help or harm because of ordering, adjacency, compactness, delimiters, and model-specific format familiarity, even when relation content is approximately equivalent.
3. **Authority-cue account:** labels and links change answers through trust, recency, appearance, or evaluator-format alignment rather than better evidence reasoning.
4. **Null or reader-bottleneck account:** once relation content, geometry, and compute are controlled, the downstream reader may still fail to use the metadata, leaving no benefit.

The Integrator should not accept an external effect claim for typed claim–support packages. A narrow pilot is externally justified only as an unresolved experiment. The cleanest first pair of contrasts remains:

- **Metadata availability:** fixed base claims, one predeclared claim–support or qualification relation absent versus explicitly supplied.
- **Metadata representation:** the same predeclared relation conveyed in controlled prose versus a typed field or edge.

Both need correctness checks, inert-structure and corrupted-link controls, package hash and surrounding-context records, explicit selected-subset logging, claim-level final-use lineage, coverage and task-completion gates, blinded evaluation, reliability reporting, and a declared full resource and saved-budget rule. A reference package should be treated as a separately costed diagnostic upper bound, not as a matched production condition. The cycle should preserve the evidence gap: no located source tests this corrected contrast in open-ended multi-source research synthesis under fixed end-to-end compute.