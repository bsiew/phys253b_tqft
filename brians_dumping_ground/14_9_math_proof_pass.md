# Task 14.9 — Math Correctness Proofreading Pass

- **Status:** pending
- **Owner:** Brian
- **Duration:** 3 hours
- **Stage:** [VI](../stages/stage_VI_integration.md)

## Goal

End-to-end read of the paper with a specific focus on: numerical factors, sign conventions, cohomology-group identities, level-quantization conditions, and ghost references.

## Specific checks

1. **Convention consistency.** Anti-Hermitian $t^a = -iT^a$ stated once in Ch 2 §2.3; verify every subsequent chapter uses this (not Hermitian).
2. **Level quantization conventions.** Ch 5 CS uses $k/(4\pi)$; Ch 6 BF uses $k/(2\pi)$ or $N/(2\pi)$ — confirm the two chapters don't contradict each other.
3. **$H^3(\mathbb{Z}_N, U(1))$.** Verify $\mathbb{Z}_N$ (Task 7.2).
4. **Modular $S$ for $U(1)_k$.** Verify $S_{rs} = k^{-1/2} e^{2\pi i rs/k}$ (Task 10.3).
5. **Hall conductance.** Verify $\sigma_{xy} = e^2/(mh)$ for Laughlin $\nu = 1/m$ (CS ex and Task 11.2).
6. **Braiding phases.** Toric code $\epsilon$: $\theta = -1$. Laughlin: $\theta_r = e^{i\pi r^2/m}$. Ising $\sigma$: $\theta = e^{i\pi/8}$.
7. **Ghost references.** Every `\cite[Theorem/Lemma/Eq X.Y]{...}` with a specific number inside the citation: open the source and verify. Remove or generalize any that can't be confirmed.

## Acceptance criteria

- Every check passes or is flagged for fix.
- Fixes committed and re-verified on re-pass.

## Risks

- **Fatigue.** This is tedious. Mitigation: take 30-min breaks every 90 minutes.
