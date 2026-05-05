# Task 3.1b — Chapter 3 §3.1 Bott, $\pi_3(G)$, and Yang-Mills Vacuum Sectors

- **Status:** pending
- **Owner:** Brian
- **Duration:** 90 min
- **Stage:** [III](../stages/stage_III_partI_B.md)

## Goal

Write the missing conceptual bridge from ordinary Yang-Mills gauge transformations to the topological classification of vacuum sectors by `\pi_3(G)`, using Bott's corollary as the clean mathematical input instead of hand-waving.

## Content

1. **Vacua as pure gauge.** On a spatial slice compactified from `\mathbb{R}^3` to `S^3`, vacuum configurations can be written locally as `A = g^{-1}dg`.
2. **Large gauge transformations.** Explain that gauge transformations are maps `g:S^3\to G`, and homotopy classes of these maps are labeled by `\pi_3(G)`.
3. **Bott input.** State the compact connected simply connected simple case `\pi_3(G)\cong\mathbb{Z}` with Bott 1956 as the primary citation.
4. **Physics meaning.** Vacuum sectors are labeled by an integer winding number `n`; the `\theta`-vacuum is a Fourier superposition across `n`.
5. **Honesty sentence.** Say explicitly that this clean integer classification assumes the standard compact simply connected normalization; refinements appear for semisimple products and more global variants.

## Reuse

- Chapter 2 example from Task `2.6b`.
- The existing narrative comments already embedded in `part1_03_ordinary_to_chern_simons.tex`.
- `tqft_algebraic_topology_review.md` sections on higher homotopy and level quantization.

## Acceptance criteria

- `\pi_3(G)` is motivated geometrically before it is used algebraically.
- Bott is cited where the theorem actually enters.
- The subsection ends with a clear transition to instantons and the `\theta` term.

## References

- Bott 1956.
- Milnor, *Morse Theory*.
- Nakahara.
- `'t Hooft 1976` pseudoparticle paper for the physics side.

## Risks

- **Over-compressing the topology.** The subsection should feel understandable to a physics reader, not like a theorem dump.
