---
created_at: "2026-05-05T21:58:45-04:00"
updated_at: "2026-05-05T21:58:45-04:00"
generated_by: "claude-code"
updated_by: "claude-code"
timestamp_source: hook
---
# Task 17.8 — Core Deliverables Audit Report

**Date:** 2026-05-05  
**Auditor:** Claude (automated)  
**Paper:** TQFT Review (253b final paper)  
**Source directory:** `253b_final_paper/tex_docs/`

---

## Summary

| # | Item | Verdict |
|---|------|---------|
| 1 | Ch 3 §3.3 gluing example (two disks → sphere) | **PASS** |
| 2 | Ch 3 pair-of-pants figure | **PARTIAL** |
| 3 | Ch 4 pair-of-pants figure (Frobenius) | **PARTIAL** |
| 4 | Ch 5 forms rehash removed | **PASS** |
| 5 | Ch 5 FQH tie-in (`ex:U1-action`) | **PASS** |
| 6 | Ch 5 Wilson-loop linking (`ex:abelian-wilson`) | **PASS** |
| 7 | Ch 8 §8.2 dictionary table | **PASS** |
| 8 | Ch 8 §8.6 HEP anomaly inflow example | **PASS** |
| 9 | Ch 8 §8.7 CM anomaly inflow example | **FAIL** |
| 10 | Ch 10 §10.5 anyon comparison table | **PASS** |
| 11 | Ch 11 §11.5 honesty box | **PARTIAL** |
| 12 | Ch 11 §11.6 Maxwell-Chern-Simons | **PASS** |
| 13 | Ch 11 §11.7 FQHE honesty box (universal vs non-universal) | **PARTIAL** |
| 14 | Ch 12 experimental honesty / synthetic-vs-natural | **PASS** |
| 15 | Ch 13 §13.3 honesty box on fault tolerance | **PASS** |
| 16 | Ch 14 §14.2 Witten-Veneziano | **PASS** |
| 17 | Ch 14 §14.3 Strong CP / axion | **PASS** |
| 18 | Ch 14 §14.4 3+1D iffiness | **PASS** |
| 19 | Ch 15 §15.2 Four-category observable taxonomy | **PASS (marginal)** |
| 20 | Ch 16 Outlook | **PASS** |
| 21 | Ch 01 Introduction | **PASS** |
| 22 | BF/toric-code triple-derivation resolved | **PARTIAL** |

**Totals:** 15 PASS, 1 PASS (marginal), 4 PARTIAL, 1 FAIL, 1 N/A (item 4 is a removal confirmation)

---

## Detailed Findings

### 1. Ch 3 §3.3: Concrete Gluing Example — PASS

**Location:** `ch03_axiomatic.tex`, lines 353–471  
**Content:** Section titled "A worked gluing example: two disks make a sphere" with label `sec:two-disks-sphere`. Contains subsections on geometry of decomposition (defining disk as cobordism, reversed disk, gluing identity $D^2_{\text{bar}} \circ D^2 = S^2$) and the Atiyah-Segal computation (Proposition 3.11). Complete and pedagogically effective.

---

### 2. Ch 3 Pair-of-Pants Figure — PARTIAL

**Location:** `ch03_axiomatic.tex`, lines 101–118 (figure environment)  
**Issue:** The figure uses `\IfFileExists{figures/cobordism_generators.pdf}` which falls back to a text placeholder. The TikZ source `figures/f_pair_of_pants.tex` exists and is complete but is **never `\input`-ed** by the chapter. The compiled document shows only the text-box placeholder.

**Fix needed:** Wire `figures/f_pair_of_pants.tex` into the chapter (either as a direct `\input` or compile it to PDF and commit as `cobordism_generators.pdf`).

---

### 3. Ch 4 Pair-of-Pants Figure (Frobenius) — PARTIAL

**Location:** `ch04_frobenius.tex`, lines 43–63 (figure environment)  
**Issue:** Same pattern as Ch 3 — the `\IfFileExists` conditional fails because the PDF doesn't exist. The fallback is a placeholder box. The TikZ file `figures/f_cobordism_generators.tex` draws identity/cup/cap/twist but NOT the pair-of-pants. The pair-of-pants TikZ (`f_pair_of_pants.tex`) is not referenced by ch04.

**Fix needed:** Either add pair-of-pants to `f_cobordism_generators.tex` and compile, or wire `f_pair_of_pants.tex` into ch04's figure.

---

### 4. Ch 5 Forms Rehash Removed — PASS

**Location:** `ch05_chern_simons.tex`, lines 37–39 (Section 5.2)  
**Content:** Section 5.2 is now a single ~5-line paragraph of convention recall with back-references to Chapter 2. The old lengthy forms review (visible in `source_tex/chern_simons_theory.tex` lines 119–366) has been fully excised.

---

### 5. Ch 5 FQH Tie-in — PASS

**Location:** `ch05_chern_simons.tex`, line 397 (`\label{ex:U1-action}`)  
**Content:** Abelian $U(1)_k$ action example with explicit forward-reference to Laughlin state and Hall conductance.

---

### 6. Ch 5 Wilson-loop Linking — PASS

**Location:** `ch05_chern_simons.tex`, lines 855–963 (`\label{ex:abelian-wilson}`)  
**Content:** Full derivation of abelian Wilson-loop correlator, linking number, and connection to anyonic statistics.

---

### 7. Ch 8 §8.2 Dictionary Table — PASS

**Location:** `ch08_gensym.tex`, lines 260–274  
**Content:** `tabular` environment within a `table` float (`\label{tab:qform-dictionary}`) mapping charged objects (local operator, Wilson line, surface operator) to symmetry defect codimension, conserved current form degree, and background field.

---

### 8. Ch 8 §8.6 HEP Anomaly Inflow — PASS

**Location:** `ch08_gensym.tex`, lines 718–881 (`\label{sec:hep-inflow}`)  
**Content:** Full treatment of chiral anomaly as 5D inflow (Callan-Harvey mechanism). Includes the anomaly equation, bulk CS action, gauge-variation cancellation proof.

---

### 9. Ch 8 §8.7 CM Anomaly Inflow — FAIL

**Location:** MISSING  
**Evidence:** Chapter ends at line 886 after §8.6. Multiple forward pointers promise §8.7 (lines 609, 715, 880–881) but the section is never written. Line 880: "Section 8.7 will now present the condensed-matter analogue, where a boundary chiral boson anomaly is cancelled by the bulk Chern-Simons response of the fractional quantum Hall fluid."

**CRITICAL:** This is the Part 1 → Part 2 bridge. The figure file `figures/f_anomaly_inflow.tex` (depicting 3D bulk with CS action + 2D boundary with chiral edge mode) exists but is unreferenced.

**Fix needed:** Write §8.7 (FQH edge anomaly cancelled by bulk CS inflow). Incorporate `f_anomaly_inflow.tex`. Target: 2–3 pages.

---

### 10. Ch 10 §10.5 Anyon Comparison Table — PASS

**Location:** `ch10_anyons.tex`, lines 727–845  
**Content:** Subsection "Anyon Comparison Table" with `tabular` comparing toric code ($\mathbb{Z}_2$), Laughlin $\nu=1/m$ ($\mathbb{Z}_m$), and Ising (non-abelian) models. Columns: system, labels, fusion rules, topological spin, statistics. Followed by commentary.

---

### 11. Ch 11 §11.5 Honesty Box — PARTIAL

**Location:** The honesty box is at `ch11_fqhe.tex` lines 508–533, but in **§11.7** not §11.5.  
**Issue:** Section 11.5 covers $K$-matrix theory and contains no honesty box. The honesty content exists but is located in §11.7 ("When the Observables Are Clean, and When They Are Only Effective"). This is consistent with the file's internal numbering plan (line 24) but conflicts with the task spec which names §11.5.

**Verdict:** Content present, section numbering mismatch. If the task spec should say §11.7, this is PASS.

---

### 12. Ch 11 §11.6 Maxwell-Chern-Simons — PASS

**Location:** `ch11_fqhe.tex`, lines 431–503 (`\label{subsec:maxwell-cs}`)  
**Content:** MCS action, Hodge star / metric dependence argument, topologically massive propagator, comparison table (Pure CS vs MCS), two-regime crossover, physical applications. ~3–4 pages. "CS term ≠ TQFT" argument is explicit.

---

### 13. Ch 11 §11.7 FQHE Honesty Box (Universal vs Non-Universal) — PARTIAL

**Location:** `ch11_fqhe.tex`, lines 508–533  
**Issue:** The section discusses platform status and measurement confirmation but does NOT address universal vs non-universal edge properties (edge velocity, reconstruction, tunneling exponent dependence on microscopic details). Also, at ~25 lines (~1 page), it falls short of the 2–3 page target.

**Fix needed:** Expand §11.7 to include explicit discussion of which edge observables are topologically protected (universal: Hall conductance, thermal Hall, quasiparticle charge) vs. which depend on non-universal microscopic details (edge velocity, tunneling exponents, edge reconstruction). Add ~1–2 pages.

---

### 14. Ch 12 Synthetic-vs-Natural Framing — PASS

**Location:** `ch12_experiments.tex`, lines 253–361  
**Content:** Multiple clearly-marked discussions: honesty box at lines 257–263 ("emulation versus discovery"), detailed "what this is and what it is not" paragraph (321–331), synthesis section (353–361) with epistemic hierarchy separating natural observations from engineered demonstrations.

---

### 15. Ch 13 §13.3 Honesty Box on Fault Tolerance — PASS

**Location:** `ch13_tqc.tex`, lines 359–412 (`\label{subsec:tqc-honesty-box}`)  
**Content:** Four-point assessment: (1) no confirmed natural non-abelian platform, (2) Majorana proposals have not delivered, (3) synthetic realizations lack passive protection, (4) fault-tolerance thresholds remain demanding.

---

### 16. Ch 14 §14.2 Witten-Veneziano — PASS

**Location:** `ch14_sectors_3plus1d.tex`, lines 199–364 (`\label{subsec:eta-prime-wv}`)  
**Content:** 7 subsubsections: flavor-singlet mass problem, effective Lagrangian, WV formula (boxed Proposition), large-N derivation, numerical evaluation, lattice verification, holographic crosscheck. ~5–6 pages.

---

### 17. Ch 14 §14.3 Strong CP / Axion — PASS

**Location:** `ch14_sectors_3plus1d.tex`, lines 366–498 (`\label{subsec:strong-cp-axion}`)  
**Content:** 7 subsubsections: $\bar\theta$ parameter, neutron EDM, strong CP problem, PQ mechanism, axion mass from $\chi_t$, UV completions (KSVZ/DFSZ), experimental landscape. ~5–6 pages.

---

### 18. Ch 14 §14.4 3+1D Iffiness — PASS

**Location:** `ch14_sectors_3plus1d.tex`, lines 500–601 (`\label{subsec:qcd-caveats}`)  
**Content:** 5 subsubsections classifying QCD observables by reliability. Includes summary table (lines 581–596) categorizing observables as (c)/(d) with forward-reference to Ch 15 taxonomy. ~3–4 pages.

---

### 19. Ch 15 §15.2 Four-Category Observable Taxonomy — PASS (marginal)

**Location:** `ch15_defects_synthesis.tex`, lines 173–245 (`\label{subsec:when-topological}`)  
**Content:** Formal Table (`tab:observable-taxonomy`, lines 183–206) defining categories (a)–(d), plus paragraph-length discussions of each category, three worked examples for category (d), and upgrading/downgrading discussion. ~4–5 pages.

**Flag:** As the declared Priority #1 / unique contribution of the paper, this is on the lean side of the 5–8 page target. The intellectual content is complete and well-structured, but an expansion of 1–2 pages (additional worked examples or extended discussion of relation to existing literature on "topological protection") would strengthen its prominence.

---

### 20. Ch 16 Outlook — PASS

**Location:** `ch16_outlook.tex`, lines 41–134  
**Content:**
- §16.1 (lines 44–49): One paragraph summarizing paper's thesis. ✓
- §16.2 (lines 51–71): Five bold-topic paragraphs on open directions. ✓
- §16.3 (lines 73–131): Five topic areas with annotated reference bullet lists. ✓
- Total: ~4–5 pages. Matches spec.

---

### 21. Ch 01 Introduction — PASS

**Location:** `ch01_introduction.tex`, lines 40–328  
**Content:** Abstract block, §1.1 (scope and thesis), §1.2 (target audience), §1.3 (chapter-by-chapter roadmap with reading paths), §1.4 (non-coverage declarations). ~8–10 pages (exceeds 3–5 page target but is appropriate given the paper's scope).

---

### 22. BF/Toric-Code Triple-Derivation — PARTIAL

**Implementation:** Effectively Option A (modular chapters, each self-contained, with cross-references):
- **Ch 6** (`ch06_bf.tex`, 811 lines): Full continuum BF derivation.
- **Ch 7** (`ch07_dw.tex`, lines 445–581, §7.3): Proves toric code = untwisted $\mathbb{Z}_2$ DW; cross-refs ch06 (line 563) and scopes vs ch09 (line 574).
- **Ch 9** (`ch09_topological_order.tex`, lines 301–377, §9.4): Self-contained Z_2 BF mini-derivation with reader's note directing ch06 readers to skip.

**Issues:**
1. Decision not formally recorded in `decision_log.md`.
2. Ch 7 partially duplicates ch09 (both define toric-code Hamiltonian and prove gauge-theory identification) without editorial acknowledgment of the overlap.
3. Appendix D (`app_bf_zn.tex`) is a stub ("[To be written.]") leaving a dangling `\ref{app:bf-zn}` from ch06 line 339.

**Fix needed:** (a) Record the Option A decision in the decision log. (b) Add a brief editorial note in ch07 §7.3 acknowledging what ch09 repeats. (c) Either write Appendix D or remove the forward reference.

---

## Blocking Items (Must Fix Before Stage VI Close)

| Priority | Item | Effort |
|----------|------|--------|
| **CRITICAL** | Ch 8 §8.7: CM anomaly inflow example (Part 1→2 bridge) | 2–3 pages new content |
| HIGH | Ch 3 & 4 figures: wire TikZ into chapters | 30 min editorial |
| HIGH | Ch 11 §11.7: expand universal vs non-universal edge discussion | 1–2 pages new content |
| MEDIUM | BF triple-derivation: formal decision + Appendix D stub resolution | 1 hour editorial |
| MEDIUM | Ch 15 §15.2: consider expanding priority-#1 section | 1–2 pages optional |
| LOW | Ch 11 §11.5 numbering mismatch: verify task spec vs actual section numbering | Clarification only |

---

## Verdict

**Stage VI cannot close.** One FAIL (Ch 8 §8.7) and four PARTIAL items remain. The critical blocker is the missing condensed-matter anomaly inflow example, which is the conceptual bridge between Parts I and II of the paper.
