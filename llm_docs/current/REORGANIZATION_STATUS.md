---
created_at: "2026-05-01T17:23:47-04:00"
updated_at: "2026-05-02T00:55:00-04:00"
generated_by: "claude"
timestamp_source: "filesystem_birthtime"
---

# Paper Reorganization Status - updated 2026-05-02

## 2026-05-02: second-pass simplification

The 10-section structure from 2026-05-01 has been simplified to a 7-section Part I / Part II structure following the user's instructions in `llm_docs/reference/Final QFT Project Overview.md` and the detailed source map in `llm_docs/reference/tqft_observables_literature_review.md`.

The previous 10 stub files were copied into `tex_docs/archive_2026-05-02_pre_simplification/` and removed from the active directory. The new files replace them and carry inline bibliographic citations.

### Simplification rationale

The user's stated preferences:
- One centralized math chapter (math is always referenceable) rather than math scattered throughout the construction.
- Part II organized by *observable family*, not by subfield.
- A dedicated "how real is this observable?" subsection, rather than apologetics scattered everywhere.
- Fewer but denser sections.

## Active TeX files (2026-05-02)

```
tex_docs/
  part1_01_introduction.tex                 [TO WRITE - write last]
  part1_02_mathematical_toolkit.tex         [EXTRACT from archive_2026-05-01]
  part1_03_ordinary_to_chern_simons.tex     [REORGANIZE from archive_2026-05-01]
  part1_04_tqft_and_observables.tex         [MERGE from archive + write]
  part2_05_response_2plus1d.tex             [PARTIAL DRAFT migrated from archive_2026-05-02]
  part2_06_sectors_3plus1d.tex              [NEW WRITING]
  part2_07_defects_caveats_outlook.tex      [NEW WRITING]
  tex_docs_main_wrapper_20260501.tex        [updated to include Parts I and II]
  tqft_observables_unresolved_refs.bib      [expanded with ~20 new entries]
  archive_2026-05-01/                       [original 7 modular TeX drafts]
  archive_2026-05-02_pre_simplification/    [2026-05-01 10-section intermediate]
```

## New 7-section structure

### Part I: Construction

| # | File | Title | Target pages | Status |
|---|------|-------|-------------:|--------|
| 1 | `part1_01_introduction.tex` | Introduction | 3-5 | TO WRITE (write last) |
| 2 | `part1_02_mathematical_toolkit.tex` | Mathematical Toolkit | 15-20 | EXTRACT from archive |
| 3 | `part1_03_ordinary_to_chern_simons.tex` | From Ordinary Gauge Theory to Chern-Simons | 20-25 | REORGANIZE |
| 4 | `part1_04_tqft_and_observables.tex` | TQFT and Its Observables | 15-20 | MERGE from archive + write |

### Part II: Physics organized by observable family

| # | File | Title | Target pages | Status |
|---|------|-------|-------------:|--------|
| 5 | `part2_05_response_2plus1d.tex` | Topological Response in 2+1 Dimensions | 25-30 | PARTIALLY DRAFTED |
| 6 | `part2_06_sectors_3plus1d.tex` | Topological Sectors in 3+1 Dimensions | 15-20 | NEW WRITING |
| 7 | `part2_07_defects_caveats_outlook.tex` | Defects, Caveats, and Outlook | 12-15 | NEW WRITING |

Expected total: ~105-135 pages.

## Citation integration

Each section's header comments now list:
- Primary sources to migrate from (archive paths).
- Pedagogical and review references tied to that section.
- Landmark theory and experiment citations tied to the relevant subsections.

Bibliography stubs for all cited works live in `tex_docs/tqft_observables_unresolved_refs.bib`. The 2026-05-02 pass added the following previously-missing entries:

- Foundational TQFT / CS: `Atiyah1988TQFT`, `Dunne1999AspectsCS`.
- Topological-phases bridges: `Witten2016ThreeLecturesTopologicalPhases`, `TongQuantumHallLectures`.
- FQHE reviews: `Wen1995TopologicalOrdersEdgeExcitations`, `Stern2008AnyonsQHEReview`, `NayakSimonSternFreedmanDasSarma2008NonabelianAnyons`, `HalperinSternNederRosenow2011FractionalCharge`.
- FQHE experiment: `Saminadayar1997FractionalCharge`.
- QCD topology / axion: `Dine2000TASIStrongCP`, `Hook2018TASIStrongCPAxions`, `Marsh2016AxionCosmology`, `Teper2000TopologyInQCD`, `CichyLatticeWittenVeneziano`, `AreanU1AHolographicQCD`.
- Monopoles / defects: `Rajantie2024MonopoleTheoryOverview`, `FairbairnMonopolesRevisited`.
- Line operators and generalized symmetries: `GaiottoKapustinSeibergWillett2015GeneralizedSymmetries`, `KapustinWitten2007ElectricMagneticLanglands`.

Pre-existing stubs reused: `Witten1988TQFT`, `Witten1989Jones`, `BlauThompson1991TopologicalGauge`, `BirminghamBlauRakowskiThompson1991TopologicalFieldTheory`, `Dijkgraaf1989Geometry2dCFT`, `ElitzurMooreSchwimmerSeiberg1989CanonicalCS`, `Nakahara2003GeometryTopologyPhysics`, `BaezMuniain1994GaugeFieldsKnotsGravity`, `Laughlin1983AnomalousQHE`, `ArovasSchriefferWilczek1984FractionalStatistics`, `ZhangHanssonKivelson1989FQHE`, `WenZee1992AbelianQHClassification`, `WenNiu1990GroundStateDegeneracy`, `Wen1990TopologicalOrders`, `TsuiStormerGossard1982FQHEDiscovery`, `dePicciotto1997FractionalCharge`, `CaminoZhouGoldman2005ABSuperperiod`, `VenkatachalamHartPfeifferWestYacobyGrapheneInterferometers`, `Nakamura2020AnyonicBraiding`, `Bartolomei2020AnyonCollisions`, `tHooft1976BellJackiw`, `tHooft1976Pseudoparticle`, `Witten1979U1GoldstoneBoson`, `Veneziano1979U1WithoutInstantons`, `DiVecchiaVeneziano1980ChiralDynamics`, `Abel2020NeutronEDM`, `Dirac1931QuantisedSingularities`, `tHooft1974MagneticMonopoles`, `Polyakov1974ParticleSpectrum`, `MantonSutcliffeTopologicalSolitons`, `ShnirMagneticMonopoles`, `WeinbergClassicalSolutionsQFT`.

Still placeholders (from `tqft_observables_unresolved_cleanup_checklist.md`): `RosenowHalperinInterferometryPlaceholder`, `ADMXOverviewPlaceholder`, `CASTIAXOOverviewPlaceholder`, `CASPErOverviewPlaceholder`, `MADMAXOverviewPlaceholder`, `PDGMagneticMonopolesPlaceholder`, `KapustinSaulinaLineOperatorsPlaceholder`. Replace these with concrete papers before submission.

## Next steps

1. Section 5 is the most populated: the Laughlin / quasihole / edge / K-matrix prose is already migrated inline, with `\cite{...}` calls present. Remaining TODOs: subsections 5.5 (Maxwell-CS) and 5.6 (QHE caveats).
2. Section 2 (math toolkit): migrate `archive_2026-05-01/topology_review.tex` subsections into the new subsection plan in `part1_02_mathematical_toolkit.tex`.
3. Section 3 (ordinary gauge -> CS): migrate `archive_2026-05-01/differential_forms_csimons_foundations_v2.tex` into subsection 3.3, and `archive_2026-05-01/dense_derivation_expansion.tex` level-quantization calculation into 3.5.
4. Section 4 (TQFT + observables): migrate Wilson-loop and torus-H computations from the archive into 4.4-4.5; write the functorial summary and observable taxonomy.
5. Sections 6 and 7: new writing from scratch, but the source map and review citations are already in the header comments.
6. Sections 1 and final outlook of 7: write last, once all other material is stable.
7. Pass through `tqft_observables_unresolved_cleanup_checklist.md` to convert placeholders to concrete papers.

## Migration priority (updated)

**Priority 1 (strongest existing content / partly migrated)**
- Section 5: finish Maxwell-CS and caveats subsections.
- Section 3: migrate anomaly-descent / CS-action / level-quantization prose.
- Section 4.4-4.5: migrate Wilson-loop and torus-H calculations.

**Priority 2 (extraction/reorganization)**
- Section 2: extract math toolkit from `archive_2026-05-01/topology_review.tex`.
- Section 4.1-4.3: write functorial summary and TQFT class taxonomy.

**Priority 3 (new writing)**
- Section 6: theta, chi_t, eta', strong CP, axion.
- Section 7.1: monopoles and line operators.
- Section 7.2: unified strict-vs-effective taxonomy.

**Priority 4 (bookends)**
- Section 1: introduction.
- Section 7.3: guide du routard and closing.

## Key principles (unchanged)

1. Math centralized in one reference chapter (Section 2).
2. Physics organized by observable family, not by subfield.
3. Concrete before abstract: Laughlin states before modular-tensor language.
4. Dedicated "iffiness" subsections in each physics section + unified taxonomy in 7.2.
5. Chern-Simons is the construction centerpiece; Sections 5-7 are the payoff.
