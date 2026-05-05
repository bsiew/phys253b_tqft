# Task 15.6 — Final PDF Compile and Page-Count Check

- **Status:** pending
- **Owner:** Brian
- **Duration:** 30 min
- **Stage:** [VII](../stages/stage_VII_presentation.md)

## Goal

Produce the final submitted PDF; confirm the page count meets the target of 110-120 main + roughly 10-15 appendix.

## Steps

1. Run the canonical compile command (see [`plan/notes/build_route.md`](../notes/build_route.md)) until refs and citations settle.
2. Page count: first count main-text pages (Chapters 1 through 14), then appendix pages.
3. If main > 120 pp: cut. Priorities to cut: SymTFT (Ch 8 §8.8), secondary experimental follow-up material, appendix spillover, then outlook compression.
4. If main < 110 pp: acceptable if the exposition is tight, but first check whether one omitted bridge subsection should return before artificially padding.
5. Filename: `TQFT_Review_Brittain_Siew_final.pdf`.

## Acceptance criteria

- PDF compiles cleanly.
- Page count within target.
- File ready for submission.

## Risks

- **Compile errors at the last minute.** Resolve immediately; if time-constrained, comment out the offending environment and submit without.
