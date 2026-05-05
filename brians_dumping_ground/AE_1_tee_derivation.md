# Task E.1 — Appendix E: Topological Entanglement Entropy Derivation

- **Status:** pending
- **Priority:** important
- **Owner:** Brian
- **Duration:** 2.5 hours
- **Stage:** [VI](../stages/stage_VI_integration.md)

## Goal

Chapter 9 (Task 9.5) states the Kitaev–Preskill / Levin–Wen result $S(A) = \alpha L - \gamma + \cdots$ with $\gamma = \log \mathcal{D}$ and explains its meaning; this appendix derives it.

## Content

1. **Setup.** A gapped 2D system on a disk; partition into a region $A$ and its complement. Entanglement entropy $S(A) = -\tr(\rho_A \log \rho_A)$.
2. **Area law with subleading correction.** On general grounds $S(A) = \alpha L - \gamma + o(1)$, where $L = |\partial A|$ and $\alpha$ is a non-universal coefficient.
3. **Kitaev–Preskill subtraction.** Partition the disk into four regions $A, B, C, D$ with specific geometry; the combination $S_A + S_B + S_C - S_{AB} - S_{BC} - S_{AC} + S_{ABC}$ cancels the area-law terms and extracts $-\gamma$.
4. **Identification of $\gamma = \log \mathcal{D}$.** The total quantum dimension $\mathcal{D} = \sqrt{\sum_a d_a^2}$ where $d_a$ are the quantum dimensions of the anyons.
5. **Worked examples.**
   - Toric code: $\mathcal{D} = 2$, $\gamma = \log 2$.
   - Laughlin $\nu = 1/m$: $\mathcal{D} = \sqrt{m}$, $\gamma = \tfrac{1}{2}\log m$.
   - Ising: $\mathcal{D} = 2$ (with $d_1 = d_\psi = 1$, $d_\sigma = \sqrt{2}$), $\gamma = \log 2$.

## Acceptance criteria

- ~4 pp.
- Kitaev–Preskill derivation outlined with geometry figure (can be hand-drawn).
- $\mathcal{D}$ values for three examples present.
- Cite Kitaev–Preskill 2006 and Levin–Wen 2006 correctly.

## Risks

- **Geometry figure.** The four-region Kitaev–Preskill diagram is small and schematic — easy to redraw.
- **Subtraction formula sign conventions.** Multiple conventions exist; pick Kitaev–Preskill's and stick with it.
