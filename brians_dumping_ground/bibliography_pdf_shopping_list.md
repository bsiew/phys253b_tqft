# PDF Shopping List — Physical Sources for `tqft_review.bib`

Living note created 2026-05-03 (Task 1.5 deliverable).

All 26 bib entries map to one of three states:

- **✅ on disk** — a PDF already sits under `references/`, and you can skim any time.
- **🛒 should fetch** — the paper is load-bearing for a chapter we plan to draft in detail; having the PDF locally would be useful for verifying theorem numbers, equations, and experimental details.
- **🟡 optional** — useful but we can get away with the arXiv abstract / DOI landing page.

## Already on disk (no action needed)

| Bib key | Corresponding file | Chapter(s) using it |
|---|---|---|
| `Schwartz2014QFT` | `references/textbook/Matthew_D_Schwartz_Quantum_Field_Theory_And_The_Standard_Model.pdf` | All of Part I (calibration) |
| `Nakahara2003GTP` | `references/textbook/Nakahara_GeometryTopologyandPhysics.pdf` | Ch 2, Ch 5, Appendix A |
| `Tong2016QHE` | `references/textbook/Tong_QuantumHallEffect.pdf` | Ch 5 (CS conventions), Ch 11 |
| `Atiyah1988TQFT` | `references/textbook/atiyahtqft.pdf` | Ch 3 (axioms source) |
| `Witten1989Jones` | `references/textbook/Witten_QFTandtheJonesPolynomial.pdf` | Ch 5 §Witten–Jones, Ch 10 |
| `Freed1995CSnotes` | `references/textbook/Freed_ChernSimonsTheoryNotes.pdf` | Ch 5 appendix, App C |
| `Kock2004Frobenius` | `references/textbook/Kock_FrobeniusAlgebrasand2DTQFTs.pdf` | Ch 4 (main source), App B |

Also on disk but not currently a bib entry:
- `Bartlett_CategoricalAspectsofTQFTs.pdf` — useful for App A (category primer). Not cited yet; I can add as `Bartlett2005` when drafting App A needs it.
- `Freed_DifferentialGeometryNotes.pdf` — background reference for Ch 2 and App A.
- `Tong_GaugeTheory.pdf` — background for Ch 6 (BF) and Ch 8 (generalized symmetry). I'll add `Tong2018GaugeTheory` when Ch 6 is drafted.

## Should fetch — load-bearing for planned chapters

Drop these into `references/textbook/` (for review-type sources) or create a new `references/experiments/` folder (for the experimental papers). Filenames below match what I'll expect when we draft the chapters; feel free to rename if you prefer.

### Experimental papers (for Ch 12)

| Bib key | Suggested filename | Where to get it | Why we need it |
|---|---|---|---|
| `Nakamura2020` | `references/experiments/Nakamura2020_FQHBraiding.pdf` | DOI `10.1038/s41567-020-1019-1` (Nature Physics 16:931–936). Harvard library access or the authors' arXiv preprint `arXiv:2006.14115`. | §12.1 interferometer schematic, the measured $e^{2\pi i/3}$ braiding phase. Helena will want this open while drafting. |
| `Werkmeister2025` | `references/experiments/Werkmeister2025_GrapheneInterferometer.pdf` | DOI `10.1126/science.adp5015` (Science 388:730–735). arXiv preprint `arXiv:2403.18983` is the free version. | §12.2. Graphene interferometer device details, telegraph-noise signal. |
| `Andersen2023` | `references/experiments/Andersen2023_SupercondBraiding.pdf` | DOI `10.1038/s41586-023-05954-4` (Nature 618:264–269). arXiv `arXiv:2210.10255`. | §12.3. Non-abelian braiding emulation on Google's Sycamore processor. The honesty box in §12.3 needs this open. |

### Foundational TQFT (for Ch 7 and Ch 8)

| Bib key | Suggested filename | Where to get it | Why we need it |
|---|---|---|---|
| `DijkgraafWitten1990` | `references/textbook/DijkgraafWitten1990.pdf` | DOI `10.1007/BF02096988` (Commun. Math. Phys. 129:393–429). Likely available through Harvard library or Springer. | Ch 7, the original paper. Nice to have open for the cohomological classification of twisted DW theories. |
| `GKSW2015` | `references/textbook/GKSW2015_GeneralizedSymmetries.pdf` | DOI `10.1007/JHEP02(2015)172` (JHEP 2015:172). arXiv `arXiv:1412.5148` is free. | Ch 8 (§8.1–8.3). This is *the* canonical reference for higher-form symmetries and must be consulted for the dictionary table (Task 8.2). |
| `CallanHarvey1985` | `references/textbook/CallanHarvey1985_AnomalyInflow.pdf` | DOI `10.1016/0550-3213(85)90489-4` (Nucl. Phys. B250:427–436). Often behind paywalls; try Harvard library. | Ch 8 §8.5–8.6 derivation of anomaly inflow. |

### Topological order (for Ch 9, Ch 10, App E)

| Bib key | Suggested filename | Where to get it | Why we need it |
|---|---|---|---|
| `Kitaev2003` | `references/textbook/Kitaev2003_AnyonsFaultTolerant.pdf` | DOI `10.1016/S0003-4916(02)00018-0` (Ann. Phys. 303:2–30). arXiv `arXiv:quant-ph/9707021` is free. | Ch 9 (toric code Hamiltonian and string operators), Ch 13 (TQC foundations). High-value paper to have open. |
| `KitaevPreskill2006` | `references/textbook/KitaevPreskill2006_TEE.pdf` | DOI `10.1103/PhysRevLett.96.110404` (Phys. Rev. Lett. 96:110404). arXiv `arXiv:hep-th/0510092` is free. | App E full derivation of the subtraction geometry. |
| `LevinWen2006` | `references/textbook/LevinWen2006_DetectingTO.pdf` | DOI `10.1103/PhysRevLett.96.110405` (same issue). arXiv `arXiv:cond-mat/0510613` is free. | App E cross-check, Ch 9 §9.1 definition of topological order. |
| `NayakSimonSternFreedmanDasSarma2008` | `references/textbook/Nayak2008_NonAbelianAnyonsRMP.pdf` | DOI `10.1103/RevModPhys.80.1083` (Rev. Mod. Phys. 80:1083–1159). arXiv `arXiv:0707.1889` is free. | Ch 10, Ch 13. The canonical pedagogical review for non-abelian anyons; should have open while drafting. |

### Optional 2025 follow-ups (for Ch 12 only if included)

| Bib key | Suggested filename | Where to get it | Why (optional) |
|---|---|---|---|
| `Ghosh2025` | `references/experiments/Ghosh2025_nu52.pdf` | DOI `10.1038/s41567-025-02960-3` | Only if we want to include $\nu = 5/2$ non-abelian claims in §12. |
| `Ruelle2025` | `references/experiments/Ruelle2025_Interferometry.pdf` | DOI `10.1126/science.adm7695` | Only if we want to discuss the 2025 Science follow-up. |

*Author lists in both `Ghosh2025` and `Ruelle2025` are placeholder — they need to be verified against the published version. Grabbing the PDF lets us fix the bib entries with exact titles.*

## Not being fetched

### `Bhardwaj2023Lectures` (arXiv:2307.07547)

We cite this as a *pedagogical* reference in Ch 8, so we don't need the PDF ourselves — the abstract plus section titles from arXiv are enough to confirm it's the right citation. **Action: skip; arXiv abstract is fine.**

### `FreedMooreTeleman2024` (arXiv:2209.07471)

Ditto — used as a *pointer* in the outlook and the Ch 8 SymTFT slogan, not as a source for a derivation. **Action: skip.**

### Other existing bib entries with DOIs but no PDF needed

`DeserJackiwTempleton1982`, `ElitzurMooreSchwimmerSeiberg1989`, `ReshetikhinTuraev1991`, `Turaev2016QuantumInvariants`, `SeibergWitten2016Spin` — we cite these at the "such-and-such established" level, not at the "we're reproducing equation X of paper Y" level. **Action: skip.**

## Summary for you

**Essential** (drop into `references/experiments/` and `references/textbook/`; these will be open while we draft):

1. Nakamura 2020 — FQH anyon braiding (arXiv:2006.14115 is fine)
2. Werkmeister 2025 — graphene interferometer (arXiv:2403.18983 is fine)
3. Andersen 2023 — superconducting non-abelian braiding (arXiv:2210.10255 is fine)
4. GKSW 2015 — generalized symmetries (arXiv:1412.5148 is fine)
5. Kitaev 2003 — anyons and fault-tolerance (arXiv:quant-ph/9707021 is fine)
6. Nayak et al 2008 — RMP review of non-abelian anyons (arXiv:0707.1889 is fine)
7. Kitaev–Preskill 2006 — TEE (arXiv:hep-th/0510092 is fine)
8. Levin–Wen 2006 — TEE cross-check (arXiv:cond-mat/0510613 is fine)

**Nice-to-have** (grab if easy):

9. Dijkgraaf–Witten 1990 — original DW paper (journal PDF; no free arXiv)
10. Callan–Harvey 1985 — original inflow paper (journal PDF; no free arXiv)

**Optional** (only if we decide to include 2025 follow-ups):

11. Ghosh 2025
12. Ruelle 2025

All eight "essential" items are freely available on arXiv. If you're comfortable with `curl`/`wget`, you can batch-grab them in five minutes; otherwise just drag-and-drop the PDFs from the arXiv abstract pages.
