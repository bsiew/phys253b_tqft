# Task 7.1 — Chapter 7 §7.1 Dijkgraaf–Witten Action and Path Integral

- **Status:** done
- **Owner:** Brian
- **Duration:** 90 min
- **Stage:** [III](../stages/stage_III_partI_B.md)

## Goal

Define Dijkgraaf–Witten (DW) theory: a finite-group gauge theory with a topological twist given by a group cohomology class. Compute the path integral as a weighted sum over homotopy classes of maps $\phi: M \to BG$ (equivalently, over flat $G$-bundles).

## Content outline

1. **Classical fields.** A gauge field is a principal $G$-bundle, equivalently a classifying map $M\to BG$, and for connected $M$ equivalently a homomorphism $\pi_1(M)\to G$ up to conjugation.
2. **Action.** Given a cohomology class $\alpha \in H^d(BG, U(1))$, the action on a map $\phi: M \to BG$ is $S[\phi] = \langle \alpha, \phi_*[M]\rangle$ where $[M]$ is the fundamental class and $\phi_*$ pushes forward to $H_d(BG)$. Pair via the canonical pairing $H^d \otimes H_d \to U(1)$.
3. **Partition function.**
   $$Z_\alpha(M)=\sum_{[\phi]:M\to BG}\frac{1}{|\Aut(\phi)|}\,\exp(iS_\alpha[\phi])$$
   and, for connected $M$,
   $$Z_\alpha(M)=\sum_{[\rho]\in \mathrm{Hom}(\pi_1(M),G)/G}\frac{1}{|C_G(\rho)|}\,\exp(iS_\alpha[\rho])
   =\frac{1}{|G|}\sum_{\rho\in \mathrm{Hom}(\pi_1(M),G)}\exp(iS_\alpha[\rho]).$$
4. **Gauge invariance.** The automorphism-factor weighting is the finite-group analogue of dividing by gauge-group volume.

## Verification

Work out the untwisted case ($\alpha = 0$): $Z_0(M) = |G|^{-1} |\mathrm{Hom}(\pi_1(M), G)|$ for connected $M$.

## Acceptance criteria

- Action defined explicitly.
- Partition function written.
- Untwisted-case formula verified.
- ~2–3 pages.

## References

- Dijkgraaf–Witten 1990 (primary).
- Freed 1995 classical CS notes for the modern exposition.
