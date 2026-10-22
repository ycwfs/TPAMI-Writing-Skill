# TPAMI Writing Skill

A reusable Codex skill for planning, drafting, revising, and reviewing manuscripts for **IEEE Transactions on Pattern Analysis and Machine Intelligence (TPAMI)**, including conference-to-journal extensions.

The skill connects scientific claims to methods and evidence. It combines section-specific writing guidance, a 100-paper AI bibliography, inspected manuscript examples, and dated IEEE/Computer Society policy references.

## What it helps with

- Build a coherent argument: problem → diagnosed limitation → insight → mechanism → evidence → scope.
- Draft or audit 22 manuscript components, from title and abstract to experiments, limitations, supplementary material, and the cover letter.
- Adapt guidance to research, theory, dataset/benchmark, and survey articles.
- Explain substantive additions beyond a conference version, using a contribution-difference worksheet.
- Check whether each contribution has supporting methods, experiments, analyses, or proofs.
- Distinguish verified submission policies from editorial recommendations and observed writing patterns.

## Install in Codex

Clone this repository into a new `tpami-writing` directory inside your Codex skills directory. If that directory already exists, review your existing skill before replacing or updating it.

**Windows PowerShell**

```powershell
git clone https://github.com/ycwfs/TPAMI-Writing-Skill.git "$env:USERPROFILE\.codex\skills\tpami-writing"
```

**macOS / Linux**

```bash
git clone https://github.com/ycwfs/TPAMI-Writing-Skill.git ~/.codex/skills/tpami-writing
```

For a custom Codex configuration, use the `skills/tpami-writing` directory under your configured `CODEX_HOME`. Start a new Codex session after installation. Private repository access requires GitHub authentication and repository access.

## Example requests

```text
Use $tpami-writing to review this manuscript. Connect each contribution
to its method and supporting evidence, and prioritize concrete revisions.
```

```text
Use $tpami-writing to turn these research notes and verified results into
an introduction and experimental outline. Mark missing evidence explicitly.
```

```text
Use $tpami-writing to compare my conference paper with the journal draft.
Prepare an extension delta table and identify unsupported novelty claims.
```

Provide the relevant manuscript sections, results, and author notes. For a journal extension, provide both versions when available. The skill preserves the author's scientific claims and preferred language; it does not invent results or references.

## Contents

| File | Purpose |
|---|---|
| [SKILL.md](SKILL.md) | Core workflow and evidence rules |
| [Section guide](references/section-guide.md) | Guidance for 22 manuscript components |
| [Genre and extension guide](references/genre-and-extension-guide.md) | Article types and conference-to-journal extensions |
| [Official requirements](references/official-requirements.md) | Verified policies, source links, and unresolved requirements |
| [Evidence atlas](references/evidence-atlas.md) | Concrete examples from inspected manuscripts |
| [100-paper index](references/corpus-index.md) | Topic-balanced TPAMI bibliography with stable paper IDs |
| [Study methods](references/study-methods.md) | Selection, date conventions, access levels, and limitations |
| [Claim–evidence matrix](assets/claim-evidence-matrix.md) | Map contributions to supporting evidence |
| [Extension delta table](assets/extension-delta-table.md) | Document additions beyond the conference version |
| [Manuscript outline](assets/manuscript-outline.md) | Adaptable drafting scaffold |
| [Codex metadata](agents/openai.yaml) | Skill display name and example invocation |

## Evidence base and boundaries

The underlying study is dated **22 October 2026**, covering publication records from **22 October 2024 through 22 October 2026**. It includes **100 unique AI-related TPAMI papers**, with 10 papers in each of 10 topic areas. All selected DOIs were matched across Crossref, Europe PMC, and OpenAlex.

The date convention uses formal issue dates where assigned and indexed online/Early Access dates otherwise. Some issue-assigned articles first appeared online before the study window. The sample was purposefully balanced by topic; it is not an exhaustive or random survey of TPAMI.

Of 42 retrieved repository manuscripts, **19 explicitly associated with TPAMI** were used to inspect structure and selected passages. This does **not** represent a full, line-by-line reading of all 100 papers. Repository copies are not asserted to be identical to the publisher's final typeset articles. See [study methods](references/study-methods.md) for the full evidence boundaries.

The repository contains the reusable skill and its readable references. Raw source snapshots, research scripts, and downloaded paper PDFs are not distributed here.

## Policy handling

Follow current journal-specific instructions first, then Computer Society guidance, then general IEEE guidance. Recheck policies before submission. The recorded Computer Society guidance specifies a 100–200-word abstract for regular and special-issue papers. The study did not verify a current TPAMI-specific page cap or any universal numerical percentage required for a conference extension.

This is an independent writing resource, with no affiliation with or endorsement by IEEE or TPAMI. Writing guidance cannot guarantee acceptance.
