---
created_at: "2026-05-05T19:01:28-04:00"
updated_at: "2026-05-05T22:02:16-04:00"
generated_by: "claude-code"
updated_by: "claude-code"
timestamp_source: hook
---
# Task 17.10 — Physics / Citation Proofreading Pass

- **Status:** pending
- **Owner:** Helena
- **Duration:** 2.5 hours (expanded scope)
- **Stage:** [VI](../stages/stage_VI_integration.md)
- **Reference:** [`llm_docs/CRITICAL_EVALUATION_AND_IMPROVEMENT_DIRECTIVES.md`](../../llm_docs/CRITICAL_EVALUATION_AND_IMPROVEMENT_DIRECTIVES.md) — see Ch 12 and Ch 13 evaluations

## Goal

End-to-end read with a focus on: experimental numbers, physical plausibility, and citation attribution.

## Specific checks

1. **Experimental values.** $\sigma_{xy}$ values, filling fractions, measured braiding phases — all match published experimental papers.
2. **Citation attribution.** Every experimental claim cites the primary source (not a review). Primary = Nakamura 2020, Werkmeister 2025, Andersen 2023, plus any 2025 follow-up papers actually mentioned.
3. **Historical claims.** Kitaev 2003 originated fault-tolerant anyonic QC — check. Callan–Harvey 1985 originated the inflow mechanism — check.
4. **Caveats tone.** Chapters 11, 12, 13 caveats sections read as matter-of-fact, not hedging or polemical.

## Additional checks from Critical Evaluation (2026-05-05)

5. **Ch 12 epistemic hierarchy.** After restructuring (if done), verify the new ordering (direct braiding → indirect correlations → synthetic emulation) is reflected in section order and prose framing.
6. **Andersen 2023 caveat sharpness.** Must say explicitly: "not an observation of non-abelian anyons in condensed matter; a programmatic verification on an engineered system." No hedging.
7. **Ch 12 synthesis paragraph.** Verify closing section states: (a) fractional charge settled, (b) abelian braiding at ν=1/3 directly observed, (c) non-abelian braiding in natural system unobserved.
8. **Ch 13 §13.4 honesty.** Must state: no natural non-abelian platform confirmed as of 2024-2025; ν=5/2 remains debated.
9. **Ch 11 §11.7 tunneling exponents.** If written: verify the Luttinger-liquid prediction $I \propto V^{2/\nu - 1}$ and the measured discrepancy are correctly attributed to edge reconstruction.

## Acceptance criteria

- All experimental numbers cross-verified with primary sources.
- Citation accuracy confirmed.
- Caveats sections read correctly.
- Epistemic-status framing in ch12 and ch13 is sharp, not hedging.
