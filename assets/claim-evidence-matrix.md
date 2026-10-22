# Claim–evidence matrix

Complete this with supplied evidence before writing contribution bullets or the final abstract. One contribution may need several rows. Delete inapplicable rows.

| Claim | Scope and assumptions | Closest alternative | Evidence needed | Actual result / source | Main-paper location | Remaining uncertainty |
|---|---|---|---|---|---|---|
| Mechanism addresses a specified failure | State task, data, supervision, and inference setting | Name the closest method and its relevant design | Diagnostic plus controlled comparison | Record measured result; mark unrun work as planned | Method and analysis | Confounders or competing explanations |
| Component improves an outcome | Hold training/data/model budget fixed where feasible | Remove, replace, or simplify the component | Ablation with appropriate uncertainty | Metric and units | Ablation table | Interactions and variance |
| Method generalizes | Name the tested shifts or held-out domains | Comparable generalization protocol | Cross-domain, transfer, or held-out evaluation | Result for each condition | Generalization experiment | Untested domains |
| Method is efficient | Hardware, batch, input shape, precision, preprocessing | Same measurement boundary | Latency, throughput, memory, or cost measurement | Hardware-specific result | Efficiency table | Platform dependence |
| Bound or guarantee holds | Enumerate assumptions | Comparable prior theorem | Proof and a clear rate/assumption comparison | Theorem and proof location | Theory | Whether assumptions hold in experiments |

Do not fill this table with plausible numerical values. Use `[RESULT NEEDED]` or `[SOURCE NEEDED]` where the author has not supplied evidence.
