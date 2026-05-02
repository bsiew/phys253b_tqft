# Writing Review

## Current Pack

pedagogical_rewrite

## Target

`PROJECTS/QFT/writings/chern_simons_review.tex`

Final-paper modular output directory: `PROJECTS/QFT/253b_final_paper/tex_docs`

Session-generated review docs directory: `PROJECTS/QFT/253b_final_paper/llm_docs`

## Research Workflow Trace

- Stage review: `state/stage_review.md`
- Automated run: `20260429T003350-072ef494`
- Automated run status: completed, but the retrieved findings were unrelated EFTofLSS vault notes. Treat it as a runtime trace, not as Chern-Simons evidence.
- Corrected literature pass: `state/writing/chern_simons_literature_expansion_2026-04-29.md`

## Verified

- The review has a clear dependency order: Schwartz total derivative, Chern-Simons three-form, action, quantization, canonical phase space, Wilson loops, and quantum Hall applications.
- The abelian torus quantization and linking-number sections are good candidates to preserve as the pedagogical spine of the draft.
- The existing bibliography already contains the right first-pass sources: Chern-Simons, Witten, Moore, Tong, Callan-Harvey, Deser-Jackiw-Templeton, ZHK, Arovas-Schrieffer-Wilczek, Wen-Niu, Wen-Zee, and EMS&S.
- The Brian review supplies the preferred mathematical style for this final-paper pass: definitions before use, explicit calculations for sign-sensitive claims, and short physical interpretation after derivations.
- Modular TeX outputs now exist for differential-form foundations, synthesis of both reviews, and anomaly/response physics.
- A source-expansion pass added `dense_derivation_expansion.tex` to restore component/form translations, Chern-Simons variation, gauge-transformation algebra, Euler-angle level normalization, torus quantization, theta functions, Wilson-loop Gaussian integration, framing, K-matrix integrate-out, edge-mode structure, and Maxwell-Chern-Simons mass derivation.
- A pedagogical rewrite pass corrected over-explanatory headings into short topic labels and added explanatory prose around the most equation-heavy derivations.
- High-value figure opportunities are now flagged in TeX with `FIGURE FLAG` comments and mirrored into `state/writing/figure_inventory.md` plus `253b_final_paper/llm_docs/figure_wishlist.md`.

## Incorrect Or Unsupported

- No specific mathematical claim is marked incorrect in this pass.
- The automated research report at `artifacts/research_reports/20260429T003350-072ef494.md` is not source-support for this draft because its findings are off-topic.

## Ambiguous Or Convention-Dependent

- Trace normalization for level quantization should be stated before relying on `k in Z`.
- Orientation conventions affect signs in the torus commutator, Wilson-loop phase, and Hall current.
- Framing dependence should be treated as part of the quantum observable, not merely as a nuisance.
- Boundary conditions are required before using the bulk variational principle on a manifold with boundary.

## Missing Assumptions

- Compactness and connectedness assumptions on the gauge group in the level-quantization argument.
- Whether the review is treating ordinary bosonic Chern-Simons theory only, or also gesturing toward spin Chern-Simons refinements.
- Whether the quantum Hall section intentionally omits Wen-Zee geometric response/shift data.

## Notation Inconsistencies

- `k` is used as Chern-Simons level; `m` is used for Laughlin filling denominator and also appears in the Maxwell-Chern-Simons mass formula context. Keep local explanations explicit.
- `K` appears as the Chern-Simons current in the Schwartz bridge and later as the K-matrix. Avoid placing those usages too close without a reminder.
- `q`, `l`, and `t` in the Wilson-loop/K-matrix sections need local definitions at first use.

## Required Revisions

1. Run notation/cross-reference and convention audits across all four TeX modules.
2. Ask for an adversarial sign/normalization review of `dense_derivation_expansion.tex`, especially the gauge transformation, Wilson-loop Gaussian, and K-matrix integrate-out.
3. Turn the strongest figure candidates into formal figure specs before generating visuals.
4. Convert final source notes into prose citations once the bibliography strategy for the partner-compiled paper is fixed.

## Modular TeX Outputs

- `PROJECTS/QFT/253b_final_paper/tex_docs/differential_forms_csimons_foundations.tex`
- `PROJECTS/QFT/253b_final_paper/tex_docs/dense_derivation_expansion.tex`
- `PROJECTS/QFT/253b_final_paper/tex_docs/chern_simons_two_review_synthesis.tex`
- `PROJECTS/QFT/253b_final_paper/tex_docs/anomalies_boundaries_topological_response.tex`

## Compile Status

- Current artifact build: `PROJECTS/QFT/artifacts/253b_final_paper_compile/tex_docs_compile_wrapper.pdf`
- Latest compile: successful after pedagogical rewrite.
- Build outputs are intentionally outside the nested `253b_final_paper` git repository.
- PDF length: 24 pages.
- Remaining compile issue: none observed on the second `pdflatex` pass.

## Claude/Codex Split

- Use Codex for repo-aware integration, large-context synthesis across source files, and writing modular TeX into the project structure.
- Use Claude for dense derivation expansion, adversarial convention checks, and making the prose more mathematically useful without losing readability.
- Best handoff format: give Claude one module at a time plus the style guide in `253b_final_paper/llm_docs/writing_style_guide.md`, then bring the result back through Codex for consistency, file placement, and notation audit.
