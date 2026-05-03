# Stage I — Scope Freeze and Repository Skeleton

**Duration:** 0.5 day (target: Day 1 morning).
**Lead:** Brian, with Helena for Task 1.2 and Task 1.3.

## Objective

Lock the outline at v3, create the repository skeleton so every chapter has a `.tex` file waiting to be written, consolidate the bibliography, agree the author split section by section, and commit the figure and table plan.

## Tasks

| # | Task | Owner | File |
|---|---|---|---|
| 1.1 | Produce `TQFT_outline_v3.tex` | B | [01_1_outline_v3.md](../tasks/01_1_outline_v3.md) |
| 1.2 | Walk Helena through v3 and confirm ownership | B+H | [01_2_author_split_walkthrough.md](../tasks/01_2_author_split_walkthrough.md) |
| 1.3 | Decide MTC-formalism ownership | B+H | [01_3_mtc_ownership.md](../tasks/01_3_mtc_ownership.md) |
| 1.4 | Create `paper/main.tex` with `\include` skeleton | B | [01_4_main_tex_skeleton.md](../tasks/01_4_main_tex_skeleton.md) |
| 1.5 | Create merged `paper/tqft_review.bib` | B | [01_5_merged_bibliography.md](../tasks/01_5_merged_bibliography.md) |
| 1.6 | Create shared `paper/preamble.tex` | B | [01_6_shared_preamble.md](../tasks/01_6_shared_preamble.md) |
| 1.7 | Commit `paper/figures/` skeleton | B | [01_7_figures_directory.md](../tasks/01_7_figures_directory.md) |
| 1.8 | Figure checklist (generate / extract / skip) | B+H | [01_8_figure_checklist.md](../tasks/01_8_figure_checklist.md) |
| 1.9 | Table checklist | B | [01_9_table_checklist.md](../tasks/01_9_table_checklist.md) |

## Acceptance criteria

- `paper/main.tex` compiles to a PDF containing a title page, table of contents, and placeholder chapters that say "To be written in Stage X." No errors.
- `paper/tqft_review.bib` contains every citation that will be needed in Parts I and II; every entry is verified against a DOI or arXiv number.
- Helena has signed off on her chapter ownership in `plan/notes/author_split_decisions.md`.
- Figure checklist enumerates every image the paper will contain; each item is tagged `generate` (we'll draw it), `extract` (with credit), or `skip`.

## Risks

- **MTC ownership dispute.** If Brian and Helena disagree on who owns the formalism in Chapter 10, Chapter 10 can stall in Stage IV. Mitigation: Task 1.3 forces the decision now.
- **Orphan citations.** Merging three bibliographies can introduce duplicates and broken keys. Mitigation: run `biber --validate-datamodel` after the merge.
