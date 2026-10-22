# Adaptable TPAMI research-paper outline

This is a planning scaffold, not the official IEEE submission template. Replace or remove the prompts before producing manuscript prose.

## Title and abstract

- Name the problem and distinguishing mechanism or contribution.
- Abstract: task/need → concrete gap → insight and mechanism → evidence → bounded implication.
- Confirm the applicable word limit; the checked Computer Society regular-paper guidance is 100–200 words.

## 1. Introduction

- What important capability is missing in the specified setting?
- What observable limitation of existing work explains the gap?
- What insight motivates this method?
- What does the paper establish, and where is the evidence?
- If applicable, disclose the conference precursor and the journal additions.

## 2. Related work

- Organize by the decisions that distinguish competing approaches.
- Compare with the closest work under the same task and supervision assumptions.
- Explain how each research line informs or differs from the proposed approach.

## 3. Problem formulation and method

- Inputs, outputs, training resources, inference resources, notation, and objective.
- Overview figure and end-to-end data flow.
- Components: motivation, operation, interface, and verification.
- Training objective and procedure; inference algorithm and cost.
- Theory or assumptions only when they are part of the contribution.

## 4. Evaluation

- Questions linked to the claim–evidence matrix.
- Datasets/splits, leakage controls, metrics, baselines, implementation, and budgets.
- Main comparisons; component/interaction ablations; generalization and stress tests.
- Efficiency; qualitative successes and representative failures.

## 5. Discussion and limitations

- What the evidence establishes and what it leaves open.
- Failure regimes, assumptions, resource requirements, and relevant societal implications.

## 6. Conclusion

- The established contribution, its scope, and the most direct unresolved question.

## Supporting material

- References, funding and acknowledgments, applicable declarations.
- Supplement: reproducibility details, proofs, additional results, and evidence too detailed for the main narrative.

For a dataset paper, put construction, annotation, and evaluation protocols before method comparisons. For a theory paper, organize around assumptions and results. For a survey, replace the proposed-method narrative with scope, taxonomy, comparison, and evidence-backed open problems.
