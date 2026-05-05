# Stage I — Scope Freeze and Repository Skeleton

**Duration:** 0.75 day (target: Day 1).
**Lead:** Brian, with Helena for Task 1.2 and Task 1.3.

## Objective

Lock the outline at v3, create the repository skeleton so every chapter has a `.tex` file waiting to be written, choose the canonical build route, consolidate the bibliography, agree the author split section by section, and commit the figure and table plan.

## Tasks

| # | Task | Owner | File |
|---|---|---|---|
| 1.1 | Produce `TQFT_outline_v3.tex` — **done 2026-05-03** | B | [01_1_outline_v3.md](../tasks/01_1_outline_v3.md) |
| 1.2 | Walk Helena through v3 and confirm ownership | B+H | [01_2_author_split_walkthrough.md](../tasks/01_2_author_split_walkthrough.md) |
| 1.3 | Decide MTC-formalism ownership | B+H | [01_3_mtc_ownership.md](../tasks/01_3_mtc_ownership.md) |
| 1.4 | Create `paper/main.tex` with `\include` skeleton — **done 2026-05-03** | B | [01_4_main_tex_skeleton.md](../tasks/01_4_main_tex_skeleton.md) |
| 1.5 | Create merged `paper/tqft_review.bib` — **done 2026-05-03** | B | [01_5_merged_bibliography.md](../tasks/01_5_merged_bibliography.md) |
| 1.6 | Create shared `paper/preamble.tex` — **done 2026-05-03** | B | [01_6_shared_preamble.md](../tasks/01_6_shared_preamble.md) |
| 1.7 | Commit `paper/figures/` skeleton — **done 2026-05-03** | B | [01_7_figures_directory.md](../tasks/01_7_figures_directory.md) |
| 1.8 | Figure checklist (generate / extract / skip) — **done 2026-05-03** | B+H | [01_8_figure_checklist.md](../tasks/01_8_figure_checklist.md) |
| 1.9 | Table checklist — **done 2026-05-03** | B | [01_9_table_checklist.md](../tasks/01_9_table_checklist.md) |
| 1.10 | Build route + `plan/notes` / `plan/presentation` scaffold — **done 2026-05-03** | B | [01_10_build_and_scaffold.md](../tasks/01_10_build_and_scaffold.md) |
| 1.11 | Global figure policy (no LLM-generated TikZ for topology) | B | [01_11_figure_policy.md](../tasks/01_11_figure_policy.md) |
| 1.12 | Seed claim verification ledger | B | [01_12_claim_ledger.md](../tasks/01_12_claim_ledger.md) |

## Acceptance criteria

- `paper/main.tex` compiles in the chosen build route from Task 1.10 and contains a title page, table of contents, and placeholder chapters that say "To be written in Stage X."
- `paper/tqft_review.bib` contains every citation that will be needed in Parts I and II; every entry is verified against a DOI or arXiv number.
- Helena has signed off on her chapter ownership in `plan/notes/author_split_decisions.md`.
- Figure checklist enumerates every image the paper will contain; each item is tagged `generate` (we'll draw it), `extract` (with credit), or `skip`.
- `plan/notes/claim_ledger.md` seeded (Task 1.12) and `plan/presentation/README.md` exists.
- `paper/figures/POLICY.md` exists (Task 1.11) and `paper/figures/README.md` tags each figure as `tikz`, `handdraw`, or `redraw-from-source`.

## Risks

- **MTC ownership dispute.** If Brian and Helena disagree on who owns the formalism in Chapter 10, Chapter 10 can stall in Stage IV. Mitigation: Task 1.3 forces the decision now.
- **Orphan citations.** Merging three bibliographies can introduce duplicates and broken keys. Mitigation: run the bibliography-validation step supported by the chosen build route after the merge.
- **No local LaTeX toolchain.** Later stages should not assume `latexmk` exists locally until Task 1.10 fixes the compile route.
