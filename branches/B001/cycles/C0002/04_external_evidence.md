# External Evidence Researcher — C0002

## Research Scope

This report addresses the corrected C0002 frontier: observable effects of prior-trace access, state serialization, retention, compression, and context use. It does not treat a nominal persistent-versus-fresh label as a causal treatment unless a study identifies a functionally relevant residual difference after visible inputs and prior-message access are matched.

The search prioritized studies that could discriminate among the three conditions proposed by the Critic and Internal Evidence Researcher:

1. persistent execution with full prior trace;
2. persistent execution with standardized-package-only access; and
3. fresh execution with the same standardized-package-only access.

The most important direct target was a noncollapsed comparison between conditions 2 and 3. No located study held the serialized package, prior-trace inaccessibility, model, prompts, stage instructions, tools, evidence, candidate and selector opportunities, and full inference cost approximately constant while changing only the conversation or invocation container. This is a search-bounded evidence-gap finding, not proof that no such study exists.

The strongest near-direct source, `C0002-SRC-01`, formalizes single-agent full-context execution versus isolated local contexts connected by bounded relays. Its central result is that unlimited relay transmission can reproduce the full upstream context, so the substantive difference arises from information compression and loss rather than nominal agent identity alone. Its experiments vary relay sufficiency and show benefits when compressed relays retain needed information and reversals when they do not. This directly supports the Critic’s decomposition, but it still does not isolate a residual package-only persistent-versus-fresh effect.

Fourteen original research sources were used: eleven peer-reviewed papers or benchmark papers and three original-author preprints. All sources are primary research. Several are not independent because they reuse LongMemEval, LoCoMo, or aggregated summarization datasets; those dependencies are identified below.

## Search Questions

1. Does any primary study compare full prior-trace access with standardized-package-only access while approximately matching model, task, prompts, visible evidence, tools, sampling, selector, evaluator, and compute?
2. Does any study identify a noncollapsed residual difference between package-only persistent and package-only fresh execution?
3. What controlled evidence shows that earlier conversational trace can contaminate later performance?
4. What controlled evidence shows that reset, summarization, or compressed handoffs can lose valid dependencies or qualifications?
5. What methods independently manipulate state representation, write-time retention, retrieval, or compression?
6. Which benchmarks provide a predeclared information inventory, evidence annotation, temporal or causal dependency graph, or known coverage target?
7. Which methods distinguish preservation, omission, contradiction, factual mutation, correction, and coverage?
8. Which studies report evaluator reliability or demonstrate that factuality metrics vary by error type and generator?
9. Which studies match compute in a way relevant to B001, and which merely add calls, tools, context, or inference?
10. Is there direct evidence from open-ended, multi-source research synthesis rather than conversational QA, static QA, summarization, or agentic task benchmarks?

## Search Method and Source Hierarchy

Searches were conducted on July 24, 2026 through arXiv, ACL Anthology, publisher and benchmark pages, and general scholarly web search used to locate original papers. Search terms combined variants of: persistent context, context reset, fresh conversation, prior conversation history, task interference, context compression, conversation condensation, memory write loss, state serialization, handoff compression, information bottleneck, summary fidelity, claim preservation, factual mutation, error correction, long-context coverage, and fixed-budget memory.

The hierarchy was:

1. peer-reviewed original papers and original-author preprints;
2. original benchmark and dataset papers;
3. official paper repositories and canonical DOI records;
4. secondary pages only for discovery, not factual support.

Strict direct-evidence inclusion required extraction of model, task, prompts or stage instructions, prior-trace access, visible inputs, state artifact, evidence and tools, sampling and selector opportunities, evaluator, context length, generation and final-answer cost, coverage measures, and manipulation checks. Sources failing those controls were retained only as indirect state or measurement evidence.

### Intervention matrix

| Source | Evidence class | Model and task conditions | Trace and visible-input manipulation | State or handoff manipulation | Sampling, selector, tools | Evaluation and coverage | Compute treatment and major confounds |
|---|---|---|---|---|---|---|---|
| `C0002-SRC-01` | Near-direct access/relay evidence | Three model scales; 18 comparisons across ALFWorld, WebShop, WorkBench, WideSearch, and TravelPlanner | Full accumulated context in single-agent/context-flow conditions versus isolated local contexts in multi-agent condition | Bounded relay messages; relay sufficiency is central | Agentic tools vary by benchmark; decomposition held similar in the main comparison | Benchmark task success; no branch-style claim lineage | Reports controlled experiments and matched maximum step budgets, but not a complete prompt/context/token/tool/final-answer ledger; isolation and compression remain bundled |
| `C0002-SRC-02` | Indirect prior-trace contamination evidence | Open- and closed-weight LLMs; six generation tasks; more than 200,000 simulated conversations | Fully specified single turn versus incrementally specified multi-turn interaction | No canonical serialized package | Multiple conversational turns; no matched selector | Task performance and unreliability decomposition; no factual-coverage control | Information timing, calls, tokens, and interaction format differ; not a reset with identical visible inputs |
| `C0002-SRC-03` | Indirect prior-history interference evidence | Popular LLMs; five datasets and fifteen task switches | Target task with versus without preceding mismatched-task conversational history | Raw conversational history, not structured state | No special selector; ordinary prompting | Dataset task metrics | Added history changes information, context length, salience, and processing cost |
| `C0002-SRC-04` | Indirect compression/state evidence | Thirteen LLMs across multi-turn benchmarks | Full accumulated history baseline versus condensed history pipeline | Few-shot condenser plus lightweight decider; selective retention; up to 72% token reduction in ten-turn dialogues | Adds a condenser agent and decision step | Accuracy, distractor robustness, token reduction; no stage-level factual lineage | Added inference and prompt design are not fully charged against baseline; not a freshness contrast |
| `C0002-SRC-05` | Strong indirect retention diagnostic | Six memory baselines, 500 LongMemEval questions, three fixed readers | Same reader evaluated under truncated full context, oracle evidence, complete stored memory, and retrieved memory | Separates write-side retention from retrieval; Expected Predictive Compression preserves predicted supporting evidence under a token budget | EPC adds a write-time LLM call; retrieval held unchanged in the key diagnostic | QA score and write/retrieval gaps; gold evidence available through LongMemEval | Fixed memory-token budget and fixed reader, with some cost-matched analysis; not full end-to-end inference-compute equality |
| `C0002-SRC-06` | Benchmark and state-stage method | 500 curated questions in scalable long-term chat histories | Full histories and memory systems evaluated on extraction, reasoning, temporal update, and abstention | Decomposes indexing, retrieval, and reading; supplies evidence annotations | Retrieval methods and query expansion may add work | QA accuracy and evidence retrieval; approximately 30% sustained-interaction drop reported | Benchmark, not causal boundary study; systems differ in retrieval and cost |
| `C0002-SRC-07` | Benchmark and dependency-reference method | Conversations averaging 600 turns and 16K tokens over up to 32 sessions | Long context and RAG systems on long-term dialogues | Persona and temporal event graphs provide a predeclared grounding structure | RAG and long-context approaches differ | QA, event summarization, dialogue generation; human-verified grounding | Synthetic machine-human pipeline; no matched reset or full cost control |
| `C0002-SRC-08` | Direct context-use diagnostic, not boundary evidence | Multiple LMs on multi-document QA and key-value retrieval | Same relevant information placed at different context positions | No serialized state; manipulates placement in long context | No agent sampling or selector | Exact task performance by position | Input content is largely held constant, but context length/position rather than reset is manipulated; supports salience explanation |
| `C0002-SRC-09` | Coverage and citation measurement method | Ten LLMs and fifty RAG systems; conversation and news domains | Long-context and retrieval systems receive synthetic haystacks with known relevant insights | Known insight inventory and source-document map | RAG variants and oracle relevance conditions | Separate Coverage and Citation scores plus Joint Score | System compute varies; method is strong for coverage control, not invocation effects |
| `C0002-SRC-10` | Error taxonomy and evaluator-reliability method | Nine summarization systems over CNN/DailyMail and XSum; 2,250 annotated summaries | Source documents compared with generated summaries | No sequential handoff; factual error categories encode relation changes | No agent sampling | Sentence-level human factuality labels; reported expert/crowd agreement supports category reliability | Older summarization setting; does not score omissions or multi-stage lineage |
| `C0002-SRC-11` | Content-retention measurement method | Reference-summary datasets and QA components | Candidate summary compared with reference content | Questions derived from reference units estimate content overlap | QA model and question-generation pipeline | Content-quality correlation and component analysis | Reference-dependent; QA errors can masquerade as omissions; not factual support or lineage by itself |
| `C0002-SRC-12` | Correction and mutation measurement method | Dialogue summarization factual-error correction dataset and systems | Erroneous summary versus reference correction | Fine-grained edits and error categories | Correction systems differ | FERRANTI scores correction by reference-aligned error type | Correction benchmark, not sequential multi-role lineage; depends on reference corrections |
| `C0002-SRC-13` | Evaluator-validity evidence | Aggregates annotations from nine factuality datasets, stratified by generator and error type | No reset manipulation | No state manipulation | Compares factuality metrics, including LLM-based metrics | Shows metric performance varies by generator and error type; no universal winner | Reuses underlying datasets, including work related to other ledger sources; not independent effect evidence |
| `C0002-SRC-14` | Indirect structured-state evidence | LoCoMo and LongMemEval long-term conversational QA | Full interaction history stored externally and selectively retrieved | Temporal property graph, append-only record, multi-tool retrieval, compact query-time summary | Adds graph construction and multi-tool retrieval agent | Reports 88.88% LoCoMo and 86.2% LongMemEval accuracy | Structured memory, retrieval tools, conflict resolution, and extra inference are bundled; reuses `C0002-SRC-06` and `C0002-SRC-07` benchmarks |

## Evidence Supporting the Main Direction

### `C0002-EXT-01` — The operative contrast is information access and relay fidelity, not nominal agent identity

`C0002-SRC-01` is the closest located study to the corrected C0002 estimand. It models a single-agent system as accumulating a full reasoning trace in one shared context and a multi-agent system as using isolated local contexts connected by bounded relay messages. The theoretical equivalence result states that with unlimited relay bandwidth, the multi-agent system can transmit the full upstream context and simulate the single-agent system. The empirical comparison similarly holds task decomposition and broad workflow structure closer than generic multi-agent papers and varies whether relays are near-sufficient or information-losing.

What this supports: the Critic’s correction that any measurable effect must be assigned to observable trace access, relay compression, and retained task information. It weakens any claim that a fresh container has a causal effect merely because it is fresh.

What it does not support: a package-only persistent-versus-package-only fresh residual. Local-context isolation and relay compression are jointly present, and the paper does not show that two byte-identical, trace-inaccessible packages behave differently solely because one call is in a continuing conversation container.

### `C0002-EXT-02` — Prior conversational trace can create measurable interference and error persistence

`C0002-SRC-02` reports an average 39% performance drop across six generation tasks when information is distributed over simulated multi-turn conversations rather than supplied as a fully specified single-turn instruction. Its analysis of more than 200,000 conversations attributes most of the loss to increased unreliability: models make early assumptions, attempt solutions prematurely, and over-rely on earlier wrong turns.

`C0002-SRC-03` supplies a narrower controlled mechanism. Across five datasets and fifteen task switches, adding mismatched-task conversational history often significantly degrades the target task. This supports treating authorized prior-trace access as a real treatment and supports contamination and task-interference mechanisms.

`C0002-SRC-08` adds a context-salience mechanism: the same relevant information can be used much less effectively when it is located in the middle of a long input. Therefore full-trace access is not simply “more information”; it changes position, salience, and retrieval difficulty. This is important for B001 because a persistent trace may harm later stages even without containing false claims.

These studies do not identify a fresh-boundary effect. Their conditions change information timing, history content, or position. They support a prior-trace-access factor and manipulation checks for context length and placement.

### `C0002-EXT-03` — State write quality and selective retention can dominate downstream retrieval

`C0002-SRC-05` provides the cleanest located decomposition of state failure. With a fixed reader, it compares truncated full context, oracle evidence, complete stored memory, and retrieved memory on all 500 LongMemEval questions. Four of six tested baselines are reported as write-dominant under the authors’ default diagnostic margin: evidence lost during memory construction is a larger bottleneck than retrieval from the resulting memory. Expected Predictive Compression improves complete-stored-memory score to 0.49 versus 0.44 for the strongest summary baseline while using the same token budget for stored state.

This supports separating schema presence from observable retention. A state object can exist and still have discarded the evidence later stages need. It also supports measuring write loss independently from retrieval loss rather than calling the whole package “complete.”

`C0002-SRC-06` independently structures long-term memory as indexing, retrieval, and reading and provides 500 curated questions spanning extraction, multi-session reasoning, temporal reasoning, knowledge updates, and abstention. Its evidence annotations and staged decomposition are useful for B001’s manipulation checks.

### `C0002-EXT-04` — Structured or selectively condensed state can outperform raw accumulated context in some regimes

`C0002-SRC-04` reports that a one-off condenser and lightweight decider can reduce history tokens by up to 72% in ten-turn dialogues while improving or preserving accuracy across thirteen LLMs and diverse multi-turn benchmarks. `C0002-SRC-14` reports strong results from an append-only temporal property graph plus multi-tool retrieval and compact query-time summaries on LoCoMo and LongMemEval. These results support the possibility that structured state and selective access reduce irrelevant context while preserving useful information.

The support is for state representation, retention policy, and retrieval design. Both methods add active components and inference. Neither establishes that a fresh invocation is beneficial once the state and full cost are matched.

### `C0002-EXT-05` — Predeclared information inventories and dependency references are feasible

`C0002-SRC-07` grounds very long conversations in personas and temporal event graphs verified and edited by humans, creating known temporal and causal dependencies before model scoring. `C0002-SRC-09` synthesizes document haystacks with known relevant insights and known source-document links, then separately scores coverage and citation. `C0002-SRC-11` turns reference content into questions to estimate how much reference information a candidate summary retains.

These methods support the Critic’s requirement to predeclare an information or dependency reference rather than infer “essential” content from which condition succeeds. For B001, injected claim relations, qualifications, objections, and unresolved questions could be scored for retention before final outcomes are interpreted.

### `C0002-EXT-06` — Fine-grained factual mutation and correction categories can be coded, but no located method completes B001’s lineage requirement

`C0002-SRC-10` supplies a grounded factual-error typology covering errors involving predicates, entities, circumstances, coreference, discourse links, unsupported external content, and grammaticality. `C0002-SRC-12` evaluates factual-error correction against reference edits with category-sensitive scoring. These methods can distinguish some contradiction, relation mutation, and correction events more precisely than semantic similarity.

They do not follow the same claim through multiple generation, criticism, evidence, and integration stages. The branch still needs explicit cross-stage identity and status links for introduced, preserved, corrected, mutated, or amplified claims.

## Evidence Weakening the Main Direction

### 1. Relay compression can reverse apparent multi-agent or reset benefits

The same source that most strongly supports the corrected information-access framing also supplies the strongest weakening evidence. `C0002-SRC-01` reports that multi-agent gains shrink or reverse when bounded relays lose task-relevant information, especially for stronger models that can extract useful information from a redundant full context. Fresh or isolated execution is therefore not monotonically protective. It can remove contamination, but it can also remove necessary dependencies.

This directly weakens `C0002-EXP-02` as a general direction and supports `C0002-EXP-03`: contamination reduction and interface loss are two sides of the same compression decision.

### 2. Long-range temporal and causal dependencies remain difficult after summarization or retrieval

`C0002-SRC-07` finds that long-context and RAG approaches improve some long-term conversational tasks but remain substantially below human performance, particularly for temporal and causal dynamics. `C0002-SRC-06` reports an approximately 30% accuracy drop across sustained interactions. These results show that a serialized package or retrieval layer does not automatically preserve the relations needed downstream.

`C0002-SRC-05` is more diagnostic: many systems lose evidence at write time before retrieval can help. This weakens any inference from field compliance or concise summaries to semantic completeness.

### 3. Full-context access sometimes preserves useful information that compressed state loses

`C0002-SRC-01` predicts and observes regimes where stronger models benefit from redundant full context because the relay discards useful information. `C0002-SRC-08` shows that long context is used imperfectly, not that it is uniformly harmful. The correct comparison must therefore measure both contamination and valid dependency preservation.

A full-trace persistent condition may outperform a package-only condition for a legitimate reason: it has retained qualifications, support, and relations. That effect should be labeled prior-trace access, not dismissed as unfair noise.

### 4. Apparent factual improvement can be an omission or coverage artifact

`C0002-SRC-09` demonstrates that coverage and citation are distinct. Even systems given oracle relevance remain more than ten points below the estimated human Joint Score, and long-context models without retrieval score below 20% in the reported setup. A system can cite correctly while missing required insights, or mention insights without adequate source attribution.

`C0002-SRC-11` provides a reference-content measure, while `C0002-SRC-13` shows that factuality metric performance varies substantially across generators and error types. Thus a lower unsupported-claim count in a fresh or compressed condition cannot be accepted without claim count, content coverage, task completion, and evaluator validation.

### 5. No exact residual-boundary study was located

No source identifies a functionally meaningful difference that remains after both persistent and fresh conditions receive the same serialized package, lack access to earlier trace, use matched instructions, roles, permissions, tools, model settings, samples and selectors, and receive matched compute. The search instead found studies of history access, multi-turn information timing, context position, relay compression, memory writing, retrieval, and structured state.

This is the strongest weakening finding for any claim of an independent fresh-container effect. A null package-only persistent-versus-package-only fresh result would remain ambiguous unless the residual manipulation is specified and verified.

## Evidence About Alternative Explanations

### Prior-trace interference

`C0002-SRC-02` and `C0002-SRC-03` support the alternative that earlier turns cause anchoring, premature commitment, and task interference. A fresh stage may help because it removes particular history, not because a new invocation is intrinsically better.

### Context position and salience

`C0002-SRC-08` shows that position within the same long context changes retrieval success. Differences between persistent and packaged conditions may reflect where evidence appears and how much irrelevant content surrounds it.

### Write-time retention versus retrieval-time failure

`C0002-SRC-05` separates evidence discarded during compression from evidence preserved but not retrieved. This alternative explanation is especially important because a failed final answer can arise from either stage, and the remedies differ.

### Structured-state dominance

`C0002-SRC-04` and `C0002-SRC-14` support the possibility that selective condensation, temporal structure, append-only history, and retrieval tools explain gains that could otherwise be attributed to context reset or role separation. Their interventions are active and bundled, so they cannot rank state versus freshness directly.

### Model-capability interaction

`C0002-SRC-01` reports that stronger models benefit less from context reduction and are harmed more when relays lose information. An average boundary or compression effect may therefore mask model-scale interactions.

### Task-structure interaction

Sequential, temporal, and causal tasks in `C0002-SRC-06` and `C0002-SRC-07` place greater demands on dependency retention than short independent subtasks. Results from static QA or conversational instruction following may not transfer to open-ended research synthesis.

### Metric and evaluator choice

`C0002-SRC-10`, `C0002-SRC-12`, and `C0002-SRC-13` show that error taxonomies and metric behavior depend on generator and error type. A claimed reduction in factual mutation can be produced or erased by evaluator choice. B001 should use explicit coding rules, multiple evaluators, adjudication, and reported agreement rather than a single LLM judge.

### Added tools and inference

The condenser in `C0002-SRC-04`, the predictive write-time call in `C0002-SRC-05`, and the graph construction and multi-tool retrieval in `C0002-SRC-14` add inference, state construction, and selection. Their gains may be caused by added compute or privileged structure rather than information exclusion alone.

## Fixed-Compute Versus Added-Compute Evidence

### `C0002-EXT-07` — No located source satisfies B001’s full compute ledger

No source reports and matches all of the following across the relevant conditions: system and role-prompt processing, accumulated-context processing, stage-package generation, package validation, completions, tool calls, retrieval, candidate generation, selection, orchestration, and final-answer generation, together with an explicit rule for saved budget.

The closest cases are partial:

- `C0002-SRC-05` fixes the stored-memory token budget and reader in its diagnostic and reports cost-aware comparisons for its extra write-time step. This is strong evidence about retention under a fixed state budget, but not equality of total end-to-end inference compute.
- `C0002-SRC-01` uses controlled benchmark comparisons and matched maximum step budgets. Step equality does not ensure equal prompt tokens, context processing, relay generation, local completions, tool costs, or final-answer costs.
- `C0002-SRC-04` reports large reductions in consumed history tokens and operational cost, but the condenser and decider add inference. Token savings after condensation do not establish equal total compute.
- `C0002-SRC-14` adds graph construction, append-only state maintenance, multi-tool retrieval, conflict resolution, and summary generation. It is an added-system comparison.
- `C0002-SRC-02` and `C0002-SRC-03` vary the number and content of conversation turns or history tokens, so they do not match inference.
- Measurement and benchmark sources do not attempt compute matching.

For B001, a primary matching rule remains mandatory. At minimum, the experiment should separately record input tokens by stage, output tokens by stage, state-construction tokens, tool and retrieval calls, candidate and selector calls, latency, and monetary cost. It must predeclare whether saved budget is unused, reallocated within the same stage, or reallocated across stages. Otherwise a concise package can gain extra reasoning budget and a full trace can consume extra context-processing budget.

## Conflicting or Inconclusive Findings

1. **Context can contaminate or preserve.** `C0002-SRC-02` and `C0002-SRC-03` show history-induced unreliability and task interference, while `C0002-SRC-01`, `C0002-SRC-06`, and `C0002-SRC-07` show that compressed or retrieved state can lose needed information. The conflict is consistent with a task- and retention-dependent tradeoff rather than a universal reset benefit.
2. **Compression can improve efficiency or create interface loss.** `C0002-SRC-04` reports broad gains or preserved accuracy from selective condensation, while `C0002-SRC-01` reports reversals when relays are insufficient and `C0002-SRC-05` finds write-side loss in many memory systems. Compression quality, not compression presence, is the likely moderator.
3. **Structured memory results are positive but bundled.** `C0002-SRC-14` reports strong benchmark scores, but its property graph, append-only state, retrieval agent, tools, and summary are changed together. It cannot establish which component matters or whether the result holds at equal compute.
4. **Long-context failure is not equivalent to a fresh-context advantage.** `C0002-SRC-08` shows position-sensitive use of long context. Removing history could help by shortening or repositioning evidence, but could also remove valid evidence. No source isolates those pathways.
5. **Factuality measurement is not stable across systems.** `C0002-SRC-13` finds no single metric superior across all generators and error types. FRANK and FERRANTI offer useful taxonomies, but their validity does not automatically transfer to multi-stage research claims.
6. **Benchmark improvements are not independent replications.** `C0002-SRC-05` and `C0002-SRC-14` use LongMemEval; `C0002-SRC-14` also uses LoCoMo. Their positive structured-memory results should not be counted as three independent datasets or mechanisms.

## Source Reliability and Independence

Eleven ledger sources are peer-reviewed conference or journal papers or accepted benchmark papers. `C0002-SRC-01`, `C0002-SRC-02`, and `C0002-SRC-05` are original-author preprints in the versions used here. The newest and most directly relevant source, `C0002-SRC-01`, was submitted July 17, 2026 and has not yet received peer-review weight in this report.

Independence constraints:

- `C0002-SRC-05` evaluates LongMemEval from `C0002-SRC-06`.
- `C0002-SRC-14` evaluates both LongMemEval and LoCoMo from `C0002-SRC-06` and `C0002-SRC-07`.
- `C0002-SRC-13` aggregates nine existing factuality datasets and therefore overlaps conceptually and potentially empirically with individual factuality benchmarks such as `C0002-SRC-10`.
- `C0002-SRC-04` responds to the same broad multi-turn degradation problem as `C0002-SRC-02`; benchmark overlap should be checked before treating their results as independent.
- `C0002-SRC-09`, `C0002-SRC-10`, `C0002-SRC-11`, and `C0002-SRC-12` primarily contribute measurement methods, not independent evidence about context reset.

Reliability is strongest for observable benchmark definitions, dataset sizes, intervention descriptions, and reported within-study comparisons. Reliability is weaker for cross-study causal synthesis because models, tasks, prompts, costs, context lengths, and evaluators differ. Marketing-style claims such as “state of the art” were not treated as proof of mechanism.

## Evidence Gaps

- No noncollapsed package-only persistent-versus-package-only fresh study was located.
- No study holds all visible inputs, role and stage instructions, permissions, tools, evidence, candidate opportunities, selector rules, and full compute constant while varying only the invocation or conversation container.
- No open-ended multi-source research-synthesis study directly tests the corrected three-condition access decomposition.
- No located study uses B001’s desired cross-stage lineage categories—introduced, preserved, corrected, mutated, and amplified—on the same claim identities across a complete research workflow.
- No accepted common measure combines schema compliance, predeclared information retention, task-relative dependency coverage, package size, transformation type, factual support, citation completeness, task completion, and usefulness.
- Inter-rater reliability is reported for some factuality taxonomies, but no located study validates reliability for the complete lineage codebook required here.
- No source fully matches end-to-end inference compute or declares a generally reusable saved-budget rule.
- Structured state versus unstructured full trace is usually confounded by retrieval, summarization, graph construction, tools, or extra inference.
- Evidence on context contamination comes mainly from multi-turn instruction following and task-switch settings, not from staged evidence synthesis.
- Evidence on dependency loss comes mainly from memory QA, long-context retrieval, summarization, or agentic benchmarks; transfer to research reports remains uncertain.
- No source establishes a scalar state-completeness threshold. The evidence instead supports separate measures of structural compliance, retained reference items, dependency coverage, and package cost.

## Source Ledger

### C0002-SRC-01

- **Source ID:** `C0002-SRC-01`
- **Title:** *When Do Multi-Agent Systems Help? An Information Bottleneck Perspective*
- **Authors or organization:** Wendi Yu, Lianhao Zhou, Xiangjue Dong, Sai Sudarshan Barath, Declan Staunton, Byung-Jun Yoon, Xiaoning Qian, James Caverlee, Shuiwang Ji
- **Date:** July 17, 2026
- **URL or DOI:** https://arxiv.org/abs/2607.16133 ; DOI 10.48550/arXiv.2607.16133
- **Source type:** Original-author preprint; theoretical analysis plus 18 controlled benchmark comparisons
- **Claim supported or weakened:** Supports treating bounded relay compression and prior-context access as the operative variables; supports near-equivalence when full upstream context can be relayed; weakens a general contamination-reduction claim because gains reverse when relays lose relevant information.
- **Important limitations:** Not peer reviewed in the cited version; isolated local context and relay compression remain bundled; maximum-step controls are not a full compute ledger; no package-only persistent-versus-fresh residual test; tasks are agentic benchmarks rather than open-ended research synthesis.

### C0002-SRC-02

- **Source ID:** `C0002-SRC-02`
- **Title:** *LLMs Get Lost In Multi-Turn Conversation*
- **Authors or organization:** Philippe Laban, Hiroaki Hayashi, Yingbo Zhou, Jennifer Neville
- **Date:** May 9, 2025
- **URL or DOI:** https://arxiv.org/abs/2505.06120 ; DOI 10.48550/arXiv.2505.06120
- **Source type:** Original-author preprint; large-scale simulation study
- **Claim supported or weakened:** Supports prior-trace contamination and error persistence: more than 200,000 simulated conversations show an average 39% multi-turn performance drop across six generation tasks, largely associated with unreliability and over-reliance on early wrong turns.
- **Important limitations:** Fully specified single-turn and incrementally specified multi-turn conditions differ in information timing, calls, tokens, and interaction; simulated users; no identical serialized package or fixed full compute; not claim-level factual synthesis.

### C0002-SRC-03

- **Source ID:** `C0002-SRC-03`
- **Title:** *LLM Task Interference: An Initial Study on the Impact of Task-Switch in Conversational History*
- **Authors or organization:** Akash Gupta, Ivaxi Sheth, Vyas Raina, Mark Gales, Mario Fritz
- **Date:** November 2024
- **URL or DOI:** https://aclanthology.org/2024.emnlp-main.811/ ; DOI 10.18653/v1/2024.emnlp-main.811
- **Source type:** Peer-reviewed EMNLP paper
- **Claim supported or weakened:** Supports an observable prior-history interference effect; many of fifteen task switches across five datasets significantly degrade target performance.
- **Important limitations:** Adding task history changes input content, length, position, and processing cost; no standardized state package; not a reset or fresh-call comparison and not open-ended research synthesis.

### C0002-SRC-04

- **Source ID:** `C0002-SRC-04`
- **Title:** *MT-OSC: Path for LLMs that Get Lost in Multi-Turn Conversation*
- **Authors or organization:** Jyotika Singh, Fang Tu, Miguel Ballesteros, Weiyi Sun, Sandip Ghoshal, Michelle Yuan, Yassine Benajiba, Sujith Ravi, Dan Roth
- **Date:** July 2026
- **URL or DOI:** https://aclanthology.org/2026.findings-acl.1354/ ; DOI 10.18653/v1/2026.findings-acl.1354
- **Source type:** Peer-reviewed Findings of ACL paper
- **Claim supported or weakened:** Supports selective condensation as an active state intervention; reports up to 72% history-token reduction in ten-turn dialogues and improved or preserved accuracy across thirteen LLMs and multiple benchmarks.
- **Important limitations:** Adds a condenser agent, few-shot prompt, and decider; does not equalize total inference compute; no explicit claim-status or dependency-retention score; no package-only persistent-versus-fresh comparison.

### C0002-SRC-05

- **Source ID:** `C0002-SRC-05`
- **Title:** *WhenLoss: Diagnosing Write and Retrieval Bottlenecks in Long-Context Memory Systems*
- **Authors or organization:** Jiangnan Yu, Kisson Songqi Lin, Jilong Wu
- **Date:** May 23, 2026
- **URL or DOI:** https://arxiv.org/abs/2605.24579 ; DOI 10.48550/arXiv.2605.24579
- **Source type:** Original-author preprint; controlled memory-system diagnostic
- **Claim supported or weakened:** Supports separating write-time retention from retrieval; under a fixed stored-state budget and fixed readers, four of six baselines are write-dominant, and Expected Predictive Compression raises complete-stored-memory score from 0.44 to 0.49 in the reported LongMemEval setup.
- **Important limitations:** Preprint; uses LongMemEval rather than independent task data; predictive compression adds an LLM call; token-budget equality is not full inference equality; oracle evidence is privileged; no freshness contrast.

### C0002-SRC-06

- **Source ID:** `C0002-SRC-06`
- **Title:** *LongMemEval: Benchmarking Chat Assistants on Long-Term Interactive Memory*
- **Authors or organization:** Di Wu, Hongwei Wang, Wenhao Yu, Yuwei Zhang, Kai-Wei Chang, Dong Yu
- **Date:** 2025; original preprint October 14, 2024, revised March 4, 2025
- **URL or DOI:** https://arxiv.org/abs/2410.10813 ; DOI 10.48550/arXiv.2410.10813
- **Source type:** Original benchmark paper, ICLR 2025
- **Claim supported or weakened:** Supports decomposition into indexing, retrieval, and reading and supplies 500 curated questions with evidence-grounded memory demands; reports an approximately 30% sustained-interaction accuracy drop for existing systems.
- **Important limitations:** Benchmark and system analysis, not an invocation-boundary experiment; memory methods vary retrieval and cost; question-answering focus; reused by `C0002-SRC-05` and `C0002-SRC-14`.

### C0002-SRC-07

- **Source ID:** `C0002-SRC-07`
- **Title:** *Evaluating Very Long-Term Conversational Memory of LLM Agents*
- **Authors or organization:** Adyasha Maharana, Dong-Ho Lee, Sergey Tulyakov, Mohit Bansal, Francesco Barbieri, Yuwei Fang
- **Date:** August 2024
- **URL or DOI:** https://aclanthology.org/2024.acl-long.747/ ; DOI 10.18653/v1/2024.acl-long.747
- **Source type:** Peer-reviewed ACL benchmark and dataset paper
- **Claim supported or weakened:** Supports predeclared temporal and causal dependency references through persona and event graphs; shows persistent difficulty with long-range dependencies in conversations averaging 600 turns and 16K tokens over up to 32 sessions.
- **Important limitations:** Synthetic machine-human conversation pipeline; benchmark systems differ in retrieval and compute; no reset/access isolation; reused by `C0002-SRC-14`.

### C0002-SRC-08

- **Source ID:** `C0002-SRC-08`
- **Title:** *Lost in the Middle: How Language Models Use Long Contexts*
- **Authors or organization:** Nelson F. Liu, Kevin Lin, John Hewitt, Ashwin Paranjape, Michele Bevilacqua, Fabio Petroni, Percy Liang
- **Date:** 2024
- **URL or DOI:** https://aclanthology.org/2024.tacl-1.9/ ; DOI 10.1162/tacl_a_00638
- **Source type:** Peer-reviewed TACL paper
- **Claim supported or weakened:** Supports context-position and salience as alternative explanations; performance on multi-document QA and key-value retrieval is often highest with relevant information at the beginning or end and lower when it appears in the middle.
- **Important limitations:** Manipulates position, not persistence or reset; does not test serialized state, handoffs, error lineage, or full compute equality.

### C0002-SRC-09

- **Source ID:** `C0002-SRC-09`
- **Title:** *Summary of a Haystack: A Challenge to Long-Context LLMs and RAG Systems*
- **Authors or organization:** Philippe Laban, Alexander Fabbri, Caiming Xiong, Chien-Sheng Wu
- **Date:** November 2024
- **URL or DOI:** https://aclanthology.org/2024.emnlp-main.552/ ; DOI 10.18653/v1/2024.emnlp-main.552
- **Source type:** Peer-reviewed EMNLP benchmark paper
- **Claim supported or weakened:** Supports a predeclared relevant-insight inventory and separate Coverage and Citation scoring; shows that even oracle-relevance systems remain more than ten points below the estimated human Joint Score in the reported setup.
- **Important limitations:** Synthetic haystacks; final-output measurement rather than cross-stage lineage; system compute varies; automatic matching may have evaluator error; not a boundary study.

### C0002-SRC-10

- **Source ID:** `C0002-SRC-10`
- **Title:** *Understanding Factuality in Abstractive Summarization with FRANK: A Benchmark for Factuality Metrics*
- **Authors or organization:** Artidoro Pagnoni, Vidhisha Balachandran, Yulia Tsvetkov
- **Date:** June 2021
- **URL or DOI:** https://aclanthology.org/2021.naacl-main.383/ ; DOI 10.18653/v1/2021.naacl-main.383
- **Source type:** Peer-reviewed NAACL benchmark and annotation study
- **Claim supported or weakened:** Supports grounded factual-error categories and reliability checks for entity, predicate, circumstance, coreference, discourse-link, unsupported-content, and grammatical errors.
- **Important limitations:** Single-stage summarization; older datasets and systems; does not score information omission or follow claim identity across stages; taxonomy transfer to open research requires validation.

### C0002-SRC-11

- **Source ID:** `C0002-SRC-11`
- **Title:** *Towards Question-Answering as an Automatic Metric for Evaluating the Content Quality of a Summary*
- **Authors or organization:** Daniel Deutsch, Tania Bedrax-Weiss, Dan Roth
- **Date:** 2021
- **URL or DOI:** https://aclanthology.org/2021.tacl-1.47/ ; DOI 10.1162/tacl_a_00397
- **Source type:** Peer-reviewed TACL measurement paper
- **Claim supported or weakened:** Supports reference-relative content retention measurement through questions derived from source or reference information; useful for detecting omission that unsupported-claim precision alone misses.
- **Important limitations:** Question generation and answering introduce their own errors; reference-dependent; does not establish source support, citation completeness, or multi-stage mutation by itself.

### C0002-SRC-12

- **Source ID:** `C0002-SRC-12`
- **Title:** *Reference Matters: Benchmarking Factual Error Correction for Dialogue Summarization with Fine-grained Evaluation Framework*
- **Authors or organization:** Mingqi Gao, Xiaojun Wan, Jia Su, Zhefeng Wang, Baoxing Huai
- **Date:** July 2023
- **URL or DOI:** https://aclanthology.org/2023.acl-long.779/ ; DOI 10.18653/v1/2023.acl-long.779
- **Source type:** Peer-reviewed ACL benchmark and evaluation paper
- **Claim supported or weakened:** Supports fine-grained, reference-aligned evaluation of factual correction and error-type changes rather than relying only on global similarity.
- **Important limitations:** Dialogue-summary correction rather than multi-stage research; requires reference corrections; does not independently score omissions, amplification, or claim lineage across more than an input-output correction pair.

### C0002-SRC-13

- **Source ID:** `C0002-SRC-13`
- **Title:** *Understanding Factual Errors in Summarization: Errors, Summarizers, Datasets, Error Detectors*
- **Authors or organization:** Liyan Tang, Tanya Goyal, Alex Fabbri, Philippe Laban, Jiacheng Xu, Semih Yavuz, Wojciech Kryscinski, Justin Rousseau, Greg Durrett
- **Date:** July 2023
- **URL or DOI:** https://aclanthology.org/2023.acl-long.650/ ; DOI 10.18653/v1/2023.acl-long.650
- **Source type:** Peer-reviewed ACL empirical meta-evaluation using aggregated primary annotations
- **Claim supported or weakened:** Weakens reliance on one factuality metric; performance varies significantly by summarization model and error type, and no metric is best in every setting.
- **Important limitations:** Aggregates nine existing datasets and is therefore not independent of all component benchmarks; summarization rather than staged research; evaluates error detection, not causal error propagation.

### C0002-SRC-14

- **Source ID:** `C0002-SRC-14`
- **Title:** *APEX-MEM: Agentic Semi-Structured Memory with Temporal Reasoning for Long-Term Conversational AI*
- **Authors or organization:** Pratyay Banerjee, Masud Moshtaghi, Shivashankar Subramanian, Amita Misra, Ankit Chadha
- **Date:** July 2026
- **URL or DOI:** https://aclanthology.org/2026.acl-long.749/ ; DOI 10.18653/v1/2026.acl-long.749
- **Source type:** Peer-reviewed ACL system paper
- **Claim supported or weakened:** Supports structured temporal state as an active mechanism; combines an entity-centric property graph, append-only history, conflict-aware multi-tool retrieval, and compact query-time summaries, reporting 88.88% on LoCoMo and 86.2% on LongMemEval.
- **Important limitations:** Components and added compute are bundled; no matched unstructured-trace inventory or cost; uses the same LoCoMo and LongMemEval benchmarks as `C0002-SRC-06` and `C0002-SRC-07`; benchmark accuracy does not establish provenance correctness or a freshness effect.

## Handoff to Alternative Theorist and Integrator

1. Treat `C0002-EXT-01` as the main identification result: the best near-direct evidence assigns effects to prior-context access and bounded relay fidelity. Do not convert it into evidence for a nominal fresh-container effect.
2. Preserve the three-condition decomposition. Full-trace persistent versus package-only persistent estimates an access-plus-context effect. Package-only persistent versus package-only fresh is causal only if a residual observable manipulation is named and verified; no external source located here supplies that residual.
3. Replace scalar “state completeness” with separate variables: schema compliance, predeclared inventory retention, task-relative dependency coverage, package size, transformation type, and write-versus-retrieval loss.
4. Treat contamination reduction and interface loss as competing outcomes of the same filtering operation. `C0002-SRC-01` supplies both directions within one framework.
5. Do not infer improvement from fewer unsupported claims without coverage, claim count, task completion, and citation completeness. `C0002-SRC-09`, `C0002-SRC-11`, and `C0002-SRC-13` are the strongest safeguards.
6. A useful branch-local experiment would inject predeclared claims, qualifications, support links, objections, contradictions, and unresolved dependencies; verify their presence in each package; and score preservation, omission, status change, contradiction, correction, and amplification with human adjudication and reliability reporting.
7. Compute remains unresolved. The branch should predeclare a primary budget and a saved-budget rule before interpreting any package or access contrast.
8. Transfer remains uncertain. None of the fourteen sources directly tests open-ended multi-source research synthesis with B001-style epistemic typing and staged error lineage.
9. Strongest supporting finding: prior trace can create unreliability and task interference, while selective structured state can preserve performance with much less context in some regimes.
10. Strongest weakening finding: the closest direct study shows that benefits shrink or reverse when relay compression loses task-relevant information, and no located study isolates a residual fresh-invocation effect after package and trace access are matched.
