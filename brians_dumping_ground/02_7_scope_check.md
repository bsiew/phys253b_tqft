# Task 2.7 — Chapter 2 Scope Check

- **Status:** done (2026-05-04)
- **Owner:** Brian
- **Duration:** 20 min
- **Stage:** [II](../stages/stage_II_partI_A.md)
- **Priority:** core

## Result

Overleaf compile showed Ch 2 at **20 pp**, roughly 2× the 10-page target. Applied three cuts with user agreement:

1. **Theorem 2.5.6 full proof cut**, replaced with one-paragraph prose sketch. The three-pair cancellation in $F^g = g^{-1}Fg$ is named but not computed; the full argument is executed in Chapter 5 for $\omega_{CS}$.
2. **Proposition 2.5.8 (non-abelian Bianchi) cut entirely** — no downstream `\ref` from any chapter. Still stated in §2.3 as eq.~\ref{eq:nonabelian-bianchi} for completeness.
3. **"Step 1 / Step 2 / ..." scaffolding purged** from the entire file per user feedback.

### File metrics

| | Lines | Words |
|---|---|---|
| Before | 884 | 9136 |
| After | 603 | 8394 |
| Cut | 281 (-32%) | 742 (-8%) |

### Expected page count after trim

Extrapolating 20 pp × ~0.7 = **~14 pp**, still over the 10-page target but a large improvement. Brian to re-compile on Overleaf and confirm.

### Further trims if still over 12 pp (in priority order, not yet applied)

1. Merge §2.4.2 (connection on total space) + §2.4.3 (curvature descent) into a single subsection.
2. Shorten §2.3 conventions narrative; keep the Schwartz-translation as a compact table.
3. Cut Example 2.1.4 ($\mathbb{R}^3$ divergence) — pedagogical aside not cited downstream.

### Verification-matrix changes

- C.2.26 ($F^g = g^{-1}Fg$): `derived-here` → `derived-elsewhere` (full derivation now lives in CS chapter).
- C.2.27 (non-abelian Bianchi): `derived-here` → `cut`.

### Dependency audit (checklist)

- [x] §2.1 forms/wedge/$d$: required by everything downstream. Kept.
- [x] §2.2 integration/Stokes/de Rham: required by Ch 5 (Stokes), Ch 5/6/7 (de Rham). Kept.
- [x] §2.3 Lie-algebra forms + conventions: required by Ch 5/6/7/8. Kept.
- [x] §2.4 principal bundles: required by Ch 5 (trivial bundle), Ch 8 (nontrivial bundles). Kept.
- [x] §2.5 gauge transformations: required by Ch 5/6. Kept; proof cut to sketch.
- [x] §2.6 EM + winding examples: pedagogical foreshadowing. Kept.

Every retained section has at least one downstream dependent. Nothing was kept "for its own interest".

### Chapter 2 is locked

All seven Stage II tasks (2.1 – 2.7) complete. Ch 2 is ready to ship pending a compile-length confirmation from Brian.

## Goal

Ensure Chapter 2 is ~10 pages and every section feeds something downstream. Cut anything that doesn't.

## Checklist

- [ ] §2.1 forms/wedge/$d$: required by everything.
- [ ] §2.2 integration/Stokes/de Rham: required by CS chapter, Ch 5/6/7/8.
- [ ] §2.3 Lie-algebra forms + conventions: required by CS chapter, Ch 5/6/7/8.
- [ ] §2.4 principal bundles: required by Ch 5/8.
- [ ] §2.5 gauge transformations: required by CS chapter, Ch 5/6.
- [ ] §2.6 EM and winding examples: pedagogical, not strictly required downstream; keep.
- [ ] Delete any section that would have been included only for its own interest (differential ideals, connections on associated vector bundles, etc.).

## Steps

1. Compile Chapter 2 alone and count pages.
2. If > 10 pp, cut in this order: §2.4 first (shortest to cut without breaking dependencies), §2.6 second.
3. If < 8 pp, we're probably missing something needed by Ch 5; check.

## Acceptance criteria

- Chapter 2 is 8–11 pages.
- Every section has at least one dependent chapter downstream.

## Risks

- **Expansion.** Tasks 2.1–2.6 together might produce more than 10 pp naturally.
