# Task 17.7 — Generate Figures

- **Status:** pending
- **Owner:** Brian + Helena (per owner in `paper/figures/README.md`)
- **Duration:** 3 hours
- **Stage:** [VI](../stages/stage_VI_integration.md)

## Goal

Produce the 8 figures from the Task 1.8 checklist, either as TikZ files or as extracted/redrawn images.

## Figures to produce

1. Cobordism generators (TikZ, B, Ch 4).
2. Pair-of-pants multiplication (TikZ, B, Ch 4).
3. Hopf link for Wilson loops (TikZ, B, Ch 5 or Ch 10).
4. Higher-form symmetry defect insertion (TikZ, B, Ch 8).
5. Bulk-boundary anomaly inflow schematic (TikZ, B, Ch 8).
6. Anyon braiding worldlines (TikZ, H, Ch 10).
7. FQH interferometer (extract or redraw, H, Ch 12) — Task 12.4.
8. Ising fusion tree (TikZ, H, Ch 13).

## Steps

1. For each TikZ figure: write the `.tex` source under `paper/figures/`, include via `\input{figures/figN_xxx}` or `\includegraphics` of a compiled PDF.
2. For the extracted figure: see Task 12.4.
3. Verify each figure renders correctly in the full compiled paper.

## Fallback

If TikZ becomes a time sink, hand-draw on tablet, export to PDF, `\includegraphics`. The rubric does not require vector graphics.

## Acceptance criteria

- All 8 figures present in compiled `main.pdf`.
- Captions are complete (one-sentence description + attribution if extracted).

## Risks

- **Time sink.** TikZ can consume hours. Switch to hand-drawn if blocked for > 30 min on any single figure.
