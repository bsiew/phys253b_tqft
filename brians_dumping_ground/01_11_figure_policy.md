# Task 1.11 — Global Figure Policy

- **Status:** pending
- **Priority:** core
- **Owner:** Brian (drafts the policy) + Helena (agrees)
- **Duration:** 20 min (decision) + implementation folded into Task 14.7
- **Stage:** [I](../stages/stage_I_scope_freeze.md)

## Goal

Gemini (P1) flagged TikZ generation for topological diagrams as a latent time-sink. LLM-authored TikZ for braided categories, cobordisms, knot projections, and fusion trees tends to compile but render wrong physics. This task records the policy so we don't lose a day to it.

## Policy

1. **Default**: redraw schematically using minimal TikZ (straight lines, arrows, labeled circles). Every diagram must be hand-verified for geometric and topological correctness.
2. **Preferred for complex topology**: hand-draw on tablet or paper, scan, insert via `\includegraphics`. No TikZ for non-trivial knots, braid traces, or fusion trees with more than three nodes.
3. **Reproduced figures from journals**: only if the source is open-license (CC BY) or permission is already clear in the publisher's policy (e.g., author's personal reproduction rights for thesis work). For experimental figures in Chapter 12, default to redraw with citation in the caption: `Schematic based on [Nakamura et al 2020].`
4. **Not allowed**: ask an LLM to generate TikZ for any diagram requiring more than 5 geometric primitives. The cost of verification exceeds the generation savings.

## Figures the policy affects

| Figure | Category | Route |
|---|---|---|
| Cobordism generators | simple TikZ (boxes + arcs) | TikZ OK, B verifies |
| Pair-of-pants | simple TikZ | TikZ OK, B verifies |
| Hopf link (Ch 5) | topology | hand-draw, scan, insert |
| Higher-form defect insertion | schematic | TikZ OK, minimal |
| Bulk-edge inflow schematic | schematic (boxes + arrows) | TikZ OK |
| Anyon braiding worldlines | topology | hand-draw, scan |
| FQH interferometer | schematic | hand-draw or adapt |
| Ising fusion tree | diagrammatic | hand-draw, scan |
| Kitaev–Preskill 4-region (App E) | schematic | simple TikZ OK |

## Acceptance criteria

- `paper/figures/POLICY.md` exists and states the policy.
- `paper/figures/README.md` tags each figure as `tikz`, `handdraw`, or `redraw-from-source`.
- Any TikZ written in Task 14.7 is limited to the `tikz` figures above.

## Risks

- **Taboo on LLM TikZ breaks when someone is tired and asks for it anyway.** Mitigation: put the policy at the top of `paper/figures/POLICY.md` as a non-negotiable rule.
- **Hand-drawn scan quality.** Scan at ≥300 DPI and convert to PDF/vector before inclusion. Budget 30 min for figure cleanup in Task 14.7.
