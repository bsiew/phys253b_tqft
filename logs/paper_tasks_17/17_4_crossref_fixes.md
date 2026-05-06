---
created_at: "2026-05-05T20:42:08-04:00"
updated_at: "2026-05-05T20:42:08-04:00"
generated_by: "claude-code"
updated_by: "claude-code"
timestamp_source: hook
---
# Task 17.4 — Cross-Reference Fixes

**Date:** 2026-05-05  
**Status:** Complete  
**Result:** 0 undefined `\ref{}` or `\eqref{}` references remain.

---

## Summary

Grepped all `.tex` files in `253b_final_paper/tex_docs/` for `\label{}`, `\ref{}`, and `\eqref{}`. Found **903 unique labels**, **195 unique `\ref{}`**, and additional `\eqref{}` uses. Identified **23 undefined references** (20 `\ref` + 3 `\eqref`) and 1 duplicate label (benign — in a comment).

---

## Fixes Applied

### Category 1: `ch:` prefix should be `sec:` (7 refs, 8 files)

The introduction and other chapters used `\ref{ch:X}` for chapters that use `\label{sec:X}` (the `\chapter` command doesn't automatically set the prefix).

| Undefined ref | Correct label | Files fixed |
|---|---|---|
| `ch:toporder` | `sec:topological-order` | ch01, ch05, ch06, ch07 |
| `ch:anyons` | `sec:anyons` | ch01, ch02, ch07 |
| `ch:tqc` | `sec:tqc` | ch01, ch05 |
| `ch:fqhe` | `sec:fqhe` | ch01 |
| `ch:outlook` | `sec:outlook` | ch01, ch07 |
| `ch:sectors-3plus1d` | `sec:sectors-3plus1d` | ch01 |
| `ch:defects-synthesis` | `sec:defects-synthesis` | ch01 |

### Category 2: Typos / wrong label name (6 refs)

| Undefined ref | Correct label | File |
|---|---|---|
| `sec:atiyah-axioms` | `sec:atiyah-segal-axioms` | ch11_fqhe.tex |
| `thm:stokes` | `thm:ch2-stokes` | ch05_chern_simons.tex |
| `sec:tqft-observables` | `sec:observables` | ch11_fqhe.tex |
| `eq:leibniz` | `eq:ch2-leibniz` | ch05_chern_simons.tex |
| `eq:gauge-A` | `eq:gauge-A-2` | ch05_chern_simons.tex |
| `eq:dginv` | `eq:dginv-lemma` | ch05_chern_simons.tex |

### Category 3: Subsection label mismatch (3 refs)

| Undefined ref | Resolution | File |
|---|---|---|
| `subsec:hilbert-surfaces-gsd` | → `subsec:U1-torus` (CS quantization on torus) | ch11_fqhe.tex |
| `subsec:cs-effective-action` | → `subsec:laughlin-to-cs` (Laughlin effective CS action) | ch16_outlook.tex |
| `subsec:photonic-braiding` | → `sec:experiments` (no photonic subsection exists; rewrote to point at experiments chapter) | ch13_tqc.tex |

### Category 4: Planned appendices — stubs created (7 refs)

These references point to appendices that are discussed in the text as deferred material but had no `.tex` file yet.

| Undefined refs | Stub file created |
|---|---|
| `app:frobenius`, `appsec:frob-to-tqft`, `appsec:mapping-class`, `appsec:handle-spectrum` | `app_frobenius.tex` |
| `app:bf-zn`, `sec:appD-bf-lattice`, `sec:appD-bar-resolution` | `app_bf_zn.tex` |

Both stubs are included in the wrapper (`tex_docs_ch02_ch13_app_e_wrapper_20260505.tex`) under `\appendix`.

---

## Duplicate Labels

| Label | Occurrences | Status |
|---|---|---|
| `sec:bf-self-contained` | Line 40 (in `%` comment), Line 302 (active) of `ch09_topological_order.tex` | Benign — only one active definition. |

---

## Verification

```
$ grep -oh '\ref{...}\|\eqref{...}' *.tex | ... | comm -23 - labels
(empty — zero undefined references)
```
