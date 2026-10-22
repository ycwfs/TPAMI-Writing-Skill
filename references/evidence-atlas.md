# Evidence atlas: sources behind the writing guidance

The following 19 papers have explicit TPAMI association in their repository version records. Selected sections and passages were inspected. Locations refer to the cached arXiv PDF revision, which can include supporting pages; they are not claims about the publisher’s exact pagination. Observations are separated from the writing recommendation derived from them.

## P003 — A Causality-Aware Paradigm for Evaluating Creativity of Multimodal Large Language Models

[TPAMI DOI](https://doi.org/10.1109/tpami.2025.3539433) · [Inspected manuscript, arXiv v2](https://arxiv.org/pdf/2501.15147v2) · [Version record](https://arxiv.org/abs/2501.15147)

**Locator:** Introduction and Sections 3–5; PDF pp. 2–8.
**Observed:** The article devotes named sections to the Oogiri evaluation platform, standard evaluation, and LoTbench. Its introduction explicitly contrasts the conference version with revised sampling and causality-aware evaluation.
**Writing recommendation:** When evaluation is a contribution, explain the construct, criteria, and measurement design as technical content. An extension statement should identify the changed scientific function.
**Interpretation boundary:** The section organization is evidence of writing practice; the study did not independently validate the proposed creativity measure.

## P006 — Prophet: Prompting Large Language Models With Complementary Answer Heuristics for Knowledge-Based Visual Question Answering

[TPAMI DOI](https://doi.org/10.1109/tpami.2025.3562422) · [Inspected manuscript, arXiv v4](https://arxiv.org/pdf/2303.01903v4) · [Version record](https://arxiv.org/abs/2303.01903)

**Locator:** Introduction; Sections 3 and 4; PDF pp. 2–14.
**Observed:** The method separates answer-heuristic generation from prompting, with preliminaries first. The experiments separate datasets, implementation, ablations, model combinations, and human analysis of failure causes. The introduction identifies a preliminary version and lists additional capabilities.
**Writing recommendation:** Connect a diagnosed failure to a staged mechanism, then use configuration tests and error analysis to explain what each stage contributes.
**Interpretation boundary:** The model/API instantiations are historical experimental settings, not recommendations to use a specific current commercial model.

## P012 — Gen-3Diffusion: Realistic Image-to-3D Generation Via 2D & 3D Diffusion Synergy

[TPAMI DOI](https://doi.org/10.1109/tpami.2025.3577067) · [Inspected manuscript, arXiv v2](https://arxiv.org/pdf/2412.06698v2) · [Version record](https://arxiv.org/abs/2412.06698)

**Locator:** Sections 3–5 and Section 6.1; PDF pp. 4–13.
**Observed:** Diffusion background precedes the coupled 2D/3D method. Experimental setup separates datasets, implementation, and metrics. Ablations test guided sampling and 2D priors. A limitations subsection discusses the resolution of the adopted model.
**Writing recommendation:** Explain complementary component roles and test them separately; attach limitations to the actual model or data dependency.
**Interpretation boundary:** Reported robustness to tested camera elevations does not establish robustness to arbitrary viewpoints or input domains.

## P025 — Learning to Answer Visual Questions From Web Videos

[TPAMI DOI](https://doi.org/10.1109/tpami.2022.3173208) · [Inspected manuscript, arXiv v2](https://arxiv.org/pdf/2205.05019v2) · [Version record](https://arxiv.org/abs/2205.05019)

**Locator:** Sections 3–6; PDF pp. 3–10.
**Observed:** The paper separates automatic VideoQA data generation, the learning procedure, the independently annotated iVQA evaluation dataset, and experiments. Evaluation distinguishes zero-shot, feature-probe, and fine-tuning settings; generated-data examples include failure cases.
**Writing recommendation:** For data-plus-method work, expose data construction and evaluation validity instead of hiding both inside a generic method section.
**Interpretation boundary:** The study inspected organization and representative examples, not the full collection pipeline or annotation process.

## P026 — Human-Centric Transformer for Domain Adaptive Action Recognition

[TPAMI DOI](https://doi.org/10.1109/tpami.2024.3429387) · [Inspected manuscript, arXiv v1](https://arxiv.org/pdf/2407.10860v1) · [Version record](https://arxiv.org/abs/2407.10860)

**Locator:** Sections 2–4; PDF pp. 3–7.
**Observed:** Related work is divided into human activity understanding, domain-adaptive recognition, and general adaptation. Problem formulation precedes the decoupled human-centric paradigm and its temporal/context interaction components.
**Writing recommendation:** Use related-work categories that explain the method’s decisions, and define target-domain information access before describing adaptation.
**Interpretation boundary:** The inspected protocol supports claims for the specified adaptation settings, not unrestricted cross-domain performance.

## P027 — Heatmap Pooling Network for Action Recognition From RGB Videos

[TPAMI DOI](https://doi.org/10.1109/tpami.2025.3640697) · [Inspected manuscript, arXiv v1](https://arxiv.org/pdf/2512.03837v1) · [Version record](https://arxiv.org/abs/2512.03837)

**Locator:** Introduction; Sections III–VI; PDF pp. 1–2, 5, 8, and 15.
**Observed:** The motivation identifies heatmap redundancy, storage, and backbone constraints. The paper has separate method, experiments, discussion, and conclusion sections, and discusses applicability beyond its principal scenario-specific datasets.
**Writing recommendation:** Tie efficiency and transferability language to the representation and tested operating conditions; use discussion to distinguish demonstrated from potential applicability.
**Interpretation boundary:** Potential applications in a discussion are not completed evaluations.

## P030 — DynaPURLS: Dynamic Refinement of Part-Aware Representations for Skeleton-Based Zero-Shot Action Recognition

[TPAMI DOI](https://doi.org/10.1109/tpami.2026.3680873) · [Inspected manuscript, arXiv v2](https://arxiv.org/pdf/2512.11941v2) · [Version record](https://arxiv.org/abs/2512.11941)

**Locator:** Introduction; Sections 3–7; PDF pp. 2–3 and 8–13.
**Observed:** The introduction identifies a conference precursor. The method introduces adaptive alignment and test-time feature refinement. Main experiments, ablations/qualitative analysis, and discussion are separate major sections.
**Writing recommendation:** When an extension changes inference behavior, state the additional information and adaptation operations and evaluate them under the corresponding protocol.
**Interpretation boundary:** Test-time refinement can change the evaluation setting; it must not be silently compared with methods denied the same access.

## P033 — Self-Supervised Learning of LiDAR 3D Point Clouds via 2D-3D Neural Calibration

[TPAMI DOI](https://doi.org/10.1109/tpami.2025.3584625) · [Inspected manuscript, arXiv v5](https://arxiv.org/pdf/2401.12452v5) · [Version record](https://arxiv.org/abs/2401.12452)

**Locator:** Introduction and Sections III–V; PDF pp. 1–2, 4–14; supplementary discussion pp. 17–21.
**Observed:** The argument distinguishes local pixel-point matching from holistic calibration and motivates a pretext task. Evaluation transfers the learned representation to multiple downstream 3D perception tasks; additional results and discussion follow in supporting pages.
**Writing recommendation:** For representation learning, connect the pretext objective to downstream utility and state which improvements belong to the representation versus the task-specific model.
**Interpretation boundary:** The repository PDF includes supporting material, so its 21 pages do not imply a submission page allowance.

## P034 — Glissando-Net: Deep Single View Category Level Pose Estimation and 3D Reconstruction

[TPAMI DOI](https://doi.org/10.1109/tpami.2024.3519674) · [Inspected manuscript, arXiv v1](https://arxiv.org/pdf/2501.14896v1) · [Version record](https://arxiv.org/abs/2501.14896)

**Locator:** Sections 3, 4, and 4.8; PDF pp. 3–11.
**Observed:** The paper distinguishes 3D information used in training from information unavailable at testing. Section 4.8 presents failure cases involving top occlusion and explicitly labels the proposed explanation as a hypothesis.
**Writing recommendation:** Make train/test resource asymmetry explicit and pair a concrete failure regime with a cautiously stated explanation.
**Interpretation boundary:** A plausible explanation of a failure is not automatically a demonstrated causal mechanism.

## P045 — A Reverse Causal Framework to Mitigate Spurious Correlations for Debiasing Scene Graph Generation

[TPAMI DOI](https://doi.org/10.1109/tpami.2025.3568644) · [Inspected manuscript, arXiv v1](https://arxiv.org/pdf/2505.23451v1) · [Version record](https://arxiv.org/abs/2505.23451)

**Locator:** Sections 3–4; PDF pp. 4–16.
**Observed:** The method defines a reverse-causal framework, while the setup enumerates different scene-graph evaluation modes and separates recall from mean recall. The paper includes component and hyperparameter analyses.
**Writing recommendation:** Define the estimand or target quantity and the evaluation regime before claiming a debiasing improvement; discuss trade-offs between metrics.
**Interpretation boundary:** The causal argument and proofs were not independently audited; the writing lesson is precise definition and scope, not endorsement of a causal guarantee.

## P050 — IGNN-Solver: A Graph Neural Solver for Implicit Graph Neural Networks

[TPAMI DOI](https://doi.org/10.1109/tpami.2026.3729092) · [Inspected manuscript, arXiv v2](https://arxiv.org/pdf/2410.08524v2) · [Version record](https://arxiv.org/abs/2410.08524)

**Locator:** Sections III–V; PDF pp. 3–11.
**Observed:** Preliminaries precede the solver design. Evaluation covers node and graph tasks, small and large graphs, baseline solvers, inference behavior, and ablations; additional setup is referenced in an appendix.
**Writing recommendation:** An efficiency argument should identify the bottleneck and measure the replacement at comparable accuracy and scale.
**Interpretation boundary:** Its reported speedups apply to its measured systems and cannot be transferred to another hardware or solver setting.

## P064 — Language-Inspired Relation Transfer for Few-Shot Class-Incremental Learning

[TPAMI DOI](https://doi.org/10.1109/tpami.2024.3492328) · [Inspected manuscript, arXiv v1](https://arxiv.org/pdf/2501.05862v1) · [Version record](https://arxiv.org/abs/2501.05862)

**Locator:** Sections 3–4 and Section 4.5; PDF pp. 3–12.
**Observed:** The approach explains visual-language transfer components. The experiments define base classes, incremental sessions, shots, and evaluation over seen classes. A limitations subsection discusses the representational restrictions of textual prototypes.
**Writing recommendation:** Define the incremental-learning protocol precisely and relate limitations to the actual representation, not only to a generic need for more data.
**Interpretation boundary:** Percent gains in an abstract require table inspection before deciding whether they are relative percentages or percentage points.

## P069 — Weakly and Self-Supervised Class-Agnostic Motion Prediction for Autonomous Driving

[TPAMI DOI](https://doi.org/10.1109/tpami.2025.3604036) · [Inspected manuscript, arXiv v1](https://arxiv.org/pdf/2509.13116v1) · [Version record](https://arxiv.org/abs/2509.13116)

**Locator:** Sections 3–6; PDF pp. 4–14.
**Observed:** The article separates formulation from different weakly/self-supervised motion-prediction variants. Evaluation states the sources of foreground/background supervision and motion ground truth. The repository identifies a CVPR 2023 precursor.
**Writing recommendation:** When supervision changes across variants, make label cost and permitted annotations central to both the method and the comparison.
**Interpretation boundary:** Reduced supervision must be compared at the stated annotation budget, not assumed to mean zero supervision.

## P079 — Learning Physics-Informed Noise Models from Dark Frames for Low-Light Raw Image Denoising

[TPAMI DOI](https://doi.org/10.1109/tpami.2026.3651447) · [Inspected manuscript, arXiv v3](https://arxiv.org/pdf/2310.09126v3) · [Version record](https://arxiv.org/abs/2310.09126)

**Locator:** Sections 3–5, especially 4.4 and 5.3; PDF pp. 3–16.
**Observed:** The method combines physical noise priors with learned components. Ablations evaluate both noise modeling and downstream denoising. Section 5.3 discusses practical limitations of noise metrics under non-independent noise.
**Writing recommendation:** Evaluate the intermediate modeling claim as well as the downstream outcome, and discuss when a metric’s assumptions fail.
**Interpretation boundary:** Good values under a metric do not by themselves guarantee perceptual or physical fidelity.

## P082 — UniAV: Unified Audio-Visual Perception for Multi-Task Video Event Localization

[TPAMI DOI](https://doi.org/10.1109/tpami.2025.3593932) · [Inspected manuscript, arXiv v3](https://arxiv.org/pdf/2404.03179v3) · [Version record](https://arxiv.org/abs/2404.03179)

**Locator:** Sections III–IV and Table IV; PDF pp. 3–12.
**Observed:** A unified framework covers temporal action localization, sound-event detection, and audio-visual localization. Component ablations report multiple task metrics and parameter counts.
**Writing recommendation:** For unified models, expose task-specific resources and interactions; report capacity alongside performance when architecture changes add parameters.
**Interpretation boundary:** A shared architecture should not be described as universal without evidence beyond the specified tasks.

## P085 — Rapid Salient Object Detection With Difference Convolutional Neural Networks

[TPAMI DOI](https://doi.org/10.1109/tpami.2025.3583968) · [Inspected manuscript, arXiv v1](https://arxiv.org/pdf/2507.01182v1) · [Version record](https://arxiv.org/abs/2507.01182)

**Locator:** Introduction and Section 3; PDF pp. 2–6; efficiency comparisons throughout evaluation.
**Observed:** The motivation distinguishes lightweight parameter counts from actual efficiency–accuracy trade-offs. It explains difference convolutions and an extension to spatiotemporal cues, and reports consumer-GPU and embedded-device results.
**Writing recommendation:** Use measured device-specific behavior to support efficiency claims and explain what changes when a spatial method is extended to video.
**Interpretation boundary:** The lesson is reporting the operating point, not copying the paper’s FPS figures into unrelated hardware claims.

## P091 — PhenoBench: A Large Dataset and Benchmarks for Semantic Image Interpretation in the Agricultural Domain

[TPAMI DOI](https://doi.org/10.1109/tpami.2024.3419548) · [Inspected manuscript, arXiv v2](https://arxiv.org/pdf/2306.04557v2) · [Version record](https://arxiv.org/abs/2306.04557)

**Locator:** Sections 3–6; PDF pp. 3–9.
**Observed:** The dataset section precedes benchmarks. The paper highlights accurate plant/leaf annotations, a hidden test set, multiple evaluation tasks, and released evaluation/baseline resources.
**Writing recommendation:** Explain annotation reliability, split independence, and the intended benchmark tasks as contributions alongside dataset scale.
**Interpretation boundary:** A hidden test split helps evaluation integrity but does not alone resolve every possible leakage or representativeness issue.

## P094 — Deep Temporal Graph Clustering: A Comprehensive Benchmark and Datasets

[TPAMI DOI](https://doi.org/10.1109/tpami.2025.3596609) · [Inspected manuscript, arXiv v1](https://arxiv.org/pdf/2601.12903v1) · [Version record](https://arxiv.org/abs/2601.12903)

**Locator:** Introduction; Sections 3–6; PDF pp. 2–15.
**Observed:** The paper separates a framework, dataset construction, experiments, and challenges. The introduction identifies new framework/data/experimental contributions beyond a conference paper. Experimental subsections are organized around explicit research questions.
**Writing recommendation:** Organize a multi-contribution paper so that each new resource or mechanism has a matching evaluation question and evidence.
**Interpretation boundary:** The authors’ “more than 50%” expansion statement is descriptive of their paper and is not a verified TPAMI novelty-percentage rule.

## P098 — ATRNet-STAR: A Large Dataset and Benchmark Toward Remote Sensing Object Recognition in the Wild

[TPAMI DOI](https://doi.org/10.1109/tpami.2026.3658649) · [Inspected manuscript, arXiv v6](https://arxiv.org/pdf/2501.13354v6) · [Version record](https://arxiv.org/abs/2501.13354)

**Locator:** Section 3 and Section 4; PDF pp. 6–14.
**Observed:** The dataset construction section is explicitly titled “Why, What, How.” It discusses the motivation, diversity, standardization, and statistical analysis before presenting benchmarks under different experimental conditions.
**Writing recommendation:** A dataset description should justify design decisions and show how the resource enables credible evaluation, not merely list counts.
**Interpretation boundary:** Benchmark coverage establishes performance under the chosen conditions; it does not prove real-world completeness.

## Additional abstract-level examples

These records support the stated abstract-level observations. They are not counted in the 19-paper journal-structure subset.

| ID | Observation from the abstract | Appropriate use |
|---|---|---|
| [P008](https://europepmc.org/article/MED/41525563) | Defines several multimodal adaptation/generalization topics and promises formal definitions, review, datasets, and open questions. | Survey scope and taxonomy; not evidence of its audited full-text section order. |
| [P047](https://europepmc.org/article/MED/41086086) | Separates nonconvex generalization results from stronger bounds under additional assumptions. | A theory abstract’s assumption/result organization; not proof validation. |
| [P059](https://europepmc.org/article/MED/41697808) | Ties fairness to a defined uncertainty set and states empirical and theoretical contributions. | Scope and assumptions in fairness claims; not independent certification of the guarantee. |
| [P073](https://europepmc.org/article/MED/40030787) | Connects a Retinex optimization model to learning-based initialization, unfolding, and adjustment. | Explaining the relationship between an optimization formulation and a network design. |
| [P086](https://europepmc.org/article/MED/39321010) | Distinguishes image, video, and unified referring-segmentation variants. | State task expansion and the corresponding evaluation scope. |
| [P093](https://europepmc.org/article/MED/40742848) | Describes datasets, algorithm evolution, international standards, comparative experiments, and future trends. | A survey/benchmark contribution should synthesize and compare, rather than only list papers. |
| [P100](https://europepmc.org/article/MED/42672027) | States slippage coverage, subject/image scale, a baseline model, and accuracy/throughput under a specified device setting. | A dataset abstract can combine resource coverage with a scoped evaluation result. |

## How evidence is used

The guide does not convert these examples into prevalence claims such as “all TPAMI papers require a theorem.” A section may be useful because it tests a paper’s claim even if it is absent from some examples. Such advice is an editorial recommendation. Formal policy statements come from the separately documented IEEE/Computer Society sources.
