# Stage IV — Part II Physical Applications

**Duration:** 2 days (target: Day 5 afternoon through Day 7).
**Lead:** Helena (Chapters 9, 11); Brian + Helena (Chapter 10).

## Objective

Write Chapters 9, 10, 11: topological order as infrared TQFT, anyons and modular data, and fractional quantum Hall as a physical realization.

## Tasks

### Chapter 9 — Topological Order as Infrared TQFT (~8 pp, Helena lead)

| # | Task | File |
|---|---|---|
| 9.1 | Draft §9.1 (long-range entanglement vs symmetry breaking) | [09_1_long_range_entanglement.md](../tasks/09_1_long_range_entanglement.md) |
| 9.2 | Draft §9.2 (toric code Hamiltonian, 4-fold torus GSD, full derivation) | [09_2_toric_code_gsd.md](../tasks/09_2_toric_code_gsd.md) |
| 9.3 | Draft §9.3 (emergent anyons from toric-code string operators) | [09_3_emergent_anyons.md](../tasks/09_3_emergent_anyons.md) |
| 9.4 | Draft §9.4 (infrared theory of toric code = $\mathbb{Z}_2$ BF, cite Ch 6) | [09_4_ir_bf_roundtrip.md](../tasks/09_4_ir_bf_roundtrip.md) |

### Chapter 10 — Anyons, Braiding, Fusion, Modular Data (~10 pp, joint)

| # | Task | File |
|---|---|---|
| 10.1 | Draft §10.1 (abelian vs non-abelian anyons, fusion, pentagon) (H) | [10_1_fusion_pentagon.md](../tasks/10_1_fusion_pentagon.md) |
| 10.2 | Draft §10.2 (braiding, hexagon, topological spin) (H) | [10_2_braiding_hexagon.md](../tasks/10_2_braiding_hexagon.md) |
| 10.3 | Draft §10.3 (derive modular $S$ for $U(1)_k$ from CS Hilbert space) (B) | [10_3_modular_S_U1k.md](../tasks/10_3_modular_S_U1k.md) |
| 10.4 | Draft §10.4 (CS connection: $U(1)_k$, $SU(2)_k$ tables) (B) | [10_4_cs_primary_labels.md](../tasks/10_4_cs_primary_labels.md) |
| 10.5 | Draft §10.5 (table: toric code / Laughlin / Ising anyons) (B+H) | [10_5_anyon_comparison_table.md](../tasks/10_5_anyon_comparison_table.md) |

### Chapter 11 — Fractional Quantum Hall Effect (~10 pp, Helena lead)

| # | Task | File |
|---|---|---|
| 11.1 | Draft §11.1 (Hall setup: Landau levels, filling, integer vs fractional) | [11_1_hall_setup.md](../tasks/11_1_hall_setup.md) |
| 11.2 | Draft §11.2 (Laughlin wavefunction → $U(1)_m$ CS effective theory) | [11_2_laughlin_to_cs.md](../tasks/11_2_laughlin_to_cs.md) |
| 11.3 | Draft §11.3 (quasiparticles as Wilson-line endpoints, cite CS Ex 6.4) | [11_3_quasiparticles.md](../tasks/11_3_quasiparticles.md) |
| 11.4 | Draft §11.4 (edge chiral boson, inflow link to Ch 8) | [11_4_edge_chiral_boson.md](../tasks/11_4_edge_chiral_boson.md) |
| 11.5 | Required honesty box on abelian vs non-abelian FQH status | [11_5_honesty_box.md](../tasks/11_5_honesty_box.md) |

## Acceptance criteria

- All three chapters compile as part of `paper/main.tex`.
- Chapter 9 derives the 4-fold toric-code GSD explicitly, not "one can show".
- Chapter 10 §10.3 derives modular $S$ from the $k$-dimensional CS Hilbert space (using `Proposition prop:dimU1k` of the CS chapter); no black-box Verlinde formula.
- Chapter 11 reuses the CS chapter's $\sigma_{xy} = e^2/(kh)$ derivation via citation, not duplication.
- The anyon comparison table in §10.5 is explicit, with labels/fusion/braiding/spin for all three systems.

## Dependencies

- Blocks: Stage V (experiments chapter references FQH setup from Ch 11).
- Depends on: Stage III (Ch 6, 7, 8) and Stage 0 (CS chapter).

## Risks

- **MTC formalism split.** If Task 1.3 did not cleanly assign §10.3 to Brian, expect stall here. Mitigation: revisit decision, push formalism to Appendix D if needed.
- **Helena's FQH chapter over-budget.** FQH is a huge topic; 10 pp is tight. Mitigation: the chapter's job is to connect FQH to the CS machinery, not survey FQH experimentally — experiments are Chapter 12.
- **Honesty-box tone.** Task 11.5 must be matter-of-fact, not hedging. See the outline's "Required honesty box" language.
