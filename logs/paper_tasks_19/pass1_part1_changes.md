---
created_at: "2026-05-06T02:15:07-04:00"
updated_at: "2026-05-06T02:15:07-04:00"
generated_by: "us.anthropic.claude-opus-4-6-v1"
updated_by: "us.anthropic.claude-opus-4-6-v1"
timestamp_source: hook
---
# Structural Editorial Pass — Part I (Chapters 2–8)

## Summary

Five edits across four files. Net effect: ~20 lines of redundant re-derivation removed, one motivational paragraph added, and the BF/DW/toric-code triple-derivation issue resolved with explicit "three routes" cross-references.

---

## Edits

### 1. ch05_chern_simons.tex — Maurer–Cartan re-proof killed

**Location:** §5.4 (former Lemma `lem:MC` proof body)  
**What was there:** Full 12-line re-derivation of the Maurer–Cartan equation (expanding $d(g^{-1}dg)$ from scratch).  
**What replaced it:** 4-line restatement citing Chapter 2's Lemma `lem:maurer-cartan`. Label `lem:MC` preserved for downstream `\ref`.  
**Rationale:** Ch02 already proves this in full. The re-proof served no pedagogical purpose in ch05 — it was invoked mid-derivation, not taught.

---

### 2. ch05_chern_simons.tex — §5.8 TQFT axiom re-statement condensed

**Location:** `\begin{setup}\label{setup:TQFT}` environment (8 lines listing the Atiyah–Segal axioms)  
**What was there:** Full itemized re-statement of what a 3D TQFT assigns — surfaces → vector spaces, closed 3-manifolds → numbers, bordisms → vectors — plus the monoidal/gluing axioms.  
**What replaced it:** One sentence: "Recall that a 3D TQFT is a symmetric monoidal functor $Z:\mathrm{Cob}_3\to\mathrm{Vect}$ satisfying the Atiyah–Segal axioms (Definition~\ref{def:Atiyah-Segal})."  
**Rationale:** Definition `def:Atiyah-Segal` is 12 pages earlier in ch03. The reader does not need it re-stated; they need to see CS *verified against* it. Label `setup:TQFT` removed (confirmed: zero downstream references).

---

### 3. ch04_frobenius.tex — Physical motivation paragraph added

**Location:** Chapter opening, between the two existing intro paragraphs (after "The classification is complete" and before "The reason this works is topological").  
**What was added:** A new paragraph connecting the Frobenius classification to the $N^{2g}$ ground-state degeneracy of BF theory, DW theory, and the toric code — explaining *why* this algebraic chapter matters physically.  
**Rationale:** The critical evaluation flagged ch04 as having no physical motivation. The algebra-only opening gave no reason for a physicist to keep reading.

---

### 4. ch07_dw.tex — "Three routes" cross-reference block

**Location:** After Remark `rem:dw-toric-scope` (end of §7.3), replacing the one-sentence forward pointer.  
**What was there:** "The reader arriving from Chapter 6 will recognize this as untwisted Z_2 BF theory; the lattice Hamiltonian formulation appears in Chapter 9."  
**What replaced it:** A bold-headed "Three routes to the same phase" paragraph with an enumerated list (continuum BF / finite-group DW / lattice Hamiltonian), followed by a sentence explaining what each derivation illuminates (why / what / how).  
**Rationale:** Resolves the triple-derivation problem by *naming it explicitly* at the point where all three routes converge, then explaining the division of labor. Reader no longer wonders why the same result appears three times.

---

### 5. ch06_bf.tex — Forward pointer consolidated

**Location:** End of Remark `rem:bf-gsd-checks` and the final paragraph of the chapter.  
**What was there:** Two overlapping paragraphs (lines 801–810) both mentioning the BF/DW/toric-code connection with partially redundant content.  
**What replaced it:** Merged into one clean paragraph: BF at finite $N$ is a special case of DW; the cocycle twist distinguishes toric code from double semion; the agreement of three derivations is the content of Proposition `prop:toric-dw` in ch07.  
**Rationale:** Eliminated the double-mention and added an explicit forward pointer to the "three routes" resolution in ch07.

---

## Verification

- `\label{setup:TQFT}` removed; `\ref{setup:TQFT}` grep returns 0 hits across all .tex files.
- `\label{lem:MC}` preserved; still targets a valid lemma statement.
- `\ref{def:Atiyah-Segal}` resolves to ch03 line 177.
- `\ref{prop:toric-dw}` resolves to ch07 line 535.
- `\ref{prop:bf-gsd}` resolves to ch06 line 762.
- No new labels introduced; no cross-file references broken.

---

## What was NOT cut

- Ch05 §5.3–§5.7 (CS form derivation, level quantization, Wilson loops, canonical quantization): dense and non-redundant.
- Ch08 generalized symmetries: self-contained by design, light touch per instructions.
- Ch04 algebraic proofs: the full Frobenius classification argument is not duplicated elsewhere.
- Ch06 BF action derivation and mixed linking phase: unique content.
- Ch07 DW path integral and $H^3(BG,U(1))$ classification: unique content.
