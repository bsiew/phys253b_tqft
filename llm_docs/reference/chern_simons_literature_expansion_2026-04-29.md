# Chern-Simons Literature Expansion Pass - 2026-04-29

## Stage, Bottleneck, Evidence, Next Actions

- Current stage: `conceptual_and_formal_modeling`.
- Current bottleneck: explicit assumptions, formal targets, and writing/synthesis priorities.
- Evidence: `state/stage_review.md` keeps QFT in `conceptual_and_formal_modeling`; `writings/chern_simons_review.tex` is now the canonical writing artifact; the automated run `20260429T003350-072ef494` completed but retrieved unrelated EFTofLSS vault notes, so its source findings should be treated as an operational trace rather than substantive Chern-Simons evidence.
- Next actions: expand the review through the source backbone below, then run citation integration, technical verification, notation/cross-reference audit, and style review in that order.

## Corrected Source Backbone

Core Chern-Simons and TQFT:

- Chern and Simons, "Characteristic Forms and Geometric Invariants" (1974). Use for transgression forms and the identity behind `d CS_3 = Tr(F wedge F)`. Existing review citation: `ChernSimons1974`.
- Witten, "Quantum Field Theory and the Jones Polynomial" (1989), DOI: <https://doi.org/10.1007/BF01217730>. Use for the action, path integral, stationary points as flat connections, Wilson loops, Jones polynomial, and framing.
- Freed, "Classical Chern-Simons Theory, Part 1", arXiv: <https://arxiv.org/abs/hep-th/9206021>. Use for the geometric meaning of the classical action, line bundles, and global normalization issues.
- Elitzur, Moore, Schwimmer, and Seiberg, "Remarks on the Canonical Quantization of the Chern-Simons-Witten Theory" (1989), DOI: <https://doi.org/10.1016/0550-3213(89)90436-7>. Use for canonical quantization, conformal blocks, and boundary/WZW structure.
- Moore, "Introduction to Chern-Simons Theories", Rutgers TASI notes: <https://www.physics.rutgers.edu/~gmoore/TASI-ChernSimons-StudentNotes.pdf>. Use as the main pedagogical bridge for descent, canonical quantization, Wilson loops, and framing.

Anomaly, boundary, and massive gauge-field context:

- Callan and Harvey, "Anomalies and Fermion Zero Modes on Strings and Domain Walls" (1985), DOI: <https://doi.org/10.1016/0550-3213(85)90489-4>. Use for anomaly inflow framing.
- Deser, Jackiw, and Templeton, "Topologically Massive Gauge Theories" (1982), DOI: <https://doi.org/10.1016/0003-4916(82)90164-6>. Use only for the Maxwell-Chern-Simons contrast.

Quantum Hall and abelian topological order:

- Zhang, Hansson, and Kivelson, "Effective-Field-Theory Model for the Fractional Quantum Hall Effect" (1989), DOI: <https://doi.org/10.1103/PhysRevLett.62.82>. Use for Chern-Simons effective theory of Laughlin states.
- Arovas, Schrieffer, and Wilczek, "Fractional Statistics and the Quantum Hall Effect" (1984), DOI: <https://doi.org/10.1103/PhysRevLett.53.722>. Use for fractional statistics and quasihole braiding.
- Wen and Niu, "Ground-State Degeneracy of the Fractional Quantum Hall States..." (1990), DOI: <https://doi.org/10.1103/PhysRevB.41.9377>. Use for topology-dependent degeneracy.
- Wen and Zee, "Classification of Abelian Quantum Hall States and Matrix Formulation of Topological Fluids" (1992), DOI: <https://doi.org/10.1103/PhysRevB.46.2290>. Use for the K-matrix framework.
- Tong, "Lectures on the Quantum Hall Effect", chapter 5 PDF: <https://www.damtp.cam.ac.uk/user/tong/qhe/five.pdf>. Use as the pedagogical calculation source for Hall response, charge/statistics, and torus degeneracy.

## Expansion Targets

1. Level quantization and global normalization.
   Evidence: the review gives the pure-gauge winding argument in lines 255-307, but it does not yet separate trace normalization, compactness of `G`, spin/non-spin refinements, and non-simply-connected subtleties.
   Next action: add a short "What the quantization argument assumes" paragraph after the level-quantization subsection. Keep the main result pedagogical, but mark the global refinements as beyond-scope rather than absent.

2. Framing as a structural feature, not only a warning.
   Evidence: lines 589-598 introduce self-linking and the abelian framing shift; Witten and Moore support a broader explanation that the quantum theory naturally gives framed link/manifold invariants.
   Next action: expand the framing subsection by two paragraphs: one on regularization of coincident Wilson loops, and one on topological spin/modular `T` as the physical way the dependence reappears.

3. Boundary CFT and WZW edge modes.
   Evidence: lines 309-320 and 749-751 correctly identify anomaly inflow, but the draft only states that boundary modes must appear. EMS&S is the natural source for the Chern-Simons/WZW quantization story.
   Next action: add a new subsection after "Anomaly inflow and boundary modes" that gives the abelian chiral-boson edge as the simplest case and names the nonabelian WZW model as the corresponding boundary theory.

4. Canonical quantization beyond the abelian torus example.
   Evidence: lines 322-436 give a strong `U(1)_k` torus calculation; the nonabelian/geometric-quantization story is only gestured at.
   Next action: add a "What changes for nonabelian `G`" bridge: phase space is the moduli space of flat `G`-connections; quantization gives a finite-dimensional space related to conformal blocks; details are deferred.

5. K-matrix scope and response conventions.
   Evidence: lines 720-745 introduce the K-matrix result compactly. Wen-Zee supports this as a classification framework, while Tong supports the pedagogical formulas.
   Next action: add one paragraph specifying which data are universal topological data (`K`, charge vector `t`, quasiparticle vector `l`) and which geometric responses, such as shift/spin vector, are intentionally omitted from this review.

6. Citation integration.
   Evidence: the draft uses `\eqsrc` after most displayed equations, which is excellent for traceability but heavy for final prose.
   Next action: keep source notes for imported identities, convention-sensitive formulas, historical claims, and delicate normalizations; move routine source support into prose citations.

## Style Revision Queue

- Preserve the linear pedagogical tone. The review is already strongest when it says what an equation is for immediately after displaying it.
- Reduce repeated transitions beginning with "This is..." where the sentence only re-labels the previous equation.
- Keep concrete mathematical headings. Do not replace them with motivational headings.
- Do not polish away warning language around orientation, framing, boundary terms, or normalization.
- In the final pass, compress the annotated reading list so it points to the expansion path rather than repeating claims already made in the body.

## Technical Verification Gates

- Check the nonabelian variation sign and boundary term against the declared convention for `A mapsto g^{-1}Ag + g^{-1}dg`.
- Check the pure-gauge shift of the action against the trace normalization used for `SU(N)` fundamental representation.
- Check all factors of 2 in the abelian Wilson-loop Gaussian computation, especially the off-diagonal double counting in the linking matrix.
- Check the Hall-current sign convention against the orientation convention for `epsilon^{ij}` and the sign of the background magnetic field.
- Check whether every occurrence of `k`, `m`, `K`, `q`, `l`, and `t` has a unique local meaning.
