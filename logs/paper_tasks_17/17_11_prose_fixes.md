---
created_at: "2026-05-05T22:09:31-04:00"
updated_at: "2026-05-05T22:09:31-04:00"
generated_by: "claude-code"
updated_by: "claude-code"
timestamp_source: hook
---
# Task 17.11 — Prose Pass and AI-Tell Purge: Summary

**Date:** 2026-05-05  
**Status:** Complete

## Banned-phrase grep results

All ten banned phrases were searched (case-insensitive) across all `.tex` files in `tex_docs/`:

| Phrase | Occurrences |
|--------|-------------|
| "we shall see" | 0 |
| "in this chapter we have proved" | 0 |
| "the key statement is" | 0 |
| "an upshot of all this is" | 0 |
| "it can be seen" | 0 |
| "it is easy to see" | 0 |
| "it is easy to verify" | 0 |
| "it can be verified" | 0 |
| "an important observation" | 0 |
| "as we shall see" | 0 |

**Result:** Zero instances of any banned phrase.

## Near-matches assessed

| Location | Phrase | Verdict |
|----------|--------|---------|
| `ch14_sectors_3plus1d.tex:548` | "The upshot is a clean separation..." | **Replaced** with "This gives a clean separation..." |
| `ch13_tqc.tex:456` | "One can verify this directly: two τ's..." | Natural — explicit computation follows. Left in place. |
| `ch02_forms.tex:83` | "we shall exploit throughout" | Standard British mathematical English. Left. |
| `ch02_forms.tex:283` | "We shall rely on..." | Standard mathematical English. Left. |
| `ch05_chern_simons.tex:31` | "as we shall derive below" | Standard forward reference in a long chapter. Left. |
| `ch05_chern_simons.tex:839` | "we shall discuss momentarily" | Standard. Left. |

## Environment check

Grepped for `\begin{upshot}`, `\begin{note}`, `\begin{slogan}`, `\begin{motivation}`:

**Result:** Zero instances found.

## Additional AI-tell sweep

| Pattern | Occurrences | Assessment |
|---------|-------------|------------|
| "it is worth noting" / "it bears mentioning" | 0 | Clean |
| "importantly" / "notably" / "crucially" / "remarkably" | 5 total | All are natural physics prose in context (e.g., "Crucially, the information stored in this degenerate space is..." in ch10). Left in place. |
| "key takeaway" / "key point" / "key idea" / "key result" | 4 total | All are standard physics usage (e.g., "The key point is that the braiding operator is diagonal..."). Left in place. |
| "to summarize" | 2 (both in ch14) | Used to introduce numbered logical chains / summary tables. Standard. Left. |

## Chapter-ending through-line check

Every Part 1 chapter ending already contains a **specific** Part-2 payoff pointer:

| Chapter | Ending payoff pointer |
|---------|----------------------|
| Ch 2 (Forms) | "the linking-number integral of Chapter 5 that predicts the $e^{2\pi i/3}$ anyonic braiding phase measured by Nakamura et al. (Chapter 12)" |
| Ch 3 (Axiomatic) | "The Frobenius algebra $\C[\Z_N]$ that appears there will resurface as the state-counting structure behind the $N$-fold toric-code ground-state degeneracy on the torus (Chapter 9)" |
| Ch 4 (Frobenius) | "the genus formula and the gauge-theory normalization...will reappear as the state-counting structure of the toric code in Chapter 9, where $N^{2g}$ becomes the topological ground-state degeneracy" |
| Ch 5 (CS) | "the Chern--Simons level becomes Hall response, the Wilson-loop phases become anyonic braiding phases, and Proposition 5.X becomes the ground-state degeneracy on the torus" |
| Ch 6 (BF) | "the continuum precursor of the mutual minus sign...Chapter 9 will return to exactly that phase from the lattice-model side" + specific degeneracy formula references |
| Ch 7 (DW) | Itemized list: Ch 8 uses §7.3 for cocycles; Ch 9 uses §7.4 for toric-code TQFT; Ch 10 uses §7.1 for topological sectors; Ch 16 uses Ch 7 as baseline classification |
| Ch 8 (GenSym) | "Chapter 9 constructs the toric code as a lattice model whose topological ground-state degeneracy and mutual braiding phase $(-1)$ are exactly the data predicted by the $\Z_2$ BF theory and anomaly-inflow structure developed in Chapters 6--8" |

All meet the specificity requirement (naming equations, observables, or experiments).

## Edits made

1. `ch14_sectors_3plus1d.tex:548`: "The upshot is" → "This gives"

## Assessment

The paper is essentially clean of AI tells. Earlier tasks (17.12, 17.13) appear to have already removed the structural AI patterns. This pass confirms:
- Zero banned phrases remain
- No `upshot`/`slogan`/`motivation` environments
- All chapter endings have specific Part-2 payoff pointers
- Remaining "shall" / "crucially" / "key point" uses are natural mathematical English
