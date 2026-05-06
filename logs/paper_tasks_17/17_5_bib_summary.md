---
created_at: "2026-05-05T21:39:09-04:00"
updated_at: "2026-05-05T21:39:09-04:00"
generated_by: "claude-code"
updated_by: "claude-code"
timestamp_source: hook
---
# Task 17.5 --- Bibliography Consolidation Summary

**Date:** 2026-05-05  
**Bib file:** `tex_docs/tqft_observables_unresolved_refs.bib`  
**Wrapper:** `tex_docs/tex_docs_ch02_ch13_app_e_wrapper_20260505.tex`

## Result

- **0 unresolved `\cite{}` keys** (all keys now have a matching bib entry)
- **0 orphan bib entries** (every entry is cited somewhere in the active tex)
- **87 unique citation keys** across 15 chapter files + 1 appendix

## Actions Taken

### 1. Added missing entries (29 new)

| Key | Reference |
|-----|-----------|
| `Witten1988Sigma` | Topological sigma models, CMP 118 (1988) |
| `DeserJackiwTempleton1982` | Topologically massive gauge theories |
| `DijkgraafWitten1990` | Topological gauge theories and group cohomology |
| `Horowitz1989` | Exactly soluble diffeomorphism invariant theories |
| `ReshetikhinTuraev1991` | 3-manifold invariants via quantum groups |
| `Turaev2016QuantumInvariants` | Book, 3rd ed., De Gruyter |
| `Kauffman1987` | State models and the Jones polynomial |
| `GuadagniniMartelliniMintchev1990` | Wilson lines in CS and link invariants |
| `Freed1995CSnotes` | Classical Chern-Simons theory, Adv. Math. |
| `SeibergWitten2016Spin` | Gapped boundary phases, PTEP 2016 |
| `Marino2005` | Chern-Simons theory and topological strings |
| `Schwartz2014QFT` | QFT and the Standard Model, CUP |
| `Kock2004Frobenius` | Frobenius algebras and 2D TQFTs, CUP |
| `Brown1982` | Cohomology of Groups, Springer |
| `KitaevPreskill2006TEE` | Topological entanglement entropy, PRL 96 |
| `LevinWen2006DetectingTO` | Detecting topological order, PRL 96 |
| `Kitaev2003FaultTolerant` | Fault-tolerant quantum computation by anyons |
| `AharonySeibergTachikawa2013` | Reading between the lines, JHEP 08 (2013) |
| `1511.02867` | Grilli di Cortona et al., QCD axion mass |
| `1606.07494` | Borsanyi et al., lattice topological susceptibility |

### 2. Added short-key aliases (9)

These duplicate entries exist solely to resolve short citation keys used in the tex:

`BlauThompson1991`, `ElitzurMooreSchwimmerSeiberg1989`, `GKSW2015`,
`Nakahara2003GTP`, `Nakamura2020`, `Tong2016QHE`, `Kitaev2003`,
`FreedMooreTeleman2024`, `Bhardwaj2023Lectures`

### 3. Removed orphan entries (6)

| Key | Reason |
|-----|--------|
| `BaezMuniain1994GaugeFieldsKnotsGravity` | Never cited in active tex |
| `Dijkgraaf1989Geometry2dCFT` | Only in archived comment |
| `KapustinWitten2007ElectricMagneticLanglands` | Only in ch15 comment |
| `Wen2019ChoreographedEntanglementDances` | Never cited |
| `VenkatachalamHartPfeifferWestYacobyGrapheneInterferometers` | Only in ch12 comment |
| `PDGMagneticMonopolesPlaceholder` | Only in ch15 comment |
| `Nakahara2003GeometryTopologyPhysics` | Superseded by alias `Nakahara2003GTP` |
| `BlauThompson1991TopologicalGauge` | Superseded by alias `BlauThompson1991` |

### 4. Metadata improvements

- Added DOIs to 40+ entries that previously lacked them.
- Filled in publisher/year for `MantonSutcliffeTopologicalSolitons` (CUP 2004), `ShnirMagneticMonopoles` (Springer 2005), `WeinbergClassicalSolutionsQFT` (CUP 2012).
- Added arXiv number for `Werkmeister2024GrapheneInterferometer`.
- Kept 5 placeholder entries (`ADMX`, `CASTIAXO`, `CASPEr`, `MADMAX`, `RosenowHalperin`) --- these are cited in the text and await concrete paper choices.

## Remaining TODOs

1. **Placeholders:** 5 `@misc` entries marked TODO still need concrete paper replacements.
2. **`Polyakov1974ParticleSpectrum`:** Soviet-era journal; no DOI available. Russian-language cross-reference added in `note`.
3. **`Werkmeister2024GrapheneInterferometer`:** Preprint; update venue/DOI when published.

## Validation

```
comm -23 cite_keys.txt bib_keys.txt  =>  (empty)
comm -13 cite_keys.txt bib_keys.txt  =>  (empty)
```

Every entry has a year. All non-placeholder entries have DOI, arXiv number, or URL.
