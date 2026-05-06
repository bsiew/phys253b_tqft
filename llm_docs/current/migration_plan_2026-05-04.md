---
created_at: "2026-05-04T16:00:00-04:00"
updated_at: "2026-05-05T22:03:06-04:00"
generated_by: "claude_opus_4.6"
timestamp_source: "agent_clock"
updated_by: "claude-code"
---

# Migration Plan: BSIEW Integration (2026-05-04)

> **Decision.** Adopt the BSIEW chapter structure for the 2+1d condensed-matter
> core (Ch 9--13), graft the current Secs 6--7 as new Ch 14--15, and add a
> short Ch 16 (Outlook) absorbing the guide du routard and BSIEW Ch 14 items.
> Part I integration is deferred; Ch 9 carries a self-contained BF insert.

## 1. What Was Done (Completed 2026-05-04)

### 1.1 Archive

All pre-integration tex files copied to:
```
tex_docs/archive_2026-05-04_pre_bsiew_integration/
  part1_01_introduction.tex
  part1_02_mathematical_toolkit.tex
  part1_03_ordinary_to_chern_simons.tex
  part1_04_tqft_and_observables.tex
  part2_05_response_2plus1d.tex
  part2_06_sectors_3plus1d.tex
  part2_07_defects_caveats_outlook.tex
  tex_docs_main_wrapper_20260501.tex
  tqft_observables_unresolved_refs.bib
```

### 1.2 New Chapter Files Created

| File | Source | Method |
|------|--------|--------|
| `ch09_topological_order.tex` | New | Written from BSIEW tasks 09_1--09_4, with self-contained BF insert in §9.4 |
| `ch10_anyons.tex` | New | Written from BSIEW tasks 10_1--10_5 |
| `ch11_fqhe.tex` | Migrated | Lines 65--301 of `part2_05_response_2plus1d.tex` restructured into §11.1--11.7. All drafted equations and prose preserved verbatim. |
| `ch12_experiments.tex` | New | Written from BSIEW tasks 12_1--12_4, plus new §12.4 (Bartolomei) |
| `ch13_tqc.tex` | New | Written from BSIEW tasks 13_1--13_3, plus new §13.4 (outlook) |
| `ch14_sectors_3plus1d.tex` | Copied | `cp part2_06_sectors_3plus1d.tex`, header updated to Ch 14 numbering |
| `ch15_defects_synthesis.tex` | Copied + edited | `cp part2_07_defects_caveats_outlook.tex`, header updated, guide du routard section removed (moved to ch16) |
| `ch16_outlook.tex` | New | Absorbs guide du routard from old Sec 7.3 + BSIEW Ch 14 outlook items |

### 1.3 Main Wrapper Updated

`tex_docs_main_wrapper_20260501.tex` now inputs Part I (unchanged) followed by
Part II chapters ch09--ch16. The old `part2_0*.tex` files remain at the top
level for now; they are superseded by the `ch*.tex` files and will be
quarantined to `_holding/` after full verification.

---

## 2. Part II Chapter Map (Ch 9--16)

| Ch | Title | pp | Source | Status | Owner | Stage |
|----|-------|----|--------|--------|-------|-------|
| 9 | Topological Order and the Toric Code | ~8 | New + BF insert | New writing | Helena | IV |
| 10 | Anyons, Braiding, Fusion, and Modular Data | ~10 | New | New writing | Joint | IV |
| 11 | Fractional Quantum Hall Effect | ~12 | Migrated from part2_05 | ~80% drafted | Helena | IV |
| 12 | Experiments on Anyonic Braiding | ~10 | New | New writing | Helena | V |
| 13 | Topological Quantum Computation | ~8 | New | New writing | Helena | V |
| 14 | Topological Sectors in 3+1D | ~15-20 | Migrated from part2_06 | TODO stubs | Helena | New |
| 15 | Defects, Global Structure, and Synthesis | ~10-12 | Migrated from part2_07 | TODO stubs | Helena | New |
| 16 | Outlook and Synthesis | ~4 | New | New writing | Joint | VI |

**Total Part II estimate:** ~77--84 pp

---

## 3. Chapter-by-Chapter Section Plans

### Ch 9: Topological Order and the Toric Code

| § | Content | BSIEW task | pp | Status |
|---|---------|------------|-----|--------|
| 9.1 | LRE vs symmetry breaking | 09_1 | ~2 | TODO |
| 9.2 | Toric code Hamiltonian, 4-fold GSD | 09_2 | ~2.5 | TODO |
| 9.3 | Emergent anyons: e, m, epsilon | 09_3 | ~1.5 | TODO |
| 9.4 | Continuum limit: Z_2 BF theory (self-contained) | 09_4 adapted | ~2 | TODO |

**Key design decision:** §9.4 derives the BF action, linking phase, and GSD
from scratch (~2 pp). Does NOT assume Part I has a BF chapter. Leaves
`\label{sec:bf-self-contained}` for Part I cross-referencing.

### Ch 10: Anyons, Braiding, Fusion, and Modular Data

| § | Content | BSIEW task | pp | Status |
|---|---------|------------|-----|--------|
| 10.1 | Fusion rules, pentagon | 10_1 | ~1.5 | TODO |
| 10.2 | Braiding, hexagon, topological spin | 10_2 | ~1.5 | TODO |
| 10.3 | Modular S-matrix for U(1)_k (DERIVATION) | 10_3 | ~3 | TODO (Brian) |
| 10.4 | CS primary labels, Wilson-loop dictionary | 10_4 | ~2 | TODO (Brian) |
| 10.5 | Anyon comparison table (SHOWPIECE) | 10_5 | ~1 | TODO (Joint) |

### Ch 11: Fractional Quantum Hall Effect

| § | Content | BSIEW task | Source | Status |
|---|---------|------------|--------|--------|
| 11.1 | Quantum Hall setup | 11_1 | part2_05 opening (expand) | Partial |
| 11.2 | Laughlin→CS, Hall response | 11_2 | part2_05 §5.1 (lines 82-131) | **DONE** |
| 11.3 | Quasiparticles as Wilson endpoints | 11_3 | part2_05 §5.2 (lines 132-172) | **DONE** |
| 11.4 | Edge, inflow, GSD | 11_4 | part2_05 §5.3 (lines 174-213) | **DONE** |
| 11.5 | K-matrix, nonabelian | — | part2_05 §5.4 (lines 215-254) | **DONE** |
| 11.6 | Maxwell-CS contrast | — | part2_05 §5.5 TODO stub | TODO |
| 11.7 | Scope/limitations + caveats | 11_5 | part2_05 §5.6 + BSIEW 11_5 | TODO |

### Ch 12: Experiments on Anyonic Braiding

| § | Content | BSIEW task | pp | Status |
|---|---------|------------|-----|--------|
| 12.1 | Nakamura 2020 nu=1/3 | 12_1 | ~3 | TODO |
| 12.2 | Werkmeister 2024 graphene | 12_2 | ~2 | TODO |
| 12.3 | Andersen 2023 + caveat | 12_3 | ~2 | TODO |
| 12.4 | Bartolomei 2020 + shot-noise | New | ~1.5 | TODO |
| 12.5 | Figures | 12_4 | — | TODO |

### Ch 13: Topological Quantum Computation

| § | Content | BSIEW task | pp | Status |
|---|---------|------------|-----|--------|
| 13.1 | Kitaev's proposal | 13_1 | ~1.5 | TODO |
| 13.2 | Ising anyons worked example | 13_2 | ~3 | TODO |
| 13.3 | Experimental status (REQUIRED) | 13_3 | ~1 | TODO |
| 13.4 | Brief outlook | New | ~1 | TODO |

### Ch 14: Topological Sectors in 3+1D

| § | Content | pp | Status |
|---|---------|-----|--------|
| 14.1 | Theta vacua, chi_t, U(1)_A | ~5 | TODO stub with outline |
| 14.2 | Eta' mass, Witten-Veneziano | ~4 | TODO stub with outline |
| 14.3 | Strong CP, nEDM, axion | ~5 | TODO stub with outline |
| 14.4 | Caveats | ~2 | TODO stub with outline |

### Ch 15: Defects, Global Structure, and Synthesis

| § | Content | pp | Status |
|---|---------|-----|--------|
| 15.1 | Monopoles, line operators, global structure | ~6 | TODO stub with outline |
| 15.2 | Four-category "when topological" taxonomy | ~4-6 | TODO stub with outline |

### Ch 16: Outlook and Synthesis

| § | Content | pp | Status |
|---|---------|-----|--------|
| 16.1 | What this paper demonstrated | ~0.5 | TODO |
| 16.2 | Open directions | ~1.5 | TODO |
| 16.3 | Guide du routard | ~2 | TODO (migrated from old Sec 7.3) |

---

## 4. BSIEW Task Coverage

### Fully covered by new chapter files

- **Stage I** (01_1--01_9): Skeleton tasks. Main wrapper updated; bib exists; figure/table checklists still applicable.
- **Stage IV** (09_1--09_4, 10_1--10_5, 11_1--11_5): All tasks mapped to ch09--ch11.
- **Stage V** (12_1--12_4, 13_1--13_3): All tasks mapped to ch12--ch13.
- **Stage VI** (14_1--14_11): Integration tasks are structure-independent; all still applicable.
- **Stage VII** (15_1--15_7): Presentation tasks are structure-independent.

### Adapted

- **09_4** (IR BF roundtrip): Now includes a self-contained BF derivation instead of cross-referencing Part I Ch 6. Task scope expanded by ~1 page.

### BSIEW chapters with no counterpart (orphaned tasks)

- **Stage II** (02_1--02_7): Part I Ch 2 math toolkit. Part I deferred; tasks still relevant when Part I integration happens.
- **Stage II** (03_1--03_5): Part I Ch 3 axiomatic TQFT. Deferred.
- **Stage II** (04_1--04_5): Part I Ch 4 Frobenius. Deferred.
- **Stage III** (06_1--06_4): Part I Ch 6 BF theory. §9.4 covers a compressed version; full BF deferred to Part I.
- **Stage III** (07_1--07_5): Part I Ch 7 DW theory. Deferred.
- **Stage III** (08_1--08_9): Part I Ch 8 generalized symmetries. Compressed into Ch 15 line operators subsection.

### New content with no BSIEW counterpart

| New section | BSIEW gap | Notes |
|-------------|-----------|-------|
| Ch 11 §11.5 (K-matrix) | No task | Drafted content from current structure, fits naturally |
| Ch 11 §11.6 (Maxwell-CS) | No task | Original scope addition |
| Ch 12 §12.4 (Bartolomei) | No task | Expands parenthetical citations |
| Ch 13 §13.4 (TQC outlook) | No task | Brief ~1 pp |
| Ch 14 (entire) | No tasks | Original scope: QCD topology, axions |
| Ch 15 (entire) | No tasks | Original scope: monopoles, synthesis |
| Ch 16 (entire) | Partially BSIEW Ch 14 | Outlook absorbs BSIEW + current Sec 7.3 |

---

## 5. Writing Priority Order

| Priority | Chapter | Rationale |
|----------|---------|-----------|
| 1 | Ch 11 | ~80% drafted; fill §11.1 expansion, §11.6, §11.7. Locks down centerpiece. |
| 2 | Ch 9 | Pedagogical on-ramp. Toric code + BF insert gives Ch 11 its conceptual foundation. |
| 3 | Ch 12 | Experiments. Depends on Ch 11 theoretical predictions. |
| 4 | Ch 10 | Anyon formalism. Can parallel Ch 12 (mostly independent). |
| 5 | Ch 13 | TQC. Depends on Ch 10 (Ising data) and Ch 12 (Andersen context). |
| 6 | Ch 14 | Independent of Ch 9--13; can write whenever. |
| 7 | Ch 15 | Independent; benefits from Ch 14 being done (four-category table cites Ch 14). |
| 8 | Ch 16 | Write last; summarizes everything. |

---

## 6. Cross-Reference Updates Needed

The migrated prose in Ch 11 contains references to the old section structure
that must be updated:

| Old reference | New reference | Location |
|---------------|---------------|----------|
| `\ref{sec:tqft-observables}` | Unchanged (Part I Sec 4 label) | ch11 §11.3 |
| `\ref{subsec:hilbert-surfaces-gsd}` | Unchanged (Part I Sec 4.5 label) | ch11 §11.4 |
| Forward-ref to "Sec 5 experiments" | `\ref{sec:experiments}` (Ch 12) | ch11 §11.3 |
| Forward-ref to "Sec 7.2 taxonomy" | `\ref{subsec:when-topological}` (Ch 15 §15.2) | ch11 §11.7 |
| Forward-ref to "Ch 10 table" | `\ref{subsec:anyon-comparison-table}` | ch11 §11.5 |

The Ch 14 and Ch 15 comment blocks reference "Sec. 5.6" and "Sec. 6.4";
these should be updated to "Ch 11 §11.7" and "Ch 14 §14.4" respectively
during the writing pass.

---

## 7. Through-Line Update

The BSIEW through-line ("TQFT is the infrared language of gapped phases;
three touchstones: Frobenius, CS, DW") no longer works because Frobenius
and DW are deferred to Part I.

**New through-line for Part II:**
> Ordinary QFT already contains topological sectors; Chern-Simons theory
> isolates them; TQFT formalizes them; observable families organize the physics.
> The condensed-matter core (Ch 9--13) demonstrates this on topological order,
> anyons, and the FQHE. The cross-disciplinary additions (Ch 14--15)
> show the same structures governing QCD vacuum topology, monopole charge
> quantization, and the "when topological vs. effective" question.

This should be reflected in Ch 1 (Introduction) and Ch 16 (Outlook) when
those chapters are written.

---

## 8. Files to Quarantine After Full Verification

Once all cross-references are confirmed working and the new chapter files
compile cleanly, the superseded files should be moved to `_holding/`:

```
part2_05_response_2plus1d.tex  -> _holding/  (superseded by ch11_fqhe.tex)
part2_06_sectors_3plus1d.tex   -> _holding/  (superseded by ch14_sectors_3plus1d.tex)
part2_07_defects_caveats_outlook.tex -> _holding/  (superseded by ch15 + ch16)
```

The Part I files (`part1_01` through `part1_04`) remain active until Part I
integration is decided.

---

## 9. Stage File Updates

The BSIEW stage files need the following updates:

- **stage_IV_partII_A.md**: Add note that Ch 9 §9.4 is now self-contained
  for BF (no dependency on Part I Ch 6). Add Ch 11 §11.5 (K-matrix) as a
  non-BSIEW addition.
- **stage_V_partII_B.md**: Add Ch 12 §12.4 (Bartolomei) and Ch 13 §13.4
  (TQC outlook) as new subsections.
- **stage_VI_integration.md**: Update "must include" audit (Task 14.8) to
  reference new chapter numbers. Add note that through-line has changed.
- **New stage file needed**: stage for Ch 14--15 writing (no BSIEW counterpart).
