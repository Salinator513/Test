# External Evidence Researcher — C0001

## Research Scope

This report investigates the narrow estimand requested by the Critic and Internal Evidence Researcher: the marginal effect of fresh role-separated execution after holding model, task, functional stages, stage instructions, artifacts, information access, tools, evaluator, and inference budget constant.

No located study satisfies that estimand exactly. The closest evidence falls into four classes:

1. near-direct comparisons of single-agent and multi-agent architectures under matched reasoning-token budgets;
2. budget-aware comparisons of debate, reflection, search, and self-consistency strategies;
3. mechanism studies on context degradation, verification, external memory, output correlation, coordination failure, and task decomposability;
4. evaluation studies on atomic factual support, citation correctness/completeness, and factual coverage.

The report therefore distinguishes direct evidence from adjacent evidence and does not treat positive results obtained with more calls, samples, retrieval, tools, or tokens as proof of an independent role-separation effect.

## Search Questions

1. Do primary studies compare fresh role-separated invocations with a staged single-model workflow while matching model, task, stage functions, information, tools, and inference compute?
2. Which studies separately vary invocation boundaries, structured memory, verification or critique, role specialization, or handoff topology?
3. How is fixed compute operationalized: requested tokens, actual tokens, input plus output tokens, calls, monetary cost, tool calls, or wall-clock time?
4. Which studies measure unsupported claims, factual support, citation support, factual coverage, contradiction, or error propagation?
5. Which matched or budget-aware studies report null or negative multi-agent results?
6. What evidence exists that same-base-model agents make correlated or redundant errors?
7. Do role or component ablations distinguish removing compute from reallocating it?

## Search Method and Source Hierarchy

Searches targeted combinations of: multi-agent versus single-agent; equal or fixed token budget; role specialization; multi-agent debate; self-refinement; verifier and critic ablation; context degradation; agent memory; correlated agent outputs; factuality metrics; atomic claims; citation correctness; and error propagation.

Priority was given to peer-reviewed conference papers, original-author preprints, official publication pages, and original benchmark or code repositories. Secondary pages were used only to locate primary material and are not included in the source ledger. Sources were screened for model conditions, task sample, architecture, information access, budget accounting, evaluator design, and whether claimed gains could be explained by extra inference.

Evidence is classified as follows:

- **Near-direct:** model and task are matched, and a primary inference budget is explicitly controlled, but prompts, message structures, or other architectural features still differ.
- **Budget-aware adjacent:** resource-performance curves or cost controls are reported, but the target factor is bundled with other workflow differences.
- **Mechanism evidence:** isolates a related mechanism such as independent verification, external memory, diversity, or coordination loss, without isolating fresh role separation.
- **Measurement evidence:** provides outcome definitions or evaluators relevant to unsupported claims and provenance, but does not compare workflows.

Sixteen primary sources are used. No forum, social-media, or informal-user report is used as factual confirmation.

## Evidence Supporting the Main Direction

The evidence supports only a conditional version of the main direction, not a general role-separation advantage.

### C0001-EXT-01 — Structured partitioning can help when a unified context is materially degraded

Tran and Kiela provide the closest controlled evidence for a context-partition mechanism. Under a fixed 1,000-thinking-token budget on MuSiQue with Qwen3-30B-A3B, a sequential multi-agent pipeline overtook the single-agent pipeline under heavy masking and substitution corruption. It did not consistently overtake it under deletion or added distractors. This supports the narrower hypothesis that structured intermediate messages can filter or stabilize reasoning when effective single-context utilization is damaged. It does not show that fresh conversations or role labels are independently causal, because the sequential condition also changes prompts, decomposition, message passing, and aggregation.

### C0001-EXT-02 — Coordination can help when the task naturally decomposes into parallel evidence streams

Kim et al. report a controlled agentic evaluation with matched total reasoning-token budgets, shared task prompts, standardized tools, common observation structures, and consistent context truncation. Centralized coordination substantially improved decomposable financial-analysis tasks, while decentralized coordination helped dynamic web navigation. Their trace analysis attributes benefits to parallel information gathering and validation bottlenecks. This supports task-conditional value for decomposition and centralized verification. It does not isolate fresh invocation boundaries, and the work remains a preprint.

### C0001-EXT-03 — Explicit adversarial and verification stages can improve outcomes, although usually with added inference

Du et al. found that three same-model agents debating for two rounds improved arithmetic, GSM8K, chess, MMLU, and biography factuality relative to single-pass and reflection baselines. For example, reported arithmetic accuracy rose from 67.0% for the single-agent condition to 81.8% for debate, and biography factual accuracy rose from 66.0% to 73.8%. These are positive primary results for structured interaction, but the debate condition uses multiple agents and rounds and therefore more inference.

Dhuliawala et al.'s Chain-of-Verification is important because it obtains factuality gains with one model performing staged draft, verification-question planning, independent question answering, and final revision. The independent answering step is designed to avoid conditioning verification answers on the draft. The method reduces hallucinations on Wikidata list questions, closed-book MultiSpanQA, and long-form generation. This supports structured verification and partial context isolation, but weakens any claim that nominal multi-agent identity is necessary.

Tyen et al. similarly separate mistake finding from correction. Across five reasoning tasks, models were poor at locating mistakes but could correct them when supplied the error location; a small out-of-domain classifier located mistakes better than prompting a large model. This supports a dedicated verification signal or deterministic checker as a potentially valuable component, rather than role count by itself.

### C0001-EXT-04 — Externalized memory can improve long-horizon agent performance

Agent Workflow Memory induces reusable workflows and supplies them to later agent runs. On Mind2Web and WebArena, it reports 24.6% and 51.1% relative success-rate improvements over its baselines and fewer steps on successfully solved WebArena tasks. This is direct evidence that structured external memory can be an active ingredient. It is not a role-separation study, and offline memory may use annotated examples while online memory adds induction and retrieval work.

### C0001-EXT-05 — Diversity, rather than agent count, can create complementary evidence

Yang et al. measure pairwise embedding similarity and an effective-channel metric across vote and debate systems using Qwen-2.5-7B, Llama-3.1-8B, and Mistral-7B on seven reasoning and knowledge benchmarks. Homogeneous outputs become increasingly redundant as agent count rises; heterogeneous models, prompts, or tools preserve lower similarity, and two diverse agents can match or exceed sixteen homogeneous agents in their tested settings. This supports the protocol's concern that same-model agreement is correlated rather than independent evidence. It also suggests role prompts may help only when they induce task-relevant, correct-path diversity.

## Evidence Weakening the Main Direction

### C0001-EXT-06 — The closest matched-budget comparison finds no general role-separated advantage

Tran and Kiela compare a single-agent system with sequential, subtask-parallel, parallel-role, debate, and ensemble multi-agent systems across FRAMES and four-hop MuSiQue, using Qwen3-30B-A3B, DeepSeek-R1-Distill-Llama-70B, Gemini 2.5 Flash, and Gemini 2.5 Pro. Budgets range from 100 to 10,000 thinking tokens. Except for the effectively non-reasoning 100-token regime, the single-agent system is best or statistically indistinguishable from the best system across model families and datasets, and often consumes fewer actual thinking tokens. The parallel-role condition explicitly includes Solver, Fact Extractor, Skeptic, and Second Solver roles, yet does not show an independent advantage.

This is the strongest weakening evidence, although its compute accounting excludes prompt and final-answer tokens, planners and aggregators are only kept "near budget-neutral," actual token use is not forced to equal the cap, and the single-agent and multi-agent prompts are not functionally identical.

### C0001-EXT-07 — Budget-aware baselines often explain gains attributed to complex workflows

Wang et al. evaluate seven reasoning strategies on GSM8K, MATH, TheoremQA, CommonsenseQA, HotpotQA, and Game of 24 using GPT-3.5 and GPT-4, with 100 sampled test items per dataset. For multi-agent debate, six agents and three rounds produce 18 calls; the self-consistency baseline receives up to 20 independent samples. They report performance against query count, input-plus-output tokens, and monetary cost. At comparable budgets, chain-of-thought self-consistency matches or beats multi-agent debate and Reflexion across the five main datasets; debate diversity falls across rounds, while dependent sampling can propagate mistakes. This strongly supports added sampling and budget allocation as alternative explanations.

### C0001-EXT-08 — Multi-agent debate is highly sensitive and does not reliably beat simpler baselines

Smit et al. benchmark Society of Mind, Multi-Persona, ChatEval, self-consistency, ensemble refinement, Medprompt, and single-agent prompting on seven datasets, primarily with GPT-3.5-turbo, and report accuracy against dollar cost, calls, prompt length, and time. Untuned debate protocols do not reliably outperform self-consistency or ensembling and generally cost more. Hyperparameter tuning and agreement modulation can improve some debate protocols, but this demonstrates sensitivity rather than a stable role effect. Their comparisons are cost-aware rather than a strict equal-token factor isolation.

### C0001-EXT-09 — Coordination can amplify error and fragment sequential reasoning

Kim et al. report that all tested multi-agent variants degraded sequential PlanCraft performance by roughly 39–70% under fixed computational budgets. Independent-agent architectures produced much more error amplification than centralized architectures because mistakes propagated without a validation bottleneck. Multi-agent overhead also hurt tool-heavy tasks by splitting a fixed token budget across coordination and execution.

Cemri et al. analyze 1,642 traces from seven multi-agent frameworks across coding, mathematics, and general-agent tasks. Their taxonomy identifies specification and design failures, inter-agent misalignment, and verification or termination failures, including repetition, context loss, information withholding, and premature termination. Role-specification and workflow interventions improved selected systems by up to 9.4% and 15.6%, but completion remained low and failures were not eliminated. This is evidence that role interfaces can introduce new cumulative-error pathways.

### C0001-EXT-10 — Same-model critique is not a dependable verifier

Huang et al. find that intrinsic self-correction without external feedback often fails to improve reasoning and can turn correct answers into incorrect ones. Tyen et al. identify mistake localization as a particular weakness. Wang et al. report that GPT-4 was strongly biased toward accepting correct-looking answers but poor at recognizing incorrect answers on several datasets; an oracle evaluator substantially outperformed model self-evaluation in Reflexion ablations. A critic role using the same base model therefore cannot be assumed to provide independent or accurate error detection.

## Evidence About Alternative Explanations

### Added sampling and voting

Self-consistency samples multiple independent reasoning paths and selects the most consistent answer. Wang et al. (ICLR 2023) report large gains on GSM8K, SVAMP, AQuA, StrategyQA, and ARC-Challenge. This mechanism can reproduce an apparent "many agents" gain without role specialization, handoffs, or fresh epistemic perspectives. The budget-aware EMNLP study finds independent sampling often uses compute more effectively than dependent debate rounds.

### Structured stages rather than agent identity

Self-Refine uses one model as generator, feedback provider, and refiner and reports approximately 20 percentage points of average absolute improvement across seven tasks. Chain-of-Verification uses one model with separated verification stages and reduces hallucinations. These studies support C0001-EXP-03 more directly than C0001-EXP-01: mandatory generation, challenge, evidence, and revision passes may matter even when no distinct agent identity exists. Both add inference relative to a one-pass baseline.

### External memory and workflow retrieval

Agent Workflow Memory improves long-horizon web navigation by supplying reusable workflow records. This supports C0001-EXP-02 as a plausible alternative mechanism. No located study holds memory content and construction cost identical while varying only fresh role-separated execution.

### Task decomposability and search breadth

Kim et al. find positive coordination effects on parallelizable financial research and dynamic web navigation, but large negative effects on sequential planning. Tran and Kiela's error analysis similarly finds that multi-agent breadth helps when it surfaces entities missed by a narrow single path, but hurts when exploration drifts and the aggregator loses a correct candidate. Task structure and the need for breadth are therefore strong moderators.

### Output diversity and error correlation

Yang et al. show that homogeneous agents produce increasingly similar outputs and diminishing returns. Wang et al. show debate-round entropy declining as agents condition on each other. These findings suggest that repeated same-model roles are not independent evidence and may become less diverse through interaction. Prompt or model heterogeneity can help, but semantic diversity is only a proxy and diversity among incorrect paths can be harmful.

### Evaluator and verifier quality

Wang et al.'s Tree-of-Thought and Reflexion ablations show that evaluator quality materially changes outcomes; a weaker but cheap evaluator can sometimes preserve most performance, while a random or inaccurate evaluator sharply degrades it. Tyen et al. show a small trained mistake locator can outperform prompted large models. Apparent critic-role value may therefore arise from the quality and information of the verification signal rather than separation into another invocation.

### Factuality metric choice and response coverage

FActScore decomposes long-form text into atomic facts and measures the percentage supported by a knowledge source. This is a usable claim-level precision measure, but a system can improve it by making fewer claims. SAFE adds an F1@K measure that balances supported-fact precision with a preferred response length, providing one way to discourage winning by terseness. ALCE separately evaluates citation correctness and citation completeness, showing that citation presence is not equivalent to complete support. None of these metrics traces an error's lineage through workflow stages.

## Fixed-Compute Versus Added-Compute Evidence

### Near-direct fixed-budget evidence

- **Tran and Kiela:** global requested thinking-token caps of 100, 500, 1,000, 2,000, 5,000, and 10,000 are divided across multi-agent workers. Prompt tokens, final answers, state construction, and most planner or aggregator overhead are excluded. Actual consumption can differ, especially for Gemini. This is a matched upper-cap comparison, not equal total inference cost.
- **Kim et al.:** all systems are reported as matched at a mean of 4,800 reasoning tokens per trial and equal tool access, with common task prompts, tool interfaces, observation structures, and truncation policies. Coordination messages consume the common budget. Architecture-specific orchestration and role prompts still differ, and some benchmark subsets are small: 20 SWE-bench Verified and 20 Terminal-Bench instances.
- **Wang et al. (EMNLP 2024):** compares performance as a function of query count, total input-plus-output tokens, and cost. Multi-agent debate receives 18 calls and self-consistency up to 20. Matching is on observed resource curves, not identical prompts or information structures.

### Cost-aware but not strictly matched evidence

- **Smit et al.:** reports accuracy-cost-call-time trade-offs over many protocols and hyperparameters, but each protocol uses different message histories, prompts, rounds, and summarization choices.
- **Du et al.:** reports agent and round scaling and acknowledges higher generation cost. The positive debate results are added-compute evidence.

### Clearly added-compute evidence

- **Self-Consistency:** adds independent sampled reasoning paths.
- **Self-Refine:** adds feedback and revision calls.
- **Chain-of-Verification:** adds verification-question planning, independent answers, and final revision.
- **Agent Workflow Memory:** adds workflow induction, storage, selection, and prompt context; offline variants can use annotated examples.
- **Multiagent Debate (Du et al.):** adds agents and rounds.

### Ablation interpretation

The located literature rarely distinguishes the two branch-required ablations cleanly:

1. remove a role and leave its compute unused, measuring the combined role-plus-compute contribution;
2. remove a role and reallocate its budget to remaining stages, measuring replaceability under a fixed budget.

Tran and Kiela reallocate a common thinking cap across architectures, and Kim et al. operate under a shared total budget, but neither performs the branch's exact one-role-at-a-time deletion under both accounting rules. Wang et al. partition proposer and evaluator budgets in Tree-of-Thought and Reflexion, which is useful component evidence but not a full role-loop ablation.

## Conflicting or Inconclusive Findings

1. **Debate gains conflict with matched-budget results.** Du et al. report sizable gains from debate, whereas Smit et al. find untuned debate unreliable, Wang et al. find self-consistency superior at comparable budget, and Tran and Kiela find single agents best or tied under matched thinking-token caps. The conflict is substantially explained by added inference, protocol tuning, datasets, and model versions, but not fully resolved.
2. **Self-refinement findings are task- and signal-dependent.** Self-Refine reports broad average gains, while Huang et al. find intrinsic reasoning self-correction can degrade accuracy. Tyen et al. reconcile part of this by showing correction is effective after an error is located, but mistake finding is weak. The critical variable may be verifier information, not merely a revision role.
3. **Heterogeneity results are not uniform.** Yang et al. find strong gains from model, prompt, and tool diversity on seven static benchmarks with 7B–8B models. Kim et al.'s preliminary heterogeneous agentic configurations do not bypass capability saturation and often underperform teams built around the strongest model. Static voting or debate and long-horizon tool use may behave differently.
4. **Context partitioning has both benefits and costs.** Tran and Kiela find crossovers under severe masking and substitution, but ordinary clean-context results favor unified single-agent reasoning. Cemri et al. identify context loss and information withholding as observed multi-agent failures. There is no clean fresh-context-only ablation.
5. **Provenance metrics disagree on what counts as success.** FActScore measures atomic support precision; ALCE separates citation correctness from completeness; SAFE adds a length-based recall proxy. Higher citation count or traceability alone cannot establish correct support, sufficient coverage, or sound synthesis.
6. **No study measures the target cumulative-error construct end to end.** Existing work measures final accuracy, execution-trace failure categories, error amplification ratios, atomic factual support, or citation quality. No located source predefines an error lineage that records introduction, preservation, correction, mutation, and amplification across a research loop.

## Source Reliability and Independence

The ledger contains sixteen primary sources: peer-reviewed conference papers, original-author preprints, and original benchmark or system papers. The strongest direct evidence comes from two recent preprints, Tran and Kiela and Kim et al.; their controlled designs are highly relevant, but peer review and broader replication remain pending.

Independence is limited in several clusters:

- Du, Smit, and Wang et al. evaluate overlapping debate concepts and reuse several common reasoning datasets; they are separate experiments but not fully independent task evidence.
- Huang and Tyen address the same self-correction controversy, and Tyen explicitly decomposes a failure reported by Huang.
- FActScore and SAFE share atomic-fact evaluation concepts; SAFE extends the precision-only framing with a recall proxy.
- Several studies use GPT-family models and LLM-as-judge evaluation, creating shared model and evaluator biases.
- Tran and Kiela's FRAMES and MuSiQue evidence is independent of Kim et al.'s six agentic tool-use benchmarks, making their shared conclusion about coordination overhead more informative than repeated results on one dataset family.

No source in the ledger is treated as independent confirmation merely because multiple agents or repeated samples agree.

## Evidence Gaps

1. No located study holds stage prompts, role instructions, external state, information set, tools, evaluator, and full inference cost constant while varying only fresh invocation boundaries.
2. No direct experiment compares persistent staged execution with fresh staged execution using identical intermediate artifacts and message content.
3. No study cleanly ablates handoff compression while preserving the same information and compute.
4. No fixed-budget study tests explicit claim labels and provenance ledgers as a factor within role-separated versus persistent workflows.
5. No located role ablation reports both budget-removed and budget-reallocated results for every stage.
6. No direct study measures unsupported claims normalized by factual coverage on multi-stage research synthesis while also scoring task usefulness or completeness.
7. No direct study verifies citation support, tracks contradiction, and traces error lineage at every workflow stage.
8. Same-base-model output correlation is measured in voting and debate settings, but not in the exact role-separated-versus-persistent staged contrast.
9. Evaluator independence remains weak: many studies use an LLM judge, sometimes from the same model family, and few report blinded multi-rater adjudication for fine-grained claim support.
10. Prompt, input-context, final-answer, tool-call, retrieval, state-maintenance, and orchestration costs are rarely included in one complete compute ledger.
11. Positive external-memory studies add information or learned workflows; they do not show whether structured memory replaces the value of role separation under equal information.
12. Evidence on open-ended research synthesis is sparse. Most direct comparisons use short-answer reasoning, static QA, or tool-execution benchmarks rather than multi-source research reports.

## Source Ledger

### C0001-SRC-01

- **Title:** Single-Agent LLMs Outperform Multi-Agent Systems on Multi-Hop Reasoning Under Equal Thinking Token Budgets
- **Authors or organization:** Dat Tran; Douwe Kiela, Stanford University
- **Date:** 2026-04-11, arXiv v2
- **URL or DOI:** https://arxiv.org/abs/2604.02460 ; https://doi.org/10.48550/arXiv.2604.02460
- **Source type:** Original-author preprint; near-direct matched-budget comparison
- **Design and conditions:** FRAMES and four-hop MuSiQue; Qwen3-30B-A3B, DeepSeek-R1-Distill-Llama-70B, Gemini 2.5 Flash and Pro; single agent versus sequential, subtask-parallel, parallel-role, debate, and ensemble architectures; six requested thinking-token caps; common LLM-judge rubric with ground-truth answers.
- **Claim supported or weakened:** Strongly weakens a general independent role-separation benefit; conditionally supports structured partitioning under severely corrupted effective context.
- **Important limitations:** Thinking tokens exclude prompts and final answers; planner and aggregator overhead is not fully charged; actual usage can be below caps; prompts and information flow differ; text-only multi-hop tasks; LLM judge; no external tools or provenance outcomes.

### C0001-SRC-02

- **Title:** Towards a Science of Scaling Agent Systems
- **Authors or organization:** Yubin Kim et al.; Google Research, Google DeepMind, MIT, and collaborators
- **Date:** 2026-04-08, arXiv v3; first posted 2025-12-09
- **URL or DOI:** https://arxiv.org/abs/2512.08296 ; https://doi.org/10.48550/arXiv.2512.08296
- **Source type:** Original-author preprint; controlled agentic architecture benchmark
- **Design and conditions:** 260 configurations; six benchmarks; single, independent, centralized, decentralized, and hybrid architectures; three LLM families; identical task prompts, standardized tools, common observation structures, consistent truncation, and mean 4,800 reasoning-token budget per trial.
- **Claim supported or weakened:** Supports task-conditional coordination and centralized verification; weakens universal role separation and shows coordination overhead and error amplification.
- **Important limitations:** Architecture-specific orchestration remains bundled; role prompts differ; some benchmark subsets contain only 20 instances; preprint; prompt optimization was not architecture-specific; absolute cross-domain prediction is limited.

### C0001-SRC-03

- **Title:** Reasoning in Token Economies: Budget-Aware Evaluation of LLM Reasoning Strategies
- **Authors or organization:** Junlin Wang, Siddhartha Jain, Dejiao Zhang, Baishakhi Ray, Varun Kumar, Ben Athiwaratkun
- **Date:** 2024-11
- **URL or DOI:** https://aclanthology.org/2024.emnlp-main.1112/ ; https://doi.org/10.18653/v1/2024.emnlp-main.1112
- **Source type:** Peer-reviewed EMNLP paper; budget-aware comparison and component ablation
- **Design and conditions:** Seven reasoning strategies; five main datasets plus Game of 24; five models including GPT-3.5 and GPT-4; 100 sampled items per dataset; query, token, and monetary budgets; multi-agent debate, Reflexion, Tree-of-Thought, and self-consistency comparisons.
- **Claim supported or weakened:** Weakens claims that debate or reflection gains are architectural; supports independent sampling and evaluator quality as alternative explanations.
- **Important limitations:** Small 100-item samples; API-era models; compared methods retain different prompts and information; no role-separated research task; no claim-level factuality or provenance scoring.

### C0001-SRC-04

- **Title:** Should we be going MAD? A Look at Multi-Agent Debate Strategies for LLMs
- **Authors or organization:** Andries Petrus Smit, Nathan Grinsztajn, Paul Duckworth, Thomas D. Barrett, Arnu Pretorius
- **Date:** 2024-07
- **URL or DOI:** https://proceedings.mlr.press/v235/smit24a.html
- **Source type:** Peer-reviewed ICML paper; broad debate benchmark
- **Design and conditions:** Multiple debate and non-debate protocols across seven reasoning and knowledge datasets; GPT-3.5-turbo primary, with supplementary GPT-4 and Mixtral conditions; accuracy, monetary cost, calls, and time considered.
- **Claim supported or weakened:** Weakens reliable general debate benefits; supports protocol sensitivity and the possibility that controlled disagreement matters.
- **Important limitations:** Not a strict equal-token design; many hyperparameters; mostly one older API model; overlapping datasets and methods with other debate papers; tuning can overfit protocol to task.

### C0001-SRC-05

- **Title:** Improving Factuality and Reasoning in Language Models through Multiagent Debate
- **Authors or organization:** Yilun Du, Shuang Li, Antonio Torralba, Joshua B. Tenenbaum, Igor Mordatch
- **Date:** 2024-07
- **URL or DOI:** https://proceedings.mlr.press/v235/du24e.html ; https://doi.org/10.48550/arXiv.2305.14325
- **Source type:** Peer-reviewed ICML paper; positive multi-agent debate study
- **Design and conditions:** Same-model multi-agent debate, typically three agents and two rounds; arithmetic, GSM8K, chess, MMLU, and generated biography factuality tasks; single-pass, reflection, majority, and debate comparisons.
- **Claim supported or weakened:** Supports structured adversarial interaction and repeated correction as potentially useful.
- **Important limitations:** Debate adds calls, samples, rounds, and tokens; no matched-compute control; task-specific automatic evaluation; consensus can remain confidently wrong; long debate histories create attention and recency problems.

### C0001-SRC-06

- **Title:** Understanding Agent Scaling in LLM-Based Multi-Agent Systems via Diversity
- **Authors or organization:** Yingxuan Yang, Chengrui Qu, Muning Wen, Laixi Shi, Ying Wen, Weinan Zhang, Adam Wierman, Shangding Gu
- **Date:** 2026-02-03
- **URL or DOI:** https://arxiv.org/abs/2602.03794 ; https://doi.org/10.48550/arXiv.2602.03794
- **Source type:** Original-author preprint; correlation and diversity study
- **Design and conditions:** Vote and debate mechanisms; seven benchmarks; Qwen-2.5-7B, Llama-3.1-8B, and Mistral-7B; agent counts up to 16; diversity from models, prompts, personas, or tools; output cosine similarity and effective-channel metrics.
- **Claim supported or weakened:** Supports correlated-error and diminishing-return objections for homogeneous same-model agents; supports task-relevant heterogeneity as a mechanism.
- **Important limitations:** Preprint; 7B–8B models; static tasks; semantic similarity is not independence or factual correctness; theoretical assumptions include idealized conditional independence and uniform coverage.

### C0001-SRC-07

- **Title:** Why Do Multi-Agent LLM Systems Fail?
- **Authors or organization:** Mert Cemri et al.; UC Berkeley and collaborators
- **Date:** 2025-03-17 initial preprint; NeurIPS 2025 Datasets and Benchmarks version
- **URL or DOI:** https://arxiv.org/abs/2503.13657 ; https://doi.org/10.48550/arXiv.2503.13657
- **Source type:** Original failure dataset and taxonomy paper
- **Design and conditions:** 1,642 traces from seven multi-agent frameworks and four model families; coding, mathematics, and general-agent tasks; six expert annotators for taxonomy construction; three annotators per initial study; LLM annotator validated against human labels.
- **Claim supported or weakened:** Supports interface-loss, context-loss, repetition, inter-agent misalignment, and verification-failure mechanisms; shows selected workflow changes can help without changing the base model.
- **Important limitations:** Primarily observational and diagnostic; systems and tasks are heterogeneous; interventions are case studies rather than fixed-compute factorial ablations; much of the large dataset uses an LLM annotator.

### C0001-SRC-08

- **Title:** Self-Refine: Iterative Refinement with Self-Feedback
- **Authors or organization:** Aman Madaan et al.
- **Date:** 2023
- **URL or DOI:** https://proceedings.neurips.cc/paper_files/paper/2023/hash/91edff07232fb1b55a505a9e9f6c0ff3-Abstract-Conference.html ; https://doi.org/10.48550/arXiv.2303.17651
- **Source type:** Peer-reviewed NeurIPS paper; single-model staged refinement
- **Design and conditions:** Same LLM serves as generator, feedback provider, and refiner; GPT-3.5, ChatGPT, and GPT-4; seven tasks; human and automatic evaluation.
- **Claim supported or weakened:** Supports staged feedback and revision without multi-agent identity, weakening claims that nominal role separation is necessary.
- **Important limitations:** Adds feedback and revision calls; tasks include subjective generation; not compute matched; feedback and revision functions are bundled.

### C0001-SRC-09

- **Title:** Large Language Models Cannot Self-Correct Reasoning Yet
- **Authors or organization:** Jie Huang, Xinyun Chen, Swaroop Mishra, Huaixiu Steven Zheng, Adams Yu, Xinying Song, Denny Zhou
- **Date:** 2024
- **URL or DOI:** https://proceedings.iclr.cc/paper_files/paper/2024/hash/8b4add8b0aa8749d80a34ca5d941c355-Abstract-Conference.html ; https://doi.org/10.48550/arXiv.2310.01798
- **Source type:** Peer-reviewed ICLR paper; intrinsic self-correction evaluation
- **Design and conditions:** Tests reasoning self-correction without external feedback across contemporary LLMs and reasoning tasks.
- **Claim supported or weakened:** Weakens assumptions that a same-model critic or revision pass reliably identifies and corrects errors.
- **Important limitations:** Focuses on intrinsic self-correction rather than role-separated critics with independent evidence; model generations have advanced since the tested checkpoints; not a fixed-compute architecture comparison.

### C0001-SRC-10

- **Title:** LLMs cannot find reasoning errors, but can correct them given the error location
- **Authors or organization:** Gladys Tyen, Hassan Mansoor, Victor Carbune, Peter Chen, Tony Mak
- **Date:** 2024-08
- **URL or DOI:** https://aclanthology.org/2024.findings-acl.826/ ; https://doi.org/10.18653/v1/2024.findings-acl.826
- **Source type:** Peer-reviewed Findings of ACL paper; verifier-function decomposition
- **Design and conditions:** Separates mistake finding from correction across five reasoning tasks; supplies ground-truth error locations for correction; trains a small out-of-domain mistake-location classifier.
- **Claim supported or weakened:** Supports a specialized external verifier or deterministic locator as a unique function; weakens generic same-model critique.
- **Important limitations:** Ground-truth error locations are privileged information; the small classifier adds training and is not a role prompt; no role-loop or full compute comparison.

### C0001-SRC-11

- **Title:** Chain-of-Verification Reduces Hallucination in Large Language Models
- **Authors or organization:** Shehzaad Dhuliawala, Mojtaba Komeili, Jing Xu, Roberta Raileanu, Xian Li, Asli Celikyilmaz, Jason Weston
- **Date:** 2024-08
- **URL or DOI:** https://aclanthology.org/2024.findings-acl.212/ ; https://doi.org/10.18653/v1/2024.findings-acl.212
- **Source type:** Peer-reviewed Findings of ACL paper; staged factual verification
- **Design and conditions:** Draft, verification-question planning, independent question answering, and final verified response; Wikidata lists, closed-book MultiSpanQA, and long-form generation.
- **Claim supported or weakened:** Supports structured verification and reduced conditioning on the draft; weakens the necessity of multiple agent identities.
- **Important limitations:** Adds calls and tokens; uses one model and task-specific factuality measures; does not test persistent versus fresh contexts at equal total compute.

### C0001-SRC-12

- **Title:** Agent Workflow Memory
- **Authors or organization:** Zora Zhiruo Wang, Jiayuan Mao, Daniel Fried, Graham Neubig
- **Date:** 2025-07, ICML; first posted 2024-09-11
- **URL or DOI:** https://proceedings.mlr.press/v267/wang25bx.html ; https://doi.org/10.48550/arXiv.2409.07429
- **Source type:** Peer-reviewed ICML paper; external-memory intervention
- **Design and conditions:** Offline and online workflow induction; Mind2Web and WebArena; more than 1,000 tasks across more than 200 domains; reusable workflow records supplied as memory.
- **Claim supported or weakened:** Supports externalized structured memory as an active ingredient and potential alternative to role count.
- **Important limitations:** Memory conditions add information, induction, retrieval, and context; offline mode can use annotated examples; no matched role-separation comparison; outcomes are navigation success, not factuality or provenance.

### C0001-SRC-13

- **Title:** Self-Consistency Improves Chain of Thought Reasoning in Language Models
- **Authors or organization:** Xuezhi Wang, Jason Wei, Dale Schuurmans, Quoc V. Le, Ed H. Chi, Sharan Narang, Aakanksha Chowdhery, Denny Zhou
- **Date:** 2023, ICLR
- **URL or DOI:** https://research.google/pubs/self-consistency-improves-chain-of-thought-reasoning-in-language-models/ ; https://doi.org/10.48550/arXiv.2203.11171
- **Source type:** Peer-reviewed ICLR paper; sampling-and-voting baseline
- **Design and conditions:** Samples multiple diverse chain-of-thought paths and marginalizes answers; arithmetic and commonsense reasoning benchmarks including GSM8K, SVAMP, AQuA, StrategyQA, and ARC-Challenge.
- **Claim supported or weakened:** Supports added independent sampling as a strong alternative explanation for multi-agent gains.
- **Important limitations:** Explicitly uses more inference samples; no roles, critique, tools, external memory, or long-form factuality; majority voting fails when individual paths are systematically wrong.

### C0001-SRC-14

- **Title:** FActScore: Fine-grained Atomic Evaluation of Factual Precision in Long Form Text Generation
- **Authors or organization:** Sewon Min et al.
- **Date:** 2023-12
- **URL or DOI:** https://aclanthology.org/2023.emnlp-main.741/ ; https://doi.org/10.18653/v1/2023.emnlp-main.741
- **Source type:** Peer-reviewed EMNLP paper; factuality benchmark and metric
- **Design and conditions:** Decomposes biographies into atomic facts and checks support against a knowledge source; human evaluation of commercial LMs; automated retrieval-plus-LLM estimator; 6,500 generations from 13 models.
- **Claim supported or weakened:** Supports atomic claim segmentation and support adjudication for unsupported-claim measurement.
- **Important limitations:** Primarily biography factual precision; no factual coverage or omission denominator in the base score; automated retrieval and judging can err; no stage-level error lineage or workflow comparison.

### C0001-SRC-15

- **Title:** Enabling Large Language Models to Generate Text with Citations
- **Authors or organization:** Tianyu Gao, Howard Yen, Jiatong Yu, Danqi Chen
- **Date:** 2023-12
- **URL or DOI:** https://aclanthology.org/2023.emnlp-main.398/ ; https://doi.org/10.18653/v1/2023.emnlp-main.398
- **Source type:** Peer-reviewed EMNLP paper; ALCE citation benchmark
- **Design and conditions:** End-to-end retrieval and generation benchmark with automatic metrics for fluency, correctness, citation correctness, and citation completeness across multiple QA datasets.
- **Claim supported or weakened:** Supports separating citation presence, entailment or correctness, and completeness; shows traceable citations can still leave claims unsupported.
- **Important limitations:** Retrieval quality and generation quality are coupled; automatic metrics are proxies; citation completeness does not trace reasoning errors or test role separation.

### C0001-SRC-16

- **Title:** Long-form factuality in large language models
- **Authors or organization:** Jerry Wei et al.; Google DeepMind
- **Date:** 2024-03-27
- **URL or DOI:** https://arxiv.org/abs/2403.18802 ; https://doi.org/10.48550/arXiv.2403.18802 ; official code: https://github.com/google-deepmind/long-form-factuality
- **Source type:** Original-author preprint and benchmark repository; LongFact and SAFE
- **Design and conditions:** 2,280 long-form fact-seeking prompts across 38 topics; SAFE decomposes answers into facts, searches the web, and adjudicates support; approximately 16,000 facts compared with crowd annotations; 13 models from four families; F1@K combines supported-fact precision with a preferred-length recall proxy.
- **Claim supported or weakened:** Supports coverage-sensitive factuality evaluation and automated claim-level support checks.
- **Important limitations:** Prompts are model-generated; search and LLM adjudication can share biases; recall depends on a preferred-length hyperparameter rather than a complete fact set; no provenance-chain or multi-stage error-lineage evaluation.

## Handoff to Alternative Theorist and Integrator

The evidence does not justify choosing a final theory. The strongest defensible pattern is conditional:

- Under clean, short-answer reasoning and matched reasoning-token budgets, single-agent systems usually match or outperform role-separated systems.
- Multi-agent or partitioned workflows can help when tasks are naturally decomposable, require parallel breadth, contain corrupted or poorly utilized context, or include a reliable centralized verification signal.
- Positive debate, self-refinement, verification, and memory results usually add inference or information and therefore cannot isolate role separation.
- Same-base-model agents provide correlated and often increasingly redundant judgments; role prompts help only if they create useful, correct-path diversity.
- External memory, structured verification, and verifier quality have direct evidence as active ingredients and should be treated as alternative explanations rather than bundled into a generic multi-agent effect.

For the next roles, the cleanest candidate experiment remains a minimal factor contrast in which the same stage prompts, artifacts, evidence, and budget are executed either in one persistent context or across fresh invocations. Prompt tokens, completion tokens, tool calls, state creation, handoff generation, and final evaluation should all be charged. Outcomes should combine atomic support precision, citation correctness and completeness, coverage, task completion, and an adjudicated error-lineage record. Role ablations should be run twice: once with freed compute removed and once with it reallocated.