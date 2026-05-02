# TQFT Observables Unresolved Citation Cleanup Checklist

Source note: `PROJECTS/QFT/253b_final_paper/llm_docs/reference/tqft_observables_literature_review.md`

Current status from the citation manifest:

- Total unique cited items: `60`
- ArXiv-resolved with local TeX already present: `19`
- Still unresolved / manual-cleanup items: `41`
- BibTeX stub file created: `PROJECTS/QFT/253b_final_paper/tex_docs/tqft_observables_unresolved_refs.bib`

## 1. Concrete citation stubs now exist

These entries now have explicit BibTeX stubs in the new `.bib` file and can be cited immediately, even if some of them still deserve a final metadata polish:

- Foundational TQFT / Chern-Simons: `Witten1988TQFT`, `Witten1989Jones`, `BlauThompson1991TopologicalGauge`, `BirminghamBlauRakowskiThompson1991TopologicalFieldTheory`, `Dijkgraaf1989Geometry2dCFT`, `ElitzurMooreSchwimmerSeiberg1989CanonicalCS`
- Pedagogical bridge texts: `Nakahara2003GeometryTopologyPhysics`, `BaezMuniain1994GaugeFieldsKnotsGravity`
- FQHE / topological order theory: `Wen1990TopologicalOrders`, `Wen2019ChoreographedEntanglementDances`, `HalperinJain2020FQHENewDevelopments`, `Laughlin1983AnomalousQHE`, `ArovasSchriefferWilczek1984FractionalStatistics`, `ZhangHanssonKivelson1989FQHE`, `WenZee1992AbelianQHClassification`, `WenNiu1990GroundStateDegeneracy`
- FQHE / anyon experiments: `TsuiStormerGossard1982FQHEDiscovery`, `dePicciotto1997FractionalCharge`, `CaminoZhouGoldman2005ABSuperperiod`, `VenkatachalamHartPfeifferWestYacobyGrapheneInterferometers`, `Nakamura2020AnyonicBraiding`, `Bartolomei2020AnyonCollisions`
- QCD / axion topology: `tHooft1976BellJackiw`, `tHooft1976Pseudoparticle`, `Witten1979U1GoldstoneBoson`, `Veneziano1979U1WithoutInstantons`, `DiVecchiaVeneziano1980ChiralDynamics`, `Abel2020NeutronEDM`
- Monopoles / defects: `Dirac1931QuantisedSingularities`, `tHooft1974MagneticMonopoles`, `Polyakov1974ParticleSpectrum`, `MantonSutcliffeTopologicalSolitons`, `ShnirMagneticMonopoles`, `WeinbergClassicalSolutionsQFT`

## 2. Stubs worth a final metadata check

These are now captured, but the source note did not include enough detail for me to be fully confident about the edition, publisher, or venue metadata:

- `Dijkgraaf1989Geometry2dCFT`: thesis citation is good enough as a stub, but degree institution / exact thesis metadata should be normalized if it goes into the final paper bibliography.
- `Nakahara2003GeometryTopologyPhysics`: the stub currently assumes the common 2nd-edition CRC/Taylor & Francis citation; confirm that this is the edition you want.
- `BaezMuniain1994GaugeFieldsKnotsGravity`: confirm preferred edition / publisher formatting.
- `HalperinJain2020FQHENewDevelopments`: editor-book stub is present, but you may want full publisher metadata.
- `VenkatachalamHartPfeifferWestYacobyGrapheneInterferometers`: the title is concrete but the literature-review note omitted venue/year; the BibTeX entry is intentionally marked `TODO`.
- `MantonSutcliffeTopologicalSolitons`, `ShnirMagneticMonopoles`, `WeinbergClassicalSolutionsQFT`: book stubs exist, but publisher/year metadata should be verified before final submission.

## 3. Entries that still need a canonical target paper chosen

These were not really single citations in the literature-review note; they were citation buckets. I added placeholder `@misc` entries so there is a stable key and a TODO marker, but each one should be replaced by one or two real papers before they appear in the final bibliography:

- `RosenowHalperinInterferometryPlaceholder`
  Action: choose 1-2 flagship interferometry / Coulomb-dominated-regime papers rather than citing "various works."

- `ADMXOverviewPlaceholder`
  Action: choose a specific ADMX overview or flagship experimental status paper.

- `CASTIAXOOverviewPlaceholder`
  Action: split this into one CAST overview and one IAXO overview if both are actually discussed in the prose.

- `CASPErOverviewPlaceholder`
  Action: replace with a concrete CASPEr overview / proposal paper.

- `MADMAXOverviewPlaceholder`
  Action: replace with a concrete MADMAX overview / design paper.

- `PDGMagneticMonopolesPlaceholder`
  Action: replace with the exact PDG edition you want to cite.

- `KapustinSaulinaLineOperatorsPlaceholder`
  Action: replace with a specific Kapustin-Saulina paper on line / surface operators.

## 4. Recommended next cleanup pass

1. Pull 1-2 concrete papers for each placeholder bucket in Section 3.
2. Decide whether the final paper wants book-style citations for the broad pedagogical references or whether those should stay in prose-only recommendation sections.
3. If you start inserting `\cite{...}` calls into `tex_docs`, either merge this stub file with a fuller bibliography or add a second bib file for the already-resolved arXiv-backed references.
