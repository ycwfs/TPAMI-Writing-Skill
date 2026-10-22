# Corpus construction and evidence boundaries

## Scope and date convention

The study was conducted on **22 October 2026**. The requested two-year window is **22 October 2024–22 October 2026**, inclusive. It covers AI-related articles in *IEEE Transactions on Pattern Analysis and Machine Intelligence*, ISSN 0162-8828 / 1939-3539.

The final catalogue uses the **formal issue publication date when assigned**, and an **indexed online/Early Access date otherwise**. This convention is explicit because publication databases do not consistently preserve the earliest online date. A paper assigned to a recent issue may have appeared online earlier than the window. Therefore, this collection is not a claim that every article first became publicly available during these two years.

Month-only dates remain month-precision dates. The catalogue also preserves Europe PMC's reported first-publication date, electronic date when supplied, and OpenAlex's publication date. None of these fields is silently substituted for another. Nine records are represented as Early Access, with no invented final issue assignment.

## Retrieval and selection

1. Crossref's TPAMI journal endpoint, filtered by the two-year publication window and journal-article type, returned **2,169** records.
2. Europe PMC's TPAMI journal search with its `FIRST_PDATE` filter returned **2,094** records.
3. Matching normalized DOI values and requiring an abstract yielded **2,092** candidates. Editorials, corrections/retractions, very short abstracts, and weak topic matches were excluded from scoring; **1,432** candidates passed the working topic/date filters.
4. A purposeful sample selected **10 papers in each of 10 AI topic areas**, using title/abstract keyword scores and date diversification. Three manual replacements improved topic fit and survey coverage; a separate survey genre label and a duplicated mathematical title rendering were corrected.
5. All **100 unique selected DOIs** matched Crossref, Europe PMC, and OpenAlex. Metadata availability is not a quality ranking or a claim of statistical representativeness.

The final bibliography includes **8 papers with a 2024 issue date, 53 with a 2025 issue/Early Access date, and 39 with a 2026 issue/Early Access date**. Its primary genre labels are 89 research, 4 survey, and 7 dataset/benchmark records. These are operational labels; hybrid contributions can span genres.

The topics are foundation/multimodal models; generative/diffusion models; video/action/temporal understanding; 3D vision/rendering; theory/optimization/graphs; robustness/privacy/fairness/uncertainty; adaptation/label-efficient learning; low-level vision/restoration; recognition/detection/segmentation; and surveys/datasets/benchmarks. Category boundaries overlap, and equal category counts were chosen for writing-guide breadth rather than to estimate TPAMI's topic distribution.

## Access and inspection levels

| Evidence level | Number | What it supports |
|---|---:|---|
| DOI-verified journal records with abstracts | 100 | Bibliographic collection, topical scope, title/abstract description, and descriptive text-length statistics |
| Open-access locations identified | 46 | A potential lawful access route; this alone does not prove journal-version identity |
| arXiv repository records checked | 43 | Title and version metadata comparison |
| Repository manuscript PDFs retrieved and text extracted | 42 | Accessible full-text source copies; not all are confirmed journal versions |
| TPAMI-identified manuscripts used for structural inspection | 19 | Selected sections, section order, contribution statements, evaluation organization, and concrete writing examples |

The 19 structural examples are P003, P006, P012, P025, P026, P027, P030, P033, P034, P045, P050, P064, P069, P079, P082, P085, P091, P094, and P098. Author-maintained arXiv comments or journal/DOI metadata explicitly associate these manuscripts with TPAMI. They are repository copies, not claimed to be the publisher's exact final typeset version.

For another 23 retrieved manuscripts, a matching title and a journal DOI establish a useful paper association, but this study did not verify that the particular repository revision is the TPAMI version. They are not counted as journal-structure evidence. P088 was conservatively excluded from full-text analysis after a title discrepancy: Europe PMC gives a shorter title, while Crossref, OpenAlex, and arXiv give a longer title under the same DOI. The catalogue follows the Crossref/OpenAlex title and preserves the discrepancy note. Its journal publication identity is established, but the repository revision was not used for structural claims. Three additional OA locations were identified but not downloaded.

Structural inspection means the titles, relevant section headings, contribution/extension statements, and selected method/evaluation/discussion passages were inspected. It does **not** mean that all 100 papers were read line by line, their experiments reproduced, or their proofs independently verified. Theory and survey guidance draws on labeled abstract examples, official guidance, and explicit editorial recommendations where verified journal full texts were unavailable.

## What was measured

In the 100-record sample, whitespace-based title length has a median of **10 words**; abstract length has a median of **201 words**, with a range of **155–309**. These are descriptive corpus statistics affected by metadata formatting. They are not submission rules, recommended targets, or evidence that overlength abstracts are compliant.

The study does not report automated counts of section prevalence. PDF heading extraction can confuse table entries, footnotes, appendices, and wrapped headings. Those extracted candidates were used for navigation, with the concrete examples inspected before inclusion in the guide.

## Limits on inference

- This is a topic-balanced convenience sample with a further availability bias in the full-text subset. It is neither an exhaustive review nor a random sample of TPAMI.
- Only published/accepted work is included. There is no rejected-paper comparison group, so no writing pattern can be claimed to cause acceptance.
- Examples describe rhetorical functions; they do not endorse every author's wording or the truth of every empirical/theoretical claim.
- Paper length in a repository may include appendices or supplementary material and cannot determine the current submission page cap.
- A journal DOI validates publication identity; it does not by itself validate all metadata dates or match an arbitrary preprint revision.

## Reproducibility assets

The study workspace contains `corpus.json`, the CSV/BibTeX/Markdown exports, raw Crossref/Europe PMC/OpenAlex responses, arXiv metadata pages, manuscript PDFs and extracted text, curation records, the full-text manifest, official-policy source snapshots, and retrieval/export scripts. Stable paper IDs P001–P100 connect the bibliography and evidence atlas. The installed skill contains the readable bibliography and synthesis references; large raw source files remain in the study workspace.
