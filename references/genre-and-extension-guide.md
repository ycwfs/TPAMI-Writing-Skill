# Article types and conference-to-journal extensions

Use a structure that makes the contribution testable. The outline of a benchmark or theorem paper can differ substantially from that of a new network. These are recommendations informed by the corpus, not mandatory TPAMI section orders.

## Method and empirical learning papers

The core argument is a diagnosed limitation, a mechanism addressing it, and evidence that isolates its effect under a defined setting. A typical organization is introduction, related work, formulation/method, experiments, discussion/limitations, and conclusion. Preliminaries can be part of the method or a separate section.

**Useful models:** P006 separates its two stages and examines different model configurations; P026 defines the adaptation problem before component design; P030 separates main experiments from ablations and qualitative analysis. These variations show that even within method papers, one fixed order is unnecessary.

**Evidence priorities:** the closest fair comparator, a diagnostic for the original failure, controlled component tests, meaningful generalization conditions, and cost reporting if efficiency is a claim. Additional data or compute should be reported as a resource difference rather than silently attributed to the method.

## Theory and optimization papers

Organize around the unresolved result, definitions, assumptions, central theorem, proof strategy, comparison to existing guarantees, and implications. Experiments can illustrate consequences when appropriate but are not a substitute for proof.

P047 provides an **abstract-level** example: the claim concerns nonconvex stochastic-optimization generalization, with stronger conclusions under additional assumptions. P050 is a **full-text method/optimization example**, not a pure theory substitute: it motivates fixed-point iteration cost and evaluates a learned solver's accuracy and speed.

**Evidence priorities:** correct assumptions, meaningful improvement at comparable assumptions, transparent constants/dependencies, boundary cases, and a clear distinction between guaranteed and empirically observed behavior. Do not require a theorem of an otherwise empirical paper merely because the target is TPAMI.

## Dataset and benchmark papers

Build the paper around why current evaluation is inadequate, what capability the new resource measures, how the resource was constructed, and what standardized experiments reveal. Data construction, annotation reliability, splits, and evaluation validity are central technical content.

P091 puts its dataset and benchmarks in dedicated sections, including a hidden test set. P094 separates the benchmark framework, datasets, experiments, and challenges. P098 organizes its construction section around “Why, What, How.” P025 combines data generation, a learning method, and an independently annotated evaluation set; it does not force all contributions into one method subsection.

**Evidence priorities:** coverage rather than size alone; meaningful held-out units; leakage and shortcut checks; annotation quality; reproducible baseline code; metrics that reflect the intended task; access and licensing information; and realistic boundaries on generalization.

## Survey and synthesis papers

State the scope, literature cut-off, inclusion/exclusion principles, taxonomy, comparison dimensions, and how conclusions were reached. Distinguish a narrative survey from a systematic review. Do not label a search systematic unless the procedures and screening justify that claim.

The corpus includes P008, P092, P093, and P099 as survey examples at **metadata/abstract level**; P099 also has an accessible repository manuscript whose TPAMI-version identity was not verified. P093 explicitly describes datasets, algorithm evolution, benchmarking, standards, and future directions in its abstract. This supports a survey outline but not a claim that its entire section structure was audited.

**Evidence priorities:** a useful organizing framework, faithful treatment of competing approaches, comparable evidence, transparent benchmark protocols if new experiments are included, and open questions grounded in demonstrated gaps. A long catalogue of papers is not by itself a synthesis.

## Multitask and foundation-model papers

Specify which capacities are unified, which components are shared, and which resources each task receives. Disclose training mixtures, label sources, contamination risks, prompts, inference budgets, and model versions. Explain when the claimed unification is architectural, procedural, or evaluative.

P082 compares a unified architecture across temporal action localization, sound-event detection, and audio-visual localization. Its component table reports parameter counts alongside multiple task metrics. P006 differentiates VQA models, language models, and multimodal models rather than treating all external engines as interchangeable.

**Evidence priorities:** comparable single-task and multitask alternatives; the effect of shared versus task-specific components; interactions and negative transfer; model/data/compute budgets; and a clear boundary between a benchmark result and a general capability claim.

## Conference-to-journal extensions

The prior conversation concerned this route, so the skill explicitly supports it. The present study also contains recent, author-identified extensions. Do not infer extension status from a “++” suffix or similar title.

### Establish provenance

Identify the exact conference paper, authors, year, and stable identifier. Check the journal manuscript's statement or author-maintained version record. Keep the conference contribution and journal addition separate in the [delta table](../assets/extension-delta-table.md).

### Make the scientific delta explicit

A substantive extension can deepen a mechanism, introduce a new setting, generalize a framework, add a theoretical result, expand a dataset to answer a new question, or provide a consequential analysis of limitations. Its strength depends on the coherence and evidence of those additions, not their labels.

Recent inspected examples:

- **P006, Prophet:** its introduction identifies a preliminary version and describes broader VQA/LLM instantiations, additional datasets, and Prophet++ with multimodal-model-derived heuristics. This illustrates connecting an extension to generality and a new mechanism.
- **P030, DynaPURLS:** the introduction identifies the earlier conference paper and explains dynamic refinement and broader evaluation. This illustrates a new inference capability with a matching analysis burden.
- **P069, motion prediction:** the repository explicitly identifies a CVPR 2023 precursor; the article separates weakly supervised and self-supervised settings. This illustrates a change in supervision assumptions that must be reflected in both formulation and comparison protocols.
- **P094, temporal graph clustering:** the introduction identifies new framework, dataset, and experimental contributions. The authors describe their expansion as “more than 50%”; that is the authors' description of this paper, **not a verified universal TPAMI percentage requirement**.
- **P003, creativity evaluation:** the introduction explicitly contrasts the conference version with a revised sampling/evaluation approach. This illustrates an extension centered on measurement design.

### Align the new claims with new evidence

For each claimed addition, record the changed assumption or capability, the closest alternative, the required comparison, the completed evidence, and the section/figure where it appears. Do not count a retained conference experiment as new evidence for an unrelated journal claim.

### Disclose the relationship

The checked Computer Society policy requires citation, substantive differentiation, notification, copies of related prior work, and a brief differences description. Use a concise manuscript statement and the required submission documentation. Do not conceal the precursor, rename it to obscure overlap, or present a text-similarity score as scientific novelty.

### Audit before polishing

Ask whether the journal's central question and answer are materially stronger, broader, or more complete than the conference version. If the only additions are a longer introduction and more benchmark rows, identify what question those results resolve before claiming a substantive extension. Do not promise acceptance from a fixed checklist.
