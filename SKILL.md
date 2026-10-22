---
name: tpami-writing
description: Plan, draft, revise, or audit IEEE TPAMI manuscripts and conference-to-journal extensions. Use section-specific guidance, a recent 100-paper corpus, and verified IEEE policies to connect scientific claims to methods and evidence. Applies to research, theory, dataset/benchmark, and survey articles targeting TPAMI.
---

# TPAMI Writing

Help the author make a precise scientific argument that a TPAMI reviewer can assess and another researcher can reproduce. Preserve the author's results, intended scope, and preferred language. Improve the reasoning and evidence before polishing sentences.

## Choose the relevant guidance

- Drafting or revising a section: read the matching part of [section-guide.md](references/section-guide.md).
- Planning a whole paper, a theory paper, a dataset/benchmark, or a survey: read [genre-and-extension-guide.md](references/genre-and-extension-guide.md).
- Extending a conference paper: use the extension workflow in that same reference and [extension-delta-table.md](assets/extension-delta-table.md).
- Checking formal requirements: read [official-requirements.md](references/official-requirements.md). It separates verified policies from recommendations and records the verification date.
- Looking for examples: select relevant paper IDs in [evidence-atlas.md](references/evidence-atlas.md) or [corpus-index.md](references/corpus-index.md). Consult [study-methods.md](references/study-methods.md) before making claims about the sample.
- Building an outline or evaluating a draft: adapt [manuscript-outline.md](assets/manuscript-outline.md) and [claim-evidence-matrix.md](assets/claim-evidence-matrix.md). These are drafting aids, not mandatory journal templates.

Load only the references relevant to the current request. Do not require another literature search or the complete 100-paper corpus for a small local revision.

## Establish the argument

From the available manuscript, results, code, and author notes, identify:

1. The task, setting, permitted information, and intended scope.
2. The specific limitation of the closest prior methods and evidence that it matters.
3. The proposed insight and why its mechanism should address that limitation.
4. The claims that the supplied experiments or proofs actually support.
5. The limitations and, when applicable, the exact additions beyond a conference version.

If essential information is missing, ask a focused question while doing independent work. For a partial drafting request, use clearly labeled placeholders for missing values; do not turn planned experiments into completed results.

Map each substantive contribution to a method section and an experiment, analysis, dataset artifact, or theorem. A module list is insufficient when it does not explain the scientific contribution. A useful test is whether each claimed advantage would be falsifiable under a specified comparison.

## Write and revise

- Use problem → diagnosed limitation → insight → mechanism → evidence → scope as an argument sequence. Adapt section order to the article type rather than enforcing a fixed number of paragraphs or contributions.
- Define training and inference conditions before equations. Distinguish access to labels, extra data, pretrained models, retrieval sources, and test-time adaptation.
- Explain what each component does, why it is needed, and which evidence isolates its effect. Separate an architectural description from a justification of the design.
- Make comparisons auditable: identify datasets/splits, metric direction, protocols, model and data budgets, uncertainty when relevant, and whether baselines were reproduced or quoted.
- Report gains with metric names and absolute or relative units. Do not convert an author's “13%” into “13 percentage points” without checking the underlying table.
- Use “significant” statistically only when an appropriate analysis supports it. Benchmark gains alone do not establish causality, universality, or deployment readiness.
- Use corpus examples to understand rhetorical functions, not to copy wording, inherit numerical claims, or prescribe every observed practice. Published papers can contain overstatement.
- For references, preserve verified identifiers and cite the version actually used. Do not infer a paper's existence, venue, or journal-extension status from memory or title similarity alone.

## Apply policy at the right level

The corpus covers publication records within 2024-10-22 to 2026-10-22, with formal issue dates and Early Access dates distinguished. It is a purposeful sample, not a census or evidence of acceptance causality. Not every record has a verified journal-version full text.

Apply the current journal-specific instructions when available, then Computer Society journal guidance, then general IEEE guidance. Recheck changing numerical limits or submission rules when they affect the task. Do not substitute a survey's observed length, an arXiv page count, or a remembered page limit for policy.

For regular-paper abstracts, the verified Computer Society guidance specifies 100–200 words; the general IEEE “up to 250” advice does not override that more specific guidance. The study did not verify a current TPAMI-specific page cap, so do not invent one. Conference extensions require disclosure, citation, and substantive new contributions; no universal percentage threshold was verified.

## Deliver the requested work

For drafting, return the requested text plus material unresolved evidence needs. For an audit, prioritize findings by their effect on the argument and specify concrete repairs. Keep stylistic preferences separate from missing scientific evidence and formal requirements. If a claim lacks support, narrow it or propose the needed verification rather than manufacture evidence.
