# Section-by-section TPAMI writing guide

This guide synthesizes observed examples and editorial recommendations. It does not claim that every practice occurs in all 100 papers or is required by TPAMI. Paper IDs resolve in [corpus-index.md](corpus-index.md); inspected sections and source locators are recorded in [evidence-atlas.md](evidence-atlas.md). Formal requirements are separated in [official-requirements.md](official-requirements.md).

## 1. Title

**Purpose:** let a specialist identify the problem, scope, and distinguishing contribution before opening the paper.

Prefer a task-plus-mechanism title or a memorable method name followed by an informative subtitle. A title can also name a scientific question, a dataset, or a theoretical result. State a task or setting when the method name alone is opaque. Keep terms aligned with those used in the abstract and experiments.

Examples of different functions in the corpus include P006's mechanism/task title, P026's architecture and adaptation setting, P047's explicit theoretical objective, and P091's dataset and application domain. Their differences are more useful than a universal title-word target.

**Revision checks:** Does each substantive word correspond to something established in the paper? Is “universal,” “general,” “robust,” or “efficient” broader than the evaluation? Would removing a decorative acronym improve discoverability? IEEE's general guide discourages “new” and “novel” in titles. Avoid placing unsupported priority claims in a title.

## 2. Abstract

**Purpose:** provide a self-contained miniature of the scientific argument.

For a regular paper, use the checked Computer Society default of **100–200 words**, subject to a current TPAMI-specific override. A useful sequence is:

1. Define the task and the practical or scientific need.
2. Identify one concrete limitation of existing approaches.
3. State the insight and the mechanism that addresses it.
4. Identify the evaluation setting and the principal supported finding.
5. End with a bounded implication or capability.

This is a functional sequence, not a mandatory five-sentence form. Allocate more space to the mechanism when it carries the novelty, and to protocol/coverage when the contribution is a benchmark. Do not use mathematical expressions or references in a submission abstract. Avoid unexplained acronyms.

P026 links loss of human cues under domain shift to a human-centric model and named benchmarks. P050 links fixed-point iteration cost to a learned solver and reports a scoped speedup. P047 illustrates a theory abstract: identify the unresolved analytical setting, summarize results and strengthened assumptions, and state their consequences. Its theoretical guarantees should not be rewritten as experimental performance claims.

**Result sentence template:** “On [datasets/settings], [method] improves [metric] by [absolute/relative amount] over [defined comparator] under [relevant resource condition].” Use this only when those facts are available. An accurate qualitative statement is preferable to an invented number.

**Revision checks:** Can a reader identify the gap, mechanism, evidence, and scope? Is the main result stated with units and a comparator? Does the abstract promise more than the results demonstrate? Are all claims unchanged by removal of promotional adjectives? Published abstracts in the corpus are not automatically good stylistic models.

## 3. Index terms

Choose discoverable terms describing the central task, method family, and setting. Use established terminology where possible, including the IEEE Thesaurus when useful. Avoid making every keyword a newly coined module name.

Keep keywords consistent with the title and problem formulation. Do not present a recommended keyword count as a TPAMI-specific rule unless verified in the current template or portal.

## 4. Introduction

**Purpose:** establish why the precise question matters and why the proposed approach is worth testing.

A productive progression is: relevant capability → specific unresolved limitation → diagnosis or observation → proposed insight → evidence-backed contributions. The motivating problem should survive the removal of the proposed architecture's name. If the “gap” is merely that nobody has combined two modules, explain the scientific limitation that the combination resolves.

Use a concrete failure, a controlled observation, or a sharply defined mismatch to establish the gap. P006 motivates its approach with missing visual information in captions and the difficulty of selecting examples. P027 uses a representation/storage/backbone limitation to motivate heatmap pooling. These are examples of linking a problem diagnosis to a mechanism.

Introduce the intuition before implementation details. Each contribution should state what is established and why it matters, rather than enumerate three components with different names. Map the contribution to a method, analysis, or experiment that can support it. Contribution bullets are optional; the number should follow the work.

For an extension, disclose the precursor and distinguish the new contributions near the end of the introduction or at the journal's required location. P006 and P003 provide contemporary examples of explicit extension statements. Do not imply that retained conference contributions originated in the journal version.

**Revision checks:** Is the closest competing approach represented fairly? Is the gap documented rather than asserted? Is the proposed insight understandable before the reader sees an equation? Does the evidence plan test the promised benefits?

## 5. Related work

**Purpose:** position the contribution against the alternatives that matter to its claims.

Organize around conceptual axes: supervision, representation, inference procedure, information access, objective, or evaluation regime. Use chronology only when it explains an important progression. End each group with a precise relationship to the present work.

Compare the closest approaches at the same level of abstraction. If the contribution changes the solver, compare solver assumptions and costs; if it changes the dataset, compare coverage, annotation, and splits. P026 separates human activity understanding, domain-adaptive recognition, and general adaptation. P025 uses its literature positioning to support a data-generation and evaluation argument.

Prefer “requires labeled target-domain data” to “cannot generalize,” and “evaluated on X but not Y” to “has limited performance” unless a direct comparison supports the latter. Distinguish “not studied in this cited paper” from “impossible for the method.”

**Revision checks:** Are the most relevant recent and foundational papers present? Is the claimed difference attributable to a specific source? Are conference and journal versions distinguished when their contributions differ? Could the reader understand the research landscape without following a long sequence of author names?

## 6. Problem formulation and preliminaries

**Purpose:** define exactly what the method is allowed to know and what it must predict or optimize.

Specify inputs, outputs, sample units, supervision, train/validation/test partitions, and deployment conditions. Introduce notation at first use and use one symbol for one object. For cross-modal, adaptation, continual, or few-shot settings, explicitly enumerate information available during training and inference.

Keep only the background needed to understand the contribution. Separate definitions from assumptions and established results from new propositions. P026 places problem formulation before its human-centric learning design; P006 includes preliminaries before the two-stage system; P012 introduces diffusion background before its synchronization mechanism.

**Revision checks:** Is unlabeled target data permitted? Are future frames accessible? Are class names or textual descriptions available at inference? Does a retrieval database contain test-derived information? Are pretrained model and API versions specified? These details can change the problem being solved.

## 7. Method overview

**Purpose:** give an end-to-end account before asking the reader to follow individual components.

Describe the data flow from input to prediction, highlighting the new operation. An overview figure should show training versus inference, frozen versus updated components, and externally supplied information when those distinctions matter. Explain how the objective and algorithm connect to the diagram.

The overview should answer: what is computed, in what order, with what resources, and why the new path addresses the diagnosed limitation? P006's separation into answer-heuristic generation and prompting is a useful staged example. P012's distinct 2D and 3D roles illustrate how to explain an interaction rather than merely name both branches.

**Revision checks:** Can a reader trace tensor/data interfaces without guessing? Does the prose explain the novelty that the figure depicts? Is a figure doing useful explanatory work rather than decorating an architecture list?

## 8. Technical components, objectives, and algorithms

For each component, connect **motivation → operation → interface → verification**. State the purpose of the component, define the transformation, explain how it fits the pipeline, and identify the experiment or argument that tests its role.

For an objective, define every term, weight, normalization, expectation, and optimization variable. Explain whether terms are jointly optimized, alternated, staged, or frozen. If a component is borrowed, cite it and focus the explanation on the changed part.

Separate the training algorithm from inference. Pseudocode is useful when updates, sampling, branching, or repeated optimization are difficult to infer from equations; it is unnecessary when it duplicates a short formula. State computational cost in the variables that govern it, and connect theoretical cost to measured efficiency where efficiency is claimed.

**Revision checks:** Can another researcher implement the component? Is the explanation of “why” independent of a favorable benchmark result? Does an ablation isolate its mechanism rather than change several budgets at once? Are numerical stability measures or stopping criteria essential to reproduction?

## 9. Theory and guarantees

**Purpose:** establish a precise result under explicit assumptions.

State the problem, assumptions, theorem, interpretation, and comparison to prior guarantees. Specify the probability space, norms, constants or hidden dependencies, asymptotic regime, and whether the guarantee concerns training loss, population risk, robustness, or optimization time.

A theoretical result earns its space by supporting a central claim or explaining a design choice. Do not insert a superficial theorem solely to imitate a journal style. P047's abstract explicitly separates nonconvex generalization bounds from stronger results under additional assumptions; this is an abstract-level example, not a claim that its proof was audited.

Provide the central proof idea in the main text when it supports understanding. Long derivations may go to the supplement if the theorem statement, assumptions, and scientific interpretation remain in the main paper. Empirical validation of a theorem's consequences must not be presented as a proof.

**Revision checks:** Are all assumptions stated where the result is used? Does the comparison hold at equal assumptions? Are claims about real data narrower than the formal statement's idealized setting? Are “causal” and “guaranteed” supported by the applicable identification or mathematical argument?

## 10. Dataset construction and benchmark design

**Purpose:** show why the resource measures a meaningful capability and how it was constructed reliably.

Document collection scope, inclusion/exclusion rules, annotation units, annotation instructions, quality checks, splits, licensing/access, and relevant participant protections. Report coverage and imbalance, not only total size. Explain which failure in existing benchmarks the new resource addresses.

State the evaluation protocol before ranking models. Define potential leakage routes and the independence unit for splitting: subject, scene, source video, identity, device, event, or document, as appropriate. Provide baseline implementations and explain what their performance reveals about the task.

P025 separates automatic training-data generation, the model, and an independently annotated evaluation dataset. P091 uses dedicated data and task descriptions before empirical evaluation. P003 devotes explicit sections to evaluation criteria and measurement. These examples support treating the benchmark's validity as part of the scientific contribution.

**Revision checks:** Could an apparent gain reflect overlap, annotation artifacts, language bias, or task shortcuts? Are labels and splits reproducible? Does the benchmark probe a capability rather than simply increase scale? Do comparisons separate model quality from resource access?

## 11. Experimental setup

**Purpose:** make the comparisons interpretable and reproducible.

Start with the questions the experiments answer. Document datasets and splits, metrics with direction, baselines, data/model budgets, tuning protocol, implementation, hardware, and random variation when relevant. Identify which baseline numbers were rerun, taken from papers, or obtained from an official leaderboard.

For foundation-model work, record model identifiers, checkpoint/API dates, prompting, decoding, retrieval, and token/call budgets. For video work, report frames, sampling rate, temporal window, views/crops, and whether future observations are used. For adaptation, disclose target-data access. For continual learning, disclose task order and replay resources.

P006 and P012 explicitly separate datasets, implementation details, and ablations. P025's evaluation protocol distinguishes zero-shot, feature-probe, and fine-tuning settings. A shared task name alone does not make such protocols comparable.

**Revision checks:** Are evaluation settings fixed before test results are examined? Is any tuning performed on the test set? Are pretrained resources comparable? Can readers distinguish a methodological improvement from more training, data, or compute?

## 12. Main results

**Purpose:** answer the main empirical question at a clearly specified operating point.

Write an interpretive result paragraph around each important table: question, result, comparison condition, and bounded inference. Avoid reading every table cell aloud. Explain meaningful exceptions instead of reporting only wins.

Use comparable protocols and mark noncomparable resource levels. Name metric units and whether gains are absolute or relative. A change from 80% to 82% is 2 percentage points or 2.5% relative, not an unspecified “2% improvement.” If reproducing a source claim with ambiguous units, inspect the underlying values before conversion.

Match uncertainty reporting to the design. Repeated runs, confidence intervals, paired evaluation, or bootstrap analysis may be relevant, but no fixed seed count was established as a TPAMI requirement. Do not imply statistical significance merely from a numerical difference.

**Revision checks:** Does every headline claim have a matching result? Are failures on relevant datasets visible? Is the strongest comparable baseline included? Is the stated improvement large relative to measured variation or evaluation uncertainty?

## 13. Ablations and mechanism analysis

**Purpose:** test the proposed explanation of why the method works.

Use removal, replacement, simplified alternatives, and interaction tests. Hold relevant budgets fixed, and state when a fair intervention cannot isolate a single factor. Parameter-matched or compute-matched controls are useful when an added component also increases capacity or cost.

Choose ablations from the contribution claims. If the method asserts cross-modal complementarity, compare each modality and their interaction. If it asserts better sampling, analyze sampling quality as well as final task accuracy. If an improvement is attributed to a new loss, separate its effect from a changed schedule.

P012 has explicit tests for guided sampling and 2D priors. P006 tests configurations of heuristics, VQA models, and language/multimodal models. These show how a section can examine both a mechanism and its range of applicability.

**Revision checks:** Could a result be explained by more compute, more data, or an easier baseline? Is there a simple alternative explanation worth testing? Is the prose identifying what the ablation actually isolates?

## 14. Generalization, robustness, and sensitivity

Define the perturbation or shift before claiming robustness: domain, sensor, viewpoint, resolution, noise, class distribution, temporal extent, adversarial threat, or missing modality. Specify which changes were anticipated in training and which were held out.

Report performance across conditions and relevant trade-offs. Distinguish a hyperparameter-sensitivity sweep from robustness to a distribution shift. Distinguish empirical resistance to a specified attack from a certified guarantee.

P012 reports a camera-elevation analysis and discusses a resolution limitation. P026 evaluates domain adaptation on specified benchmarks. P059's abstract illustrates how a fairness claim is bounded by a defined uncertainty set and datasets; its detailed mathematical argument was not audited in this study.

**Revision checks:** Does “generalizes” refer to tested domains or an unjustified universal claim? Are failed regimes shown? Is a robust result merely a higher clean-data baseline? Are threshold choices tuned fairly?

## 15. Efficiency and resource reporting

Measure the quantity named in the claim: latency, throughput, peak memory, training cost, energy, API calls, or storage. FLOPs and parameter count are useful descriptors but are not substitutes for wall-clock performance.

Define the measurement boundary, including preprocessing, feature extraction, retrieval, prompt construction, host-device transfer, and postprocessing when applicable. Report device, precision, input shape, batch size, warm-up, and synchronization. Show the accuracy–cost trade-off when multiple operating points are available.

P050 is useful for linking solver-level acceleration to inference behavior. P027 motivates a more compact representation. Do not transfer their numeric speedups to a different system or infer deployment readiness from a single device measurement.

**Revision checks:** Are competing methods measured under the same boundary? Is a large pretrained teacher or retrieval index omitted from the cost? Does the efficiency benefit remain at comparable accuracy?

## 16. Qualitative analysis, figures, and tables

Use visuals to test an explanation or expose a failure. Include representative examples, clearly defined selection rules where important, and matched baselines. Attention maps or embedding visualizations are descriptive evidence; they do not by themselves establish a causal mechanism.

An architecture figure should distinguish new from inherited components. A data figure should show distributions or coverage. A result plot should expose variation or trade-offs. A caption should identify the setting, symbols, units, and the conclusion the figure supports without forcing the reader to search several pages.

Tables need comparable conditions, metric directions, exact units, and intelligible emphasis. Distinguish an unavailable result from zero. Avoid excessive decimal places unsupported by variability. Keep figure text readable at final publication size.

P025 displays valid and erroneous automatically generated examples. P006 includes a human analysis of failure causes. These are stronger models for diagnostic presentation than a gallery of selected successes.

## 17. Discussion and limitations

**Purpose:** interpret what the evidence establishes, what it does not establish, and why that boundary matters.

Connect results back to the initial diagnosis. Discuss plausible competing explanations and circumstances that would invalidate the method's assumptions. Separate observed failures from plausible but untested risks. State costs, dependency on a pretrained model or external service, annotation limitations, and scope restrictions when they affect use.

A useful limitation names a condition, its effect, and the supporting evidence. “More datasets will be explored” is weaker than identifying a tested failure regime and explaining its cause. A limitation need not be a separately titled section if it is clear in the appropriate discussion.

P012 contains a dedicated limitations subsection tied to model/input constraints. P027 has a distinct discussion of applicability and challenges. P006's failure taxonomy illustrates a concrete error analysis. These examples motivate the function, not a mandatory section heading.

**Revision checks:** Are limitations scientifically specific? Are explanations tested or explicitly tentative? Does a stated broader implication remain inside the tested scope? Are relevant human or societal implications supported rather than appended as generic text?

## 18. Conclusion

Restate the established contribution at the level of insight or capability, supported by the scope of the results. Identify a focused unresolved question or practical constraint when useful. Avoid introducing new results, unreported datasets, or stronger claims than those supported earlier.

A concise conclusion can say what was learned, under which conditions, and what remains open. IEEE's general guidance explicitly cautions against inflating findings. It does not require the conclusion to repeat the abstract or list every contribution again.

**Revision checks:** Would the conclusion remain true if the strongest result table were removed? If not, is its dependence stated clearly? Are speculative applications marked as future possibilities?

## 19. References

Use references to support claims, identify the closest alternatives, and credit reused methods or data. Verify bibliographic details, and distinguish an Early Access DOI record from a final issue citation. Use the latest relevant journal version when discussing its additions, while citing the conference precursor when discussing provenance.

Follow IEEE's numbered reference order. Do not increase citation count to imitate a long TPAMI bibliography. Do not cite a paper as evidence for a claim based only on its title or abstract when the claim requires a particular experiment or theorem.

**Revision checks:** Does each factual comparison have an appropriate source? Do author names, title, venue, year, DOI, and version agree? Are preprints clearly identifiable? Is any citation included only to decorate a paragraph?

## 20. Supplementary material and reproducibility

Use the supplement for detailed proofs, complete hyperparameters, additional controls, extra qualitative examples, and implementation details that would interrupt the main argument. Keep definitions and evidence essential to the central contribution accessible in the main paper.

Organize it as a document with navigation and precise cross-references. Separate a proof from an empirical diagnostic. Provide dataset/split identifiers, preprocessing, environment, checkpoint identifiers, evaluation commands or pseudocode, and limitations on release where relevant.

The checked Computer Society guidance requires a separate supplemental file. Do not use extra material to silently change the claimed setting or conceal an essential baseline.

**Revision checks:** Do all main-paper links resolve? Can a reader reproduce the central comparison? Are code/data availability claims accurate? Are inaccessible or restricted resources identified without implying they are publicly released?

## 21. Authors, acknowledgments, funding, and declarations

Use verified author names, affiliations, contribution agreements, and funding information supplied by the authors. Apply the current IEEE and journal instructions for corresponding authors, equal contributions, funding placement, disclosures, human/animal research, conflicts, and AI-assisted content as applicable.

Do not fabricate approval numbers, licenses, funding identifiers, conflicts, or claims of public data availability. Distinguish declarations the author must supply from factual information already present in the manuscript. Do not infer that every computer-vision paper requires the same ethics statement.

## 22. Cover letter and submission positioning

State the manuscript's question, substantive contribution, fit to TPAMI, and the evidence supporting that contribution. For a conference extension, name the precursor and summarize the scientific delta; provide the prior paper and differences documentation required by the applicable policy.

Avoid claiming likely acceptance, citing journal prestige as scientific evidence, or promising results that are not in the submission. Treat suggested reviewers and administrative declarations as author-controlled information.

## Final coherence pass

Trace the same central argument across title, abstract, introduction, method, evaluation, and conclusion. Check for scope drift, renamed metrics, inconsistent notation, mismatched datasets, and unsupported comparative language. Prioritize fixes to the scientific argument over sentence-level polish.

Deliver a revision proportional to the request. A request to polish an abstract should not trigger unsolicited restructuring of the entire manuscript or invented new experiments.
