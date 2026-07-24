# Alternative Theorist — C0002

## Strongest Current Interpretation

The strongest current interpretation is an **information-access and relay-fidelity tradeoff**, not an intrinsic benefit from a fresh conversation container.

Under this interpretation, persistent full-trace execution and package-mediated execution differ because the latter filters, compresses, reorders, and sometimes structures prior information. That operation can help when the prior trace contains premature commitments, mismatched-task residue, irrelevant material, or unsupported claims. The same operation can harm when it removes qualifications, temporal or causal relations, support links, objections, or other task-relevant dependencies. The direction of the effect therefore depends on what the package retains, what it excludes, how later stages retrieve it, the task’s dependency structure, model capability, and the resources consumed by creating and reading the package.

This interpretation is supported most directly by `C0002-EXT-01` and `C0002-SRC-01`: unlimited relay capacity can reproduce upstream context in the formal framing, while bounded relays create gains or reversals according to whether task-relevant information survives. `C0002-EXT-02` and `C0002-SRC-02`, `C0002-SRC-03`, and `C0002-SRC-08` support observable harms from earlier trace, task interference, and context position. `C0002-EXT-03` and `C0002-SRC-05` support a separate write-time retention bottleneck. `C0002-EXT-04` supports structured or selective state as an active intervention. The same record also weakens any universal reset benefit: `C0002-SRC-01`, `C0002-SRC-05`, `C0002-SRC-06`, and `C0002-SRC-07` show that compressed or retrieved state can lose valid information.

The interpretation remains qualified. No located study identifies a noncollapsed package-only persistent-versus-package-only fresh comparison after matching prior-trace inaccessibility, serialized inputs, instructions, tools, sampling and selection opportunities, model settings, and full inference cost. Therefore the evidence supports mechanisms involving access, compression, retention, salience, and state use, but does not establish a residual fresh-container effect.

## Alternative Theory 1

### Context-Salience and Retrieval-Geometry Theory

- **Core claim:** Apparent benefits or harms attributed to fresh execution may arise mainly from where relevant information appears, how much irrelevant context surrounds it, and how easily later stages retrieve it—not from contamination by earlier conclusions or from semantic information loss alone.
- **Evidence status:** Evidence-backed as a plausible alternative mechanism; not directly tested in B001-style staged research synthesis.

### Mechanism

A persistent trace can contain all necessary evidence and still perform poorly because relevant material is buried, duplicated, separated from its qualification, or placed in a low-salience region. A concise package can improve performance by moving selected facts to prominent positions and reducing retrieval competition, even when it does not remove any false claim. Conversely, a package can preserve the same atomic items but alter adjacency, order, or relation cues so that downstream stages fail to connect them.

This mechanism differs from the strongest interpretation in emphasis. The information-bottleneck account focuses on what is retained or lost. The salience account predicts meaningful differences even when the same reference inventory is retained, because ordering, grouping, redundancy, and context length change effective usability.

### Evidence it explains

- `C0002-SRC-08` directly supports position-sensitive context use: the same relevant information can produce different performance depending on its position in a long input.
- `C0002-EXT-02` notes that full-trace access changes context length, position, salience, and retrieval difficulty, so “more information” is not a unitary advantage.
- `C0002-SRC-04` is consistent with selective condensation helping partly because it reduces distractors and foregrounds selected content, even though it also changes prompts and compute.
- The ambiguity in `C0002-SRC-02` and `C0002-SRC-03` can also be partly explained by information timing and target-task material being embedded after earlier turns, rather than only by commitment to false beliefs.
- It explains why byte-identical inventories need not yield functionally equivalent use, matching the Explorer’s and Critic’s warning that equality of supplied items does not guarantee equality of retrieval or salience.

### Evidence it struggles with

- It does not by itself explain evidence that memory systems discard supporting evidence at write time, as diagnosed in `C0002-SRC-05`; absent evidence cannot be recovered through better positioning.
- It does not fully explain error persistence specifically associated with premature assumptions or earlier wrong turns in `C0002-SRC-02` unless those effects are mediated by repeated or salient placement.
- It cannot explain benefits from structured temporal graphs or explicit conflict handling in `C0002-SRC-14` when those benefits depend on relations and tools not present in a reordered raw trace.
- It does not establish whether salience effects are large enough in open-ended multi-source research to dominate retention, verifier quality, or task decomposition.

### Predictions

1. With the information inventory held constant, outcomes will vary when package order, evidence position, adjacency of claims and qualifications, or irrelevant-context volume is varied.
2. Moving the same verified package to the beginning or end of a persistent context should recover part of an apparent fresh-context advantage without changing invocation continuity.
3. A persistent condition receiving a concise package appended prominently while retaining inaccessible or ignored prior trace may perform similarly to a fresh package-only condition.
4. Effects should correlate more strongly with context length, relevant-item position, and retrieval success than with the persistent/fresh label.
5. Explicit relation-preserving formatting should outperform a flat list with the same atomic item coverage when tasks depend on qualifications, contradictions, temporal order, or causal links.

## Alternative Theory 2

### Resource-Allocation, Sampling, and Orchestration Theory

- **Core claim:** Apparent gains from role separation, fresh stages, or structured state may be produced by unequal allocation of inference resources, better functional prompts, added tools, repeated candidate generation, selector opportunities, or favorable reporting rather than by the separation itself.
- **Evidence status:** Strongly supported as a confounding explanation; the evidence does not establish that it explains every observed effect.

### Mechanism

Fresh or staged systems often alter several resource channels at once. Shorter contexts can reduce input-processing cost and leave more budget for completion. Condensers, graph builders, retrieval agents, verifiers, and selectors add calls and privileged transformations. Role-specific instructions can be better prompts than a generic persistent instruction. Multiple stages can create repeated samples or revision opportunities, while a final integrator acts as a selector. Researchers may then report the best architecture, benchmark, model, prompt, or metric, producing a selection effect at the study level.

Under this theory, “role separation” is often a label placed on a bundle that includes more or differently spent compute, longer aggregate context across calls, more total generated tokens, additional sampling, prompt specialization, and stronger selection. Even under a nominal fixed token or step budget, conditions can differ in prompt tokens, accumulated-context processing, state construction, tool calls, candidate counts, final-answer budget, and the handling of saved compute.

### Evidence it explains

- `C0002-EXT-07` reports that no located source satisfies the full B001 compute ledger or supplies a generally reusable saved-budget rule.
- `C0002-SRC-04` adds a condenser and decider while reducing history tokens; its benefits could reflect both better prompting and reallocated processing.
- `C0002-SRC-05` adds a predictive write-time LLM call even when stored-state token budget and readers are controlled.
- `C0002-SRC-14` bundles graph construction, append-only memory, conflict-aware retrieval, multiple tools, and compact summaries.
- `C0002-SRC-01` matches maximum steps rather than all prompt, context, relay, tool, and final-answer costs.
- The accepted C0001 state already identifies added sampling, selector quality, prompt tuning, and compute allocation as alternative explanations for apparent multi-agent gains. C0002 does not remove those concerns.
- It explains why structured systems can outperform a raw-context baseline even if information exclusion has no intrinsic benefit: the structured system may receive an additional optimization pass and a better retrieval interface.

### Evidence it struggles with

- It does not fully explain `C0002-SRC-08`, where information position changes performance without requiring added calls or a selector.
- It does not eliminate the possibility of a real prior-trace interference effect in `C0002-SRC-02` and `C0002-SRC-03`; unequal resources can coexist with genuine interference.
- The fixed-reader, fixed-state-budget diagnostics in `C0002-SRC-05` provide some evidence that write quality matters beyond simple reader compute, although total end-to-end cost remains unequal.
- It cannot explain a future result that survives exact matching of visible inputs, total processing and generation budget, candidate count, selector access, tools, prompts, and saved-budget treatment.

### Predictions

1. Apparent fresh or structured-state gains will shrink when total input processing, output generation, state construction, tools, candidates, selectors, and final integration are charged to one declared budget.
2. Results will change depending on whether savings from shorter context are left unused, reallocated within the same stage, or reallocated to later stages.
3. A persistent single-context workflow given the same specialized stage prompts, number of samples, verification calls, and selector opportunities will recover much of the staged system’s gain.
4. Removing role labels while preserving the functional instructions will have little effect if prompt quality, not social-role framing, is operative.
5. Reporting all preregistered tasks, models, prompts, and metrics rather than best-performing combinations will reduce estimated average benefits and expose heterogeneous or null regimes.
6. Benefits attributed to “independent agents” will track candidate diversity and selector accuracy more strongly than the number of fresh conversations.

## Additional Alternative or Null Explanation

### State-Write Bottleneck Theory

- **Core claim:** The decisive event occurs when prior material is promoted into the stage package. Later outcomes are governed primarily by write-time selection, classification, and relation preservation; persistence or freshness matters only indirectly through the package-construction policy.
- **Evidence status:** Evidence-backed as an indirect state mechanism.

`C0002-SRC-05` provides the strongest support by separating write-side loss from retrieval-side loss and finding write-dominant failures in multiple tested memory baselines. `C0002-SRC-06` distinguishes indexing, retrieval, and reading. `C0002-SRC-07`, `C0002-SRC-09`, `C0002-SRC-10`, `C0002-SRC-11`, and `C0002-SRC-12` show that reference inventories, dependency structures, content retention, factual mutation, and correction can be measured in pieces.

This theory explains why a formally complete Markdown schema can still fail: the package may omit a qualification, reclassify a hypothesis as fact, separate a claim from its support, flatten a contradiction, or preserve text while changing epistemic status. It also explains why downstream retrieval improvements cannot repair evidence that was never written.

It struggles to explain cases where the same package performs differently because of context position, reader capability, or prior-trace interference. Its principal prediction is that, with the downstream reader and context fixed, outcomes will track package construction policy and measured dependency retention. A replay design that supplies exact archived packages to identical downstream stages should reproduce the difference even after removing the original persistent/fresh execution path.

### Residual-Boundary Null

- **Core claim:** After authorized prior trace, serialized inputs, role instructions, permissions, tools, model settings, candidate and selector opportunities, and full compute are matched, conversation-container continuity has no stable average independent effect.
- **Evidence status:** Plausible minimal explanation, but not established. The current record mainly shows non-identification and an absence of direct evidence.

This null is stronger than saying that no study has yet shown an effect. It proposes that the supposed residual factor may be operationally empty: once prior messages are unavailable and the same package is supplied, “persistent” and “fresh” can become functionally the same treatment. The Critic and `C0002-INT-05` identify this collapse risk, while `C0002-EXT-01` and the search-bounded gap in `04_external_evidence.md` show that no located source supplies a verified residual manipulation.

The null explains package-matched equality, but such equality would not confirm the theory unless the branch demonstrates that a nontrivial residual difference remained. It also cannot explain full-trace versus package-only differences, which belong to access, salience, retention, and cost. A valid test must first name an observable residual property; otherwise the correct conclusion is not “zero effect” but “no distinct treatment was implemented.”

## Hybrid Explanations

1. **Interference plus valid-dependency loss:** A prior trace can contain both harmful early commitments and useful qualifications. Package construction removes some of each. The net result depends on the relative mass and importance of contaminated versus valid material. This hybrid is directly compatible with `C0002-SRC-01`, which reports both benefits and reversals as relay sufficiency changes.

2. **State-write quality plus salience:** A package may retain the correct inventory but organize it poorly, or omit key items while prominently presenting the remainder. Write retention and retrieval geometry should therefore be measured separately. `C0002-SRC-05` and `C0002-SRC-08` support the two components.

3. **Structured state plus added compute:** Condensation, predictive writing, graph construction, and retrieval can improve state quality while also consuming additional calls and enabling better prompts or selection. Positive results in `C0002-SRC-04`, `C0002-SRC-05`, and `C0002-SRC-14` can reflect both mechanisms simultaneously.

4. **Task structure × model capability × relay fidelity:** Stronger models may extract value from redundant full context and be harmed by lossy relays, while tasks with weak cross-stage dependencies may benefit from aggressive filtering. Sequential, temporal, causal, or open-ended synthesis tasks may require higher dependency retention than separable subtasks. `C0002-SRC-01`, `C0002-SRC-06`, and `C0002-SRC-07` support treating these as interactions rather than nuisance variation.

5. **Prompt specialization plus contamination control:** A fresh role can receive a narrower and better instruction while also avoiding earlier framing. An observed gain may require both. Removing either the specialized prompt or the prior trace could reduce the effect.

6. **Measurement plus selection effects:** A concise condition can show fewer unsupported claims because it makes fewer claims, while a study can emphasize tasks or metrics favorable to that condition. Coverage, citation completeness, task completion, and preregistered aggregation are needed to prevent an apparent epistemic gain from being a measurement and reporting artifact.

## False Dichotomies or Framing Problems

- **Contamination reduction versus interface loss is not a clean either/or.** Both are consequences of filtering. The same package can remove an unsupported claim and a valid qualification simultaneously.
- **Fresh versus persistent is not one factor.** It can bundle prior-message access, context length, information position, new role prompts, permissions, tools, state format, and new model calls.
- **Complete versus incomplete state is a false scalar choice.** Schema compliance, reference-item retention, dependency coverage, relation preservation, package size, transformation type, and retrieval success can move independently.
- **More context versus less context confuses quantity with usability.** More context can preserve evidence while reducing salience; less context can improve retrieval while deleting dependencies.
- **Single-agent versus multi-agent obscures functional equivalence.** A persistent system can use staged prompts, samples, verifiers, and selectors; a nominal multi-agent system can be only repeated calls with lossy handoffs.
- **Boundary effect versus state effect may be an invalid partition.** If a fresh boundary is implemented only through state serialization and trace exclusion, state transfer and access are the observable treatments.
- **Accuracy versus factuality is incomplete.** A system can reduce unsupported claims while losing coverage, usefulness, citation completeness, or task completion.
- **Null versus benefit is premature.** A null can mean no effect, treatment collapse, weak manipulation, insensitive tasks, unreliable measurement, or opposing subgroup effects.

## Discriminating Tests

1. **Three-condition access decomposition:** Compare full-trace persistent, package-only persistent, and package-only fresh execution. The first contrast estimates authorized trace access plus context and cost. The second is interpreted as a residual boundary contrast only after an observable residual property is named and verified.

2. **Package replay test:** Archive exact packages produced under each construction policy and replay them to identical downstream readers with fixed prompts, tools, model settings, and budgets. If differences persist, they are attributable to package content or representation rather than the original boundary.

3. **Inventory-versus-geometry factorial:** Hold a predeclared information inventory constant while varying order, grouping, evidence position, claim-support adjacency, and irrelevant-context volume. This distinguishes semantic retention from salience and retrieval geometry.

4. **Write-versus-read decomposition:** Use oracle packages, complete stored packages, and retrieved packages with fixed readers. Measure which required items were never written, which were written but not retrieved, and which were retrieved but misused.

5. **Dependency-injection lineage test:** Before execution, inject known claims, qualifications, support links, objections, contradictions, and unresolved dependencies. Track each identity and epistemic status through package construction and final synthesis as preserved, omitted, retyped, contradicted, corrected, mutated, or amplified.

6. **Compute and saved-budget crossover:** Run each principal contrast twice: once with any saved budget left unused and once with it reallocated under a predeclared rule. Record input tokens, output tokens, state construction, tools, candidates, selectors, latency, and monetary cost by stage.

7. **Sampling and selector equalization:** Give persistent and fresh conditions the same number of candidate generations, verifier passes, and selector opportunities. Separately compare one candidate versus repeated sampling within the same continuity condition.

8. **Prompt and role-label ablation:** Preserve functional instructions while removing role names, then preserve role names while weakening functional instructions. This separates role framing from prompt specialization.

9. **Coverage-constrained evaluation:** Require a minimum predeclared factual coverage and task-completion threshold. Report unsupported-claim precision together with claim count, support correctness, citation correctness, citation completeness, coverage, usefulness, and omission severity.

10. **Task and model stratification:** Preregister separable, sequential, temporal, causal, and open-ended synthesis strata and multiple model capability levels. Test interactions instead of relying on one pooled average.

11. **Blinded evaluator and reporting audit:** Use multiple blinded evaluators, adjudication, and agreement reporting for lineage categories. Publish all preregistered conditions, tasks, metrics, and negative results; do not count reused benchmarks as independent replication.

12. **Residual-manipulation check:** Before accepting any package-only persistent-versus-package-only fresh test, document exactly what remains different, how it is observed, and why it is not merely a label or hidden access difference. If no property remains, classify the comparison as an implementation-equivalence check.

## Comparative Evidence Table

| Theory | Main mechanism | Evidence it explains well | Evidence or outcome it cannot yet explain | Most discriminating observation | Current status |
|---|---|---|---|---|---|
| Information-access and relay-fidelity tradeoff | Filtering removes both harmful trace and useful dependencies | `C0002-SRC-01` through the relay-sufficiency pattern; contamination evidence in `SRC-02` and `SRC-03`; dependency-loss evidence in `SRC-05` through `SRC-07` | A residual effect with byte-identical package, no trace access, and matched resources | Net outcomes track measured harmful-item exclusion and valid-dependency retention | Strongest current interpretation; qualified |
| Context-salience and retrieval geometry | Position, adjacency, context length, and distraction change effective use of retained information | `C0002-SRC-08`; parts of `SRC-02`, `SRC-03`, and `SRC-04` | Evidence never written into state; gains requiring new relational tools | Same inventory yields different outcomes under position and ordering changes | Evidence-backed alternative |
| Resource allocation, sampling, and orchestration | Added or differently allocated compute, prompts, tools, candidates, and selectors produce gains | `C0002-EXT-07`; bundled interventions in `SRC-04`, `SRC-05`, and `SRC-14` | Pure position effects; a future exactly cost-matched residual effect | Gains shrink under full ledger matching and sampling/selector equalization | Strong confound; incomplete explanation |
| State-write bottleneck | Package promotion and classification discard or mutate needed content before retrieval | `C0002-SRC-05`; staged memory and reference methods in `SRC-06`, `SRC-07`, `SRC-09` through `SRC-12` | Different performance from an exact same package caused by salience or reader differences | Package replay and write-versus-retrieval diagnostics localize failures to construction | Evidence-backed indirect mechanism |
| Residual-boundary null | No stable effect remains after all observable factors are matched | No direct residual study; treatment-collapse logic in Critic and `C0002-INT-05`; search gap in `04_external_evidence.md` | Full-trace access effects and any future verified noncollapsed residual effect | A verified residual manipulation produces no stable effect across powered strata | Plausible minimal explanation; unproven |
| Hybrid interaction | Multiple mechanisms change sign across task, model, state, and budget regimes | Conflicting results across `SRC-01`, `SRC-04`, `SRC-05`, `SRC-06`, `SRC-07`, and `SRC-08` | A simple uniform effect across all conditions | Significant preregistered interactions and mechanism-specific mediation | Likely framework, not yet quantified |

## Remaining Uncertainty

- No accepted operational definition identifies a residual invocation-boundary treatment after prior-trace access and visible inputs are equalized.
- No located source directly tests open-ended multi-source research synthesis using B001-style epistemic typing, provenance, staged permissions, and cross-stage claim lineage.
- The branch has no accepted canonical stage package, retention inventory, dependency reference, transformation policy, or state-replay protocol.
- No primary compute-matching rule, tolerance, or saved-budget policy has been selected.
- The relative contributions of write loss, retrieval failure, context salience, prompt specialization, added inference, repeated sampling, selector quality, and reporting bias are not quantified.
- Existing evidence does not establish whether contamination-control benefits generalize beyond multi-turn instruction following and task-switch settings.
- Existing dependency-loss evidence comes mainly from agentic benchmarks, conversational memory, retrieval, and summarization; transfer to research synthesis is uncertain.
- Measurement components exist, but no validated codebook follows the same claim and epistemic status across generation, criticism, evidence review, and integration with established reliability.
- A pooled average may conceal opposite effects across task structure, model capability, package retention, and stage location.
- The absence of an exact residual-boundary study is a search-bounded gap, not proof that no qualifying experiment exists.

## Handoff to Integrator

The Integrator should preserve the strongest current interpretation as a qualified **information-access and relay-fidelity tradeoff** and should not accept an intrinsic fresh-container effect. It should recognize at least three serious competing mechanisms: **context-salience and retrieval geometry**, **resource allocation/sampling/orchestration**, and **state-write bottlenecks**, plus the **residual-boundary null**.

The branch should replace the scalar “state completeness” language with separately measured schema compliance, reference-item retention, task-relative dependency coverage, package size, transformation type, write loss, retrieval loss, and relation/status preservation. Contamination reduction and interface loss should be treated as simultaneous possible outcomes of one filtering operation rather than as mutually exclusive theories.

The next accepted methodological step should be a preregistered three-condition access decomposition combined with package replay, dependency injection, coverage-sensitive lineage scoring, full compute and sampling accounting, prompt/role-label ablations, and explicit residual-manipulation checks. Until those controls exist, positive findings should be attributed to observable access, state, salience, prompt, tool, sampling, selection, or budget factors; null findings should not be treated as evidence against freshness when the comparison may have collapsed to functionally identical treatments.