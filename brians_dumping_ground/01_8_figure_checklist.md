# Task 1.8 — Figure Checklist

- **Status:** done (2026-05-03)
- **Owner:** Brian + Helena
- **Duration:** 20 min
- **Stage:** [I](../stages/stage_I_scope_freeze.md)
- **Priority:** core

## Result

Figure list frozen at **10 figures** and committed to `paper/figures/README.md`. Split: 7 hand-drawn scans for topological content, 3 TikZ block schematics for low-topology-content schematics. Upper-bound page cost ~1.5 pp across the paper.

### The reconciled list

| # | Figure | Chapter | Type | Owner |
|---|---|---|---|---|
| 1 | Cobordism generators (cap/cup/cyl/pair-of-pants) | Ch 3, Ch 4 | hand-drawn | B |
| 2 | Pair-of-pants multiplication/comultiplication | Ch 4 | hand-drawn | B |
| 3 | Hopf link for Witten–Jones bridge | Ch 5 | hand-drawn | B |
| 4 | Higher-form symmetry defect insertion | Ch 8 | hand-drawn | B |
| 5 | Bulk–boundary anomaly inflow schematic | Ch 8 | hand-drawn | B |
| 6 | Toric-code lattice with $A_v, B_p, W_1$ | Ch 9 | TikZ schematic | H |
| 7 | Anyon braiding worldlines | Ch 10 | hand-drawn | H |
| 8 | Interferometer comparison (Nakamura / Werkmeister / Andersen) | Ch 12 | TikZ composite | H |
| 9 | Ising fusion tree | Ch 10, Ch 13 | hand-drawn | H |
| 10 | Kitaev–Preskill subtraction geometry | App E | hand-drawn | B |

### Reconciliation with the earlier spec

The earlier spec had 8 figures. The final register has 10. Three changes:

| Change | Rationale |
|---|---|
| **Added** toric-code lattice (Ch 9) | Earlier spec cut this; restored because Ch 9 §9.2 derives the 4-fold GSD from $W_1, W_2$ string operators on a square lattice and "in words" does not suffice for the string-operator algebra. |
| **Added** Kitaev–Preskill geometry (App E) | Earlier spec did not have Appendix E as a taskified deliverable; the four-region subtraction geometry is required by the App E derivation of $\gamma = \log \mathcal{D}$. |
| **Merged** three separate experiment schematics into one composite | Composite side-by-side comparison reads cleaner than three isolated interferometer sketches and makes the synthetic-vs-natural editorial distinction visible in one glance. |

### Deliberate cuts (do not re-add without a scope conversation)

- Hall-bar geometry (Ch 11). Ch 11 derives $\sigma_{xy}$ symbolically; the diagram would be cosmetic.
- Separate interferometer figures (see "merged" above).
- BF phase diagram. The $\mathbb{Z}_N$ reduction is algebraic.
- Landau-level energy ladder. Helena to re-raise if drafting shows a need.
- MCG action diagrams for App B. Text suffices.

### Agreement recorded

Brian agrees (present at drafting). Helena walkthrough: pending Task 1.2; if she objects to any row, we amend this task and the register in the same edit.

## Goal

Freeze the list of figures so we don't add or drop any mid-stream.

## The list (working paper figure list; adjust only if scope changes)

1. Cobordism generators in 2D TQFT (Ch 4, TikZ, B)
2. Pair-of-pants multiplication/comultiplication diagram (Ch 4, TikZ, B)
3. Wilson-loop link diagram for CS (Hopf link shown) (Ch 5, TikZ, B — may already be in chapter)
4. Higher-form symmetry defect insertion picture (Ch 8, TikZ, B)
5. Bulk–boundary anomaly inflow schematic (Ch 8, TikZ, B)
6. Anyon braiding worldlines (Ch 10, TikZ, H)
7. Interferometer schematic for FQH experiments (Ch 12, redraw from Nakamura 2020 / Werkmeister 2025 as needed, H)
8. Fusion tree / braiding diagram for Ising anyons (Ch 13, TikZ, H)

## Cuts

- No toric-code lattice diagram. The Hamiltonian definition in words suffices.
- No BF-theory phase diagram. Reference Tong's notes.
- No FQH Landau-level energy diagram unless Helena decides it's necessary for Ch 11.

## Acceptance criteria

- Figure list above is committed to `paper/figures/README.md`.
- Both authors agree.
- Each figure has a target chapter and an owner.

## Risks

- **Permission issues on Figure 7.** Default to redraw schematically with citation; do not let permissions block Chapter 12.
