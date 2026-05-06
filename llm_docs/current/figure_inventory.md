---
created_at: "2026-04-29T01:28:29-04:00"
updated_at: "2026-05-05T19:14:31-04:00"
generated_by: "codex"
timestamp_source: "agent_clock"
updated_by: "claude-code"
---

# Figure Inventory

This is the active combined figure inventory for the simplified seven-section
253b final paper. It replaces the separate `figure_wishlist.md`; archived
wishlist entries that only served the old modular draft are not active targets.

| Figure id | Section | Purpose | Type | Must show | Status |
| --- | --- | --- | --- | --- | --- |
| F-forms-orientation | `part1_02_mathematical_toolkit.tex` | Teach wedge-product orientation before forms enter Chern-Simons algebra. | Concept diagram | Oriented area/volume elements; sign flip under basis exchange. | complete: `253b_final_paper/tex_docs/figures/f_forms_orientation.tex` |
| F-transgression-ladder | `part1_03_ordinary_to_chern_simons.tex` | Show how the four-form descends to the Chern-Simons three-form and boundary/anomaly terms. | Dependency diagram | `tr(F wedge F)`, `omega_CS`, exact term, Wess-Zumino term, boundary term. | complete: `253b_final_paper/tex_docs/figures/f_transgression_ladder.tex` |
| F-su2-winding | `part1_03_ordinary_to_chern_simons.tex` | Explain the normalization behind level quantization. | Geometry diagram | `SU(2) ~ S^3`, Euler-angle ranges, normalized volume form, `24 pi^2`. | complete: `253b_final_paper/tex_docs/figures/f_su2_winding.tex` |
| F-flat-moduli | `part1_04_tqft_and_observables.tex` | Visualize flat connections as finite/global phase-space data. | Geometry diagram | Surface cycles, holonomies, conjugation quotient, moduli-space idea. | complete: `253b_final_paper/tex_docs/figures/f_flat_moduli.tex` |
| F-torus-holonomies | `part1_04_tqft_and_observables.tex` | Connect canonical quantization on the torus to finite Hilbert-space dimension. | Geometry/algebra diagram | Alpha/beta cycles, holonomies, `k` basis states, clock and shift operators. | complete: `253b_final_paper/tex_docs/figures/f_torus_holonomies.tex` |
| F-wilson-linking | `part1_04_tqft_and_observables.tex` | Make Wilson-loop linking concrete. | Topology diagram | Two loops, Seifert surface, intersection point, linking number. | blocked: hand-drawn spec `253b_final_paper/llm_docs/current/figure_specs/f_wilson_linking.md` |
| F-framing-ribbon | `part1_04_tqft_and_observables.tex` | Distinguish self-linking/framing from ordinary mutual linking. | Knot/ribbon diagram | Framed knot, push-off curve, twist, self-linking phase. | blocked: hand-drawn spec `253b_final_paper/llm_docs/current/figure_specs/f_framing_ribbon.md` |
| F-response-overview | `part2_05_response_2plus1d.tex` | Orient the 2+1d response section around measurable observables. | Overview schematic | Bulk CS term, edge anomaly, Hall response, braiding, torus degeneracy. | complete: `253b_final_paper/tex_docs/figures/f_response_overview.tex` |
| F-hall-response | `part2_05_response_2plus1d.tex` | Tie the Chern-Simons response equation to a quantum Hall measurement. | Physical schematic | Electric field, transverse current, filling fraction, Hall conductance. | complete: `253b_final_paper/tex_docs/figures/f_hall_response.tex` |
| F-anyon-braid | `part2_05_response_2plus1d.tex` | Distinguish exchange phase from full monodromy. | Worldline diagram | Two quasiparticle worldlines, exchange path, full braid path, phase labels. | blocked: hand-drawn spec `253b_final_paper/llm_docs/current/figure_specs/f_anyon_braid.md` |
| F-inflow-edge | `part2_05_response_2plus1d.tex` | Make bulk-boundary anomaly cancellation spatially intuitive. | Spacetime schematic | Bulk variation, boundary variation, chiral edge mode, cancellation arrow. | blocked: hand-drawn spec `253b_final_paper/llm_docs/current/figure_specs/f_inflow_edge.md` |
| F-kmatrix-observables | `part2_05_response_2plus1d.tex` | Compactly review how K-matrix data feed observables. | Table/flow diagram | `K`, `t`, `ell`, `K^{-1}`, charge, statistics, Hall response, degeneracy. | complete: `253b_final_paper/tex_docs/figures/f_kmatrix_observables.tex` |
| F-theta-observable-chain | `part2_06_sectors_3plus1d.tex` | Show how 3+1d topological sectors become physical constraints or observables. | Flow diagram | Theta term, topological susceptibility, eta prime, nEDM, axion response. | complete: `253b_final_paper/tex_docs/figures/f_theta_observable_chain.tex` |
| F-defect-taxonomy | `part2_07_defects_caveats_outlook.tex` | Separate exact TQFT observables from effective/topological-sector observables. | Taxonomy table | Strict TQFT, topological term in local QFT, defect/global-structure observable, experimental proxy. | complete: `253b_final_paper/tex_docs/figures/f_defect_taxonomy.tex` |

## Figures Inspired by arXiv:2306.00912v2 (Brennan-Hong GGS Review)

These are style-reference figures from the generalized-symmetries review. Their visual approach (showing operator *action* and *deformation*, not just static topology) is better pedagogy for the defect/symmetry material than our current static diagrams.

| Figure id | Source figure | Target chapter | Purpose | Status |
| --- | --- | --- | --- | --- |
| F-sdo-deformation | `TopologicalSDOFig.pdf` | ch08 §8.1 | Show $U_g(\Sigma)$ deforming to $U_g(\Sigma')$ past a charged local operator; demonstrate topological invariance of SDO | new target |
| F-0form-action | `0FormAction.pdf` | ch08 §8.1 | SDO sweeping past a charged operator, enacting the group action — Ward identity made visual | new target |
| F-1form-braiding | `1formBraiding.pdf` | ch08 §8.2 / ch15 §15.1 | 1-form symmetry defect braiding with a Wilson line; visualizes the linking/action of higher-form symmetries on line operators | new target |
| F-bf-thooft-defects | `BFTHooftDefects.pdf` | ch06 §6.3 / ch15 §15.1 | 't Hooft defects in BF theory; shows how magnetic defects produce the linking phase | new target |
| F-axion-string-defect | `AxionStringDef.pdf` | ch14 §14.3 | Axion string as a codimension-2 defect; relevant if axion section is expanded | stretch target |

## Deferred From The Old Wishlist

- `F-worked-map`: no longer useful after the old dense-derivation module was
  folded into the seven-section migration plan.
- `F-cs-roadmap`: overlaps with the paper outline and would likely become a
  decorative roadmap rather than a derivation aid.
- `F-linking-framing-summary`: folded into `F-wilson-linking` and
  `F-framing-ribbon`.
- `F-kmatrix-flow` and `F-kmatrix-table`: folded into
  `F-kmatrix-observables`.
