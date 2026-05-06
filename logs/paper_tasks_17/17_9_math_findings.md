---
created_at: "2026-05-05T20:25:23-04:00"
updated_at: "2026-05-05T20:25:23-04:00"
generated_by: "claude-code"
updated_by: "claude-code"
timestamp_source: hook
---
# Task 17.9 — Math Correctness Proofreading Pass: Findings

**Date:** 2026-05-05  
**Status:** Complete

---

## Summary

10 specific checks performed. **2 issues found and fixed**, all others pass.

---

## Check Results

### 1. Anti-Hermitian Convention Consistency — PASS

- **Ch02** establishes `t^a := -iT^a` at line 417 (eq `eq:anti-herm-def`), Section 2.3.1 (`sec:anti-hermitian-conv`).
- **Ch05** explicitly references ch02's convention table at line 39 with cross-refs to `sec:anti-hermitian-conv`, `def:F-nonabelian`, `eq:anti-herm-trace`.
- **Ch08** uses `F = dA + A ∧ A` consistently (anti-Hermitian). No re-establishment of convention.
- **Ch14** uses `T^a` (Hermitian) for *flavor*-group generators in the chiral Lagrangian (Di Vecchia–Veneziano), not gauge generators. No conflict.
- **Ch15** has no generator-level expressions.

**No fix needed.** Optional clarity note for ch14 line 223 (cosmetic, not mathematical).

### 2. Level Quantization Conventions — PASS (with sign fix, see below)

- **Ch05 CS action** (line 387): `S_CS = (k/4π) ∫ tr(A∧dA + 2/3 A∧A∧A)` — correct.
- **Ch06 BF action** (line 20): `S_BF = (k/2π) ∫ B∧dA` — correct.
- **Ch09 BF action** (line 313): `S_BF = (N/2π) ∫ B∧dA` — matches ch06.

The `k/(4π)` vs `k/(2π)` difference is standard (CS is quadratic in one field, BF is bilinear in two fields). No contradiction.

### 3. H³(Z_N, U(1)) = Z_N — PASS

- **Ch07** line 220–222 (Proposition 7.2.1): States `H³(BZ_N, U(1)) ≅ Z_N`. Correct.
- Proof via connecting homomorphism `H³(BZ_N,U(1)) ≅ H⁴(BZ_N,Z) ≅ Z_N` is sound.

### 4. Modular S-matrix for U(1)_k — PASS

- **Ch10** line 451 (Proposition 10.3.1, eq `eq:s-matrix-u1k`):
  `S_{rs} = (1/√k) exp(2πi rs/k)`, r,s = 0,...,k-1. Correct.

### 5. Hall Conductance — PASS

- **Ch11** line 233–234: `σ_xy = 1/(2πm) = (e²/h)(1/m)`. Correct.
- **Ch05** line 402: `σ_xy = e²/(kh)`. Consistent with ν=1/k.

### 6. Braiding Phases — PASS

| Anyon | Expected | Paper states | Location |
|-------|----------|--------------|----------|
| Toric code ε | θ = −1 | θ_ε = −1 | ch09 line 287, ch10 line 337 |
| Laughlin charge-r | θ_r = exp(iπr²/m) | θ_r = exp(iπr²/k) with k=m | ch10 line 567 |
| Ising σ | θ = exp(iπ/8) | θ_σ = exp(iπ/8) | ch10 line 357 |

All correct.

### 7. Ghost References — PASS

All `\cite[...]` with specific pointers verified:
- `\cite[Ch.~8]{Schwartz2014QFT}` — Ch 8 "Spin 1 and gauge invariance." Correct.
- `\cite[Ch.~30]{Schwartz2014QFT}` — Ch 30 "Anomalies." Correct.
- `\cite[§1.3]{Kock2004Frobenius}` — generators/relations for 2Cob. Correct.
- `\cite[Chs.~1--2]{Kock2004Frobenius}` (×2) — classification theorem. Correct.

No ghost references found.

### 8. Notation Drift (Ch08, Ch14, Ch15 referencing Ch02) — PASS

- Ch05 line 39 has comprehensive convention-recall paragraph citing ch02 equation labels.
- Ch08 uses the convention implicitly (F = dA + A∧A) without re-establishing.
- Ch14, Ch15 do not use gauge-algebra generators.

### 9. BF Level Convention (Ch06 vs Ch09) — FIXED

**Issue found:** Ch06 rigorously derives the BF linking phase as:
```
exp(−2πi qn/N · Lk(C,C'))
```
(minus sign, from the field-shift direction in the path integral).

Ch09 line 334 stated:
```
exp(+2πi/N · Lk(γ,γ'))
```
(plus sign). For N=2 both give −1, but for general N this is a sign error.

**Fix applied:** Changed ch09 eq `eq:bf-linking` to use `−2πi/N`.

**Additional fix:** Renamed duplicate labels in ch09 (`eq:bf-action` → `eq:bf-action-ch9`, `eq:bf-eom` → `eq:bf-eom-ch9`, `eq:bf-gsd` → `eq:bf-gsd-ch9`) and updated all internal `\eqref` references.

### 10. Jones Polynomial / Skein Relation — PASS

- **Ch05** line 1455: `q := exp(2πi/(k+2))` — correctly uses dual Coxeter shift.
- Kauffman bracket skein relation with `A = q^{-1/4}` at line 1458. Correct.
- Partition function `Z_k(S³) = √(2/(k+2)) sin(π/(k+2))` uses shifted level. Correct.
- Modular S-matrix for SU(2)_k uses `sin((a+1)(b+1)π/(k+2))`. Correct.

---

## Fixes Applied

1. **ch09_topological_order.tex line 334:** Sign of BF linking phase corrected from `+` to `−`.
2. **ch09_topological_order.tex lines 313, 321, 345:** Duplicate labels renamed (`eq:bf-action-ch9`, `eq:bf-eom-ch9`, `eq:bf-gsd-ch9`).
3. **ch09_topological_order.tex lines 320, 363, 368:** Internal `\eqref` references updated to match renamed labels.

## Items Flagged (Non-Critical)

- **Bib file** (`tqft_observables_unresolved_refs.bib`): 7 placeholder entries and 5 incomplete entries need resolution before submission. One arXiv number mismatch (`HalperinSternNederRosenow2011` cites arXiv:2102.08998 which is from 2021).
- **Ch14 line 223 (cosmetic):** Could add parenthetical clarifying that `T^a` there are flavor-group generators, not the gauge-algebra `t^a` of ch02.
