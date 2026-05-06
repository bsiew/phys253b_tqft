---
created_at: "2026-05-05T19:00:58-04:00"
updated_at: "2026-05-05T19:00:59-04:00"
generated_by: "claude-code"
updated_by: "claude-code"
timestamp_source: hook
---
# Task 17.9 — Math Correctness Proofreading Pass

- **Status:** pending
- **Owner:** Brian
- **Duration:** 3 hours
- **Stage:** [VI](../stages/stage_VI_integration.md)
- **Reference:** [`llm_docs/CRITICAL_EVALUATION_AND_IMPROVEMENT_DIRECTIVES.md`](../../llm_docs/CRITICAL_EVALUATION_AND_IMPROVEMENT_DIRECTIVES.md) — see "Notation Drift" cross-cutting problem

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

## Additional checks from Critical Evaluation (2026-05-05)

8. **Notation drift.** Ch02 establishes anti-Hermitian conventions. Verify ch08, ch14, ch15 all reference ch02's convention table rather than re-establishing their own. After §5.2 deletion, verify ch05 convention-recall paragraph correctly cites ch02 equation numbers.
9. **BF level convention.** Ch06 uses $N/(2\pi)$; ch09 self-contained BF uses the same? Verify after the triple-derivation resolution.
10. **Jones polynomial section (§5.9).** Is the skein relation correctly stated with the $q = e^{2\pi i/(k+2)}$ convention for $SU(2)_k$? Verify against Witten 1989.

## Risks

- **Fatigue.** This is tedious. Mitigation: take 30-min breaks every 90 minutes.
