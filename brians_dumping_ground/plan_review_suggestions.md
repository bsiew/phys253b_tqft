# Review Notes on the Current `plan/` Tree

This document records suggested improvements to the current plan tree. It is intentionally non-destructive: it does not assume any of these changes have been made yet.

Scope of this review:

- I reviewed `plan/README.md`, `plan/plan_of_attack.tex`, all stage summaries, and a representative spread of task files.
- I cross-checked the plan against the current repo state, especially `paper/chern_simons_theory.tex`, `TQFT_outline_v2.tex`, and the existing folder structure.
- I also checked the current status of a few time-sensitive experimental references so the review does not inherit stale 2024/2025 placeholders.

## Overall assessment

The plan is strong in one important way: it decomposes the work into small enough units that another model or collaborator can pick up a task file and understand the intended output. The stage summaries are also useful.

The main problems are not about detail. They are about consistency and execution:

- the page budget and the day budget are both currently impossible,
- the plan is not yet aligned with the actual architecture of the existing Chern--Simons chapter,
- one of the outline's advertised deep dives has silently disappeared,
- some of the experimental tasks are already stale as of May 3, 2026,
- and several "compile / folder / label" assumptions are false in the current repo.

## Highest-priority fixes

### 1. The page budget is internally inconsistent

`plan_of_attack.tex` currently budgets about 145 pages of main text if the listed chapter targets are added literally. This directly conflicts with the stated target of `75-100` pages main text plus `15-25` appendix.

This is the single biggest structural problem in the plan.

Suggested fix:

- Add a one-page "budget reconciliation" task before any new chapter drafting begins.
- Decide which budget is real: either the paper is actually aiming for `120-150` pages, or the per-chapter targets must be cut now.
- If the `75-100` target is real, then Chapters 2, 3, 4, 6, 7, 8, 9, 10, 11, 12, and 13 all need smaller caps immediately, and some technical derivations need to move to appendices by design rather than by emergency trimming.

### 2. The stage timeline sums to 10 days, not 9

The planned durations for Stages I-VII add to `10` days, not `9`.

Suggested fix:

- Add an explicit "critical path / cut ladder" section.
- Mark tasks as `core`, `important`, or `stretch`.
- Define a hard fallback rule such as:
  - if Stage III slips, move the full `H^3(Z_N,U(1))` bar-resolution calculation to an appendix,
  - cut SymTFT from the main text entirely,
  - compress the condensed-matter inflow example,
  - and reduce Chapter 10 to the operational anyon/modular-data minimum.

### 3. The current paper architecture does not match the existing CS chapter

The plan assumes `paper/main.tex` can absorb `paper/chern_simons_theory.tex` cleanly. In the current repo, `paper/chern_simons_theory.tex` is still a standalone `article` document with its own preamble and `\begin{document}`/`\end{document}`.

There is also a content-level mismatch:

- the current CS file still behaves like a self-contained chapter draft,
- it includes forward pointers to a later "Chern--Simons and knot invariants" chapter,
- and its internal sectioning is not yet synchronized with a multi-chapter master file.

Suggested fix:

- Add a dedicated Stage I task called something like `1.x chapter-architecture-normalization`.
- Preserve `paper/chern_simons_theory.tex` as a standalone archival compile target until the very end.
- Create a new include-able body file such as `paper/ch05_chern_simons_body.tex` instead of destructively stripping the existing file early.
- Freeze one canonical document architecture before further drafting:
  - either `report`/`book` with real `\chapter`s,
  - or `article` with top-level `\section`s standing in for chapters.
- Right now the plan tries to do both. Task 1.4 explicitly mentions `article`, but its placeholders use `\chapter{...}`. That must be resolved first.

### 4. One of the outline's deep dives has disappeared

`TQFT_outline_v2.tex` explicitly keeps `Witten--Jones: CS => Jones polynomial via surgery` as one of the selected deep dives. The generated plan tree silently drops it as a planned chapter/task cluster, even though the current CS chapter still points forward to it.

This is a major conceptual drift from the agreed outline.

Suggested fix:

- Decide explicitly whether the Witten--Jones material is:
  - a real chapter,
  - a compact section inside the CS chapter,
  - a short survey subsection with citations only,
  - or fully cut.
- Do not leave it in the outline and the existing CS forward pointers while omitting it from the actual plan.
- If it is cut, then update the through-line and the CS chapter's forward references accordingly.

### 5. The appendix program is underspecified

The plan promises five appendices, but only Appendix B is really taskified. Appendix A, C, D, and E are mostly placeholders.

This matters because the plan repeatedly says "move technical details to the appendix," but the appendix writing itself is not fully scheduled.

Suggested fix:

- Add explicit appendix task files for each appendix.
- At minimum, create tasks for:
  - Appendix A: category theory minimum,
  - Appendix C: Chern--Simons global / level-quantization technicalities,
  - Appendix D: BF <-> `Z_N` details,
  - Appendix E: topological entanglement entropy derivation.
- Otherwise the "appendix escape hatch" is not operational.

## Repo and workflow fixes

### 6. The plan refers to folders that do not yet exist

The README and tasks refer to `plan/notes/` and `plan/presentation/`, but neither folder currently exists.

Suggested fix:

- Add explicit directory-creation tasks in Stage I.
- If `notes/` is supposed to be a living decision log, make that real before the plan starts being executed.

### 7. The build assumptions are false in the current workspace

The plan repeatedly requires `pdflatex`, `latexmk`, and `biber`, but this workspace currently does not have a LaTeX toolchain installed.

Suggested fix:

- Add a Stage I environment-bootstrap task.
- That task should decide the actual build route:
  - local TeXLive/MiKTeX,
  - Overleaf as canonical compile target,
  - or "draft locally, compile elsewhere."
- Do not make later stage acceptance criteria depend on tools that are not yet available.

### 8. `plan_of_attack.tex` is not self-compiling in its current form

The master plan cites many sources, but its inline bibliography only defines three entries.

Suggested fix:

- Either make `plan_of_attack.tex` citation-free,
- or give it a tiny companion bibliography so it actually compiles if you want to share the PDF.

### 9. There are two sources of truth, and they will drift

Right now the same planning content lives in:

- `plan/plan_of_attack.tex`,
- stage summaries,
- and task files.

That is workable, but only if one of them is explicitly canonical.

Suggested fix:

- Declare one canonical planning artifact.
- My recommendation: keep the task files canonical, keep the stage files as human-facing summaries, and treat `plan_of_attack.tex` as a generated narrative artifact or executive overview.

### 10. The naming convention is inconsistent with the actual filenames

The README says task files are named by stage number. In reality the filenames mostly follow chapter numbers: `02_*`, `03_*`, `04_*`, `06_*`, `07_*`, etc.

Suggested fix:

- Correct the README.
- If you keep the chapter-number naming scheme, say so explicitly.

## Content and scope fixes

### 11. The current Chapter 2 plan may create avoidable duplication with Chapter 5

Several Stage II tasks assume you will move forms/gauge-transform material out of the CS chapter and into Chapter 2. That is sensible in principle, but risky in practice because the existing CS chapter is already coherent and verified.

Suggested fix:

- Decide between two models now:
  - `Model A`: Chapter 2 becomes the canonical source of forms/gauge preliminaries, and Chapter 5 is refactored to depend on it.
  - `Model B`: Chapter 5 stays self-contained, and Chapter 2 is a lighter primer that does not forcibly centralize all earlier lemmas and labels.
- Do not half-move content. That creates brittle label dependencies and double maintenance.

### 12. Chapter 4 and Chapter 7 need clearer main-text vs appendix boundaries

The current plan wants:

- Chapter 4 to present the Frobenius classification theorem seriously,
- and Chapter 7 to compute `H^3(Z_N,U(1))` via the bar resolution in full.

Both are mathematically worthwhile. Together, inside a nine-day endgame, they are dangerous.

Suggested fix:

- Decide explicitly what must appear in the main text and what may live in appendices.
- Recommended split:
  - Chapter 4 main text: one direction in full, the converse at review level, appendix for the most technical generator-and-relation bookkeeping.
  - Chapter 7 main text: state the canonical cocycle, verify it is a cocycle, explain the `Z_N` classification, and move the full bar-resolution machinery to an appendix unless the schedule is clearly ahead.

### 13. Chapter 8's condensed-matter anomaly example should be reconsidered for coherence

The plan currently uses the 3D topological-insulator `theta = pi` bulk-edge story as the condensed-matter anomaly-inflow example.

That is a respectable choice, but it is not the tightest match to the paper's main through-line, which is TQFT as the infrared language of gapped phases, especially FQH and topological order.

Suggested fix:

- Decide whether the CM inflow example should instead be the FQH chiral-boson / bulk-CS inflow story.
- That example is more unified with the rest of the paper, easier to connect directly to Chapters 5 and 11, and likely easier for the target audience.
- If you keep the TI example for breadth, say explicitly that it is the "breadth" example and the FQH edge story is deferred to Chapter 11.

### 14. Topological entanglement entropy is missing as an actual task

The outline includes topological entanglement entropy in the topological-order arc, with a full appendix derivation. The generated plan barely operationalizes it.

Suggested fix:

- Add one main-text task for a short conceptual discussion of TEE in the topological-order chapter.
- Add one appendix task for the derivation.
- If it is not actually wanted, cut it cleanly from both the outline and the appendix list.

### 15. The generalized-symmetry chapter should be treated as a likely compression point

This is already partly acknowledged, but the plan could be sharper.

Suggested fix:

- Explicitly say that Chapter 8 is the first compression target if the schedule slips.
- Put the cut order in writing:
  - SymTFT paragraph first,
  - extra defect-language exposition second,
  - full TI example third,
  - but keep the dictionary table and one explicit inflow example no matter what.

## Experimental and citation fixes

### 16. The experiment shortlist is already stale as of May 3, 2026

The plan still refers to "Werkmeister 2024," but the peer-reviewed graphene paper is:

- Werkmeister et al., `Science 388, 730-735 (2025)`, published `April 10, 2025`, DOI `10.1126/science.adp5015`.

The plan should also decide whether to mention the newer 2025 results:

- Ghosh et al., `Nature Physics 21, 1392-1397 (2025)`, published `July 2, 2025`, DOI `10.1038/s41567-025-02960-3`.
- Ruelle et al., `Science 389, eadm7695 (2025)`, published `July 3, 2025`, DOI `10.1126/science.adm7695`.

Suggested fix:

- Refresh the Chapter 12 task list before writing begins.
- Either:
  - expand Chapter 12 to a deliberately selected `2020 + 2025` arc,
  - or state clearly that the chapter is not trying to be fully up-to-date and explain the cutoff.

### 17. The honesty box in Task 11.5 is too broad in its current wording

It currently groups several filling fractions and platforms under "directly measured" language that is stronger than the citations listed in the plan actually justify.

Suggested fix:

- Narrow the honesty box to the specific experimentally supported statements.
- Make the claims map one-to-one to actual cited platforms.
- Avoid sweeping statements like "Laughlin states `1/5` and Jain states `2/5, 3/7` have braiding statistics measured directly" unless you actually plan to cite the relevant experiments.

### 18. Figure-permission policy should default to redraw, not reproduce

Several tasks speak as if "reproduced with permission" is the default route. That is slow and uncertain.

Suggested fix:

- Make the default policy:
  - redraw schematically unless the source is open-license or permission is already explicit,
  - use literal reproduction only when that is clearly allowed.
- Add a tiny figure-rights ledger if you want this to stay organized.

## Style and proofing fixes

### 19. The prose purge is too aggressive in a way that conflicts with Brian's actual style

Task 14.11 bans phrases like "note that" and even "observe that," but Brian's style references use those naturally inside proofs.

Suggested fix:

- Ban AI filler, not normal mathematical connective tissue.
- Keep the ban on phrases like:
  - "we shall see,"
  - "the key statement is,"
  - "it can be seen/verified/shown,"
  - "an upshot of all this is."
- But do not globally ban ordinary proof language like "now observe" or "note that" when used naturally.

### 20. The plan should add a claim-verification ledger

The plan already cares about ghost references, but the execution model would be much stronger with a single place where every important claim is tagged:

- `derived here`,
- `derived elsewhere in paper`,
- `cited to source`,
- `moved to appendix`,
- or `cut`.

Suggested fix:

- Add a `plan/notes/claim_ledger.md` or `plan/notes/verification_matrix.md`.
- This is especially important for Chapters 4, 5, 7, 8, 10, and 11.

### 21. Hard-coded theorem/example references inside task files are brittle

Many task files already refer to labels like `prop:dimU1k` or example numbers that may change once the chapter architecture is normalized.

Suggested fix:

- Keep semantic labels like `prop:dimU1k`, but avoid human-written references to provisional example numbering such as "Example 6.4 of the CS chapter" inside planning docs.
- Those will drift.

### 22. Consider ASCII-normalized copies for LLM handoff

The markdown files use a lot of Unicode punctuation. That is fine locally, but since you plan to paste these into multiple web UIs, it increases the chance of mojibake and formatting corruption.

Suggested fix:

- Either normalize the planning docs to mostly ASCII punctuation,
- or generate a stripped ASCII handoff version before sending to other models.

## Presentation fixes

### 23. Brian's current board-script plan is not aligned with the actual level-quantization derivation

Task 15.1 currently phrases the minute-10 showpiece as `A -> A + d lambda`, which is not the actual large-gauge derivation you now have in the CS chapter. The verified derivation is the `SU(2)` non-abelian one using the winding-number integral.

Suggested fix:

- Make the presentation choose one honest route:
  - either present the actual `SU(2)` large-gauge derivation,
  - or present a different showpiece entirely, such as the abelian Wilson-linking phase or torus Hilbert-space dimension.
- Do not present an abelian shorthand as if it were the same theorem.

### 24. Presentation rehearsal needs to start before Stage VII

A joint dry run "at least 48 hours before the presentation" is incompatible with a schedule that only starts presentation work on the last day.

Suggested fix:

- Pull board-script drafting into Stage VI at the latest.
- Start individual timed runs before the paper is fully polished.

## Suggested questions to hand to Claude / Gemini

If you want a good next-round refinement prompt, I would ask for the following specifically:

1. Reconcile the page budget and produce a revised chapter-by-chapter target that really sums to `75-100` pages main text.
2. Reconcile the 9-day calendar and mark every task as `core`, `important`, or `stretch`.
3. Decide whether Witten--Jones is restored, compressed, or cut, and propagate that decision consistently through the outline, plan, and current CS chapter.
4. Produce a non-destructive repo architecture for integrating the standalone CS chapter into `main.tex`.
5. Add explicit appendix tasks.
6. Refresh the experimental chapter with the correct `Werkmeister 2025` citation and decide whether the 2025 Mach--Zehnder / time-domain anyon papers should be included.
7. Rewrite the prose-pass rules so they match Brian's actual proof style instead of banning ordinary mathematical connectives.
