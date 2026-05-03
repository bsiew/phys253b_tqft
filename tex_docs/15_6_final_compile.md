# Task 15.6 — Final PDF Compile and Page-Count Check

- **Status:** pending
- **Owner:** Brian
- **Duration:** 30 min
- **Stage:** [VII](../stages/stage_VII_presentation.md)

## Goal

Produce the final submitted PDF; confirm the page count meets the target of 75–100 main + 15–25 appendix.

## Steps

1. `latexmk -pdf paper/main.tex` three times clean.
2. Page count: first count main-text pages (Chapters 1 through 14), then appendix pages.
3. If main > 100 pp: cut. Priorities to cut: SymTFT (Ch 8 §8.8), fault-tolerant discussion (Ch 13), outlook (Ch 14).
4. If main < 75 pp: unlikely, but if it happens, expand the CS chapter's discussion or add FQH material to Chapter 11.
5. Filename: `TQFT_Review_Brittain_Siew_final.pdf`.

## Acceptance criteria

- PDF compiles cleanly.
- Page count within target.
- File ready for submission.

## Risks

- **Compile errors at the last minute.** Resolve immediately; if time-constrained, comment out the offending environment and submit without.
