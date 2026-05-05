---
created_at: "2026-05-03T15:30:00-04:00"
updated_at: "2026-05-03T15:30:00-04:00"
generated_by: "claude_opus_4.6"
timestamp_source: "agent_clock"
---

# Compiled Literature for Deep Lit Review

> **Purpose.** This file consolidates every citation used in or planned for the 253b TQFT review paper. It is designed to be handed to an LLM for related-paper discovery, annotation, and gap analysis.
>
> **Paper structure.** Part I (Construction): Sec 1 Introduction, Sec 2 Mathematical Toolkit, Sec 3 From Ordinary QFT to Chern-Simons, Sec 4 TQFT and Observables. Part II (Physics by Observable Family): Sec 5 Topological Response in 2+1d, Sec 6 Topological Sectors in 3+1d, Sec 7 Defects, Caveats, and Outlook.
>
> **How to use this file.** Each entry has full bibliographic metadata, a one-line annotation of its role in the paper, the section(s) it serves, its BibTeX status, and a link where available. Entries marked `placeholder` need a canonical paper identified. Entries marked `not-in-bib` have a known paper but need a BibTeX entry written. The placeholder resolution tracker in Appendix A collects the 7 stubs needing real papers.

## Status Legend

| Tag | Meaning |
|-----|---------|
| `ready` | In `tqft_observables_unresolved_refs.bib` with complete metadata |
| `in-bib-incomplete` | In `.bib` but has TODO notes (missing DOI, publisher, year, etc.) |
| `placeholder` | BibTeX stub exists as `@misc{...Placeholder}` — needs canonical paper |
| `not-in-bib` | Known paper, not yet in any `.bib` file — needs entry created |

---

## Section 1: Foundational TQFT and Chern-Simons

> Papers defining TQFT axiomatically, constructing Chern-Simons theory, and establishing the core formal machinery.

### [01] Atiyah1988TQFT

- **Authors:** Atiyah, Michael F.
- **Title:** *Topological Quantum Field Theories*
- **Venue:** Publications Mathematiques de l'IHES **68** (1988) 175-186
- **Link:** DOI: not standardized (NUMDAM)
- **Status:** `ready`
- **Sections served:** Sec 1, Sec 2 (2.8 bordisms), Sec 4 (4.1 functorial definition)
- **Role:** Standard axiomatic/functorial starting point for TQFT; the paper that defines the framework

### [02] Witten1988TQFT

- **Authors:** Witten, Edward
- **Title:** *Topological Quantum Field Theory*
- **Venue:** Communications in Mathematical Physics **117** (1988) 353-386
- **Link:** DOI:10.1007/BF01223371
- **Status:** `ready`
- **Sections served:** Sec 1, Sec 4 (4.2 Witten-type TQFTs)
- **Role:** Original cohomological TQFT paper; distinguishes Witten-type from Schwarz-type TQFTs

### [03] Witten1989Jones

- **Authors:** Witten, Edward
- **Title:** *Quantum Field Theory and the Jones Polynomial*
- **Venue:** Communications in Mathematical Physics **121** (1989) 351-399
- **Link:** DOI:10.1007/BF01217730
- **Status:** `ready`
- **Sections served:** Sec 1, Sec 2, Sec 3, Sec 4 (4.3 CS as central example, 4.4 Wilson lines), Sec 7
- **Role:** Canonical reference for Chern-Simons theory, Wilson loops, knot invariants, and framing

### [04] BlauThompson1991TopologicalGauge

- **Authors:** Blau, M.; Thompson, G.
- **Title:** *Topological Gauge Theories of Antisymmetric Tensor Fields*
- **Venue:** Annals of Physics **205** (1991) 130-172
- **Link:** DOI:10.1016/0003-4916(91)90240-9
- **Status:** `ready`
- **Sections served:** Sec 4 (4.2 TQFT classes)
- **Role:** Broadens beyond CS to BF and other topological gauge theories

### [05] BirminghamBlauRakowskiThompson1991TopologicalFieldTheory

- **Authors:** Birmingham, D.; Blau, M.; Rakowski, M.; Thompson, G.
- **Title:** *Topological Field Theory*
- **Venue:** Physics Reports **209** (1991) 129-340
- **Link:** DOI:10.1016/0370-1573(91)90117-5
- **Status:** `ready`
- **Sections served:** Sec 1, Sec 3, Sec 4 (4.2), Sec 7 (caveats)
- **Role:** Best broad review of TQFTs; distinguishes classes, early gauge-theoretic examples

### [06] Dunne1999AspectsCS

- **Authors:** Dunne, Gerald V.
- **Title:** *Aspects of Chern-Simons Theory*
- **Venue:** Lectures at Les Houches 1998, arXiv:hep-th/9902115
- **Link:** [arXiv:hep-th/9902115](https://arxiv.org/abs/hep-th/9902115)
- **Status:** `ready`
- **Sections served:** Sec 1, Sec 3 (3.4 CS action), Sec 4 (4.4 linking), Sec 7
- **Role:** Physics-centered review of abelian and nonabelian CS; good for abelian linking derivations

### [07] Dijkgraaf1989Geometry2dCFT

- **Authors:** Dijkgraaf, R.
- **Title:** *A Geometrical Approach to Two-Dimensional Conformal Field Theory*
- **Venue:** PhD thesis (1989)
- **Link:** —
- **Status:** `in-bib-incomplete` (TODO: normalize institution/degree metadata)
- **Sections served:** Sec 4 (4.2 2d/3d boundary relation)
- **Role:** Historical/conceptual source for 2d boundary / 3d bulk relation

### [08] ElitzurMooreSchwimmerSeiberg1989CanonicalCS

- **Authors:** Elitzur, S.; Moore, G.; Schwimmer, A.; Seiberg, N.
- **Title:** *Remarks on the Canonical Quantization of the Chern-Simons-Witten Theory*
- **Venue:** Nuclear Physics B **326** (1989) 108-134
- **Link:** DOI:10.1016/0550-3213(89)90436-7
- **Status:** `ready`
- **Sections served:** Sec 2 (2.7 symplectic quantization), Sec 4 (4.5 Hilbert spaces)
- **Role:** Canonical quantization of CS, conformal blocks, boundary/WZW structure

---

## Section 2: Pedagogical Bridges and Textbooks

> Textbooks and lecture notes bridging standard QFT to topological/geometric methods.

### [09] Witten2016ThreeLecturesTopologicalPhases

- **Authors:** Witten, Edward
- **Title:** *Three Lectures on Topological Phases of Matter*
- **Venue:** Rivista del Nuovo Cimento **39** (2016) 313-370
- **Link:** [arXiv:1510.07698](https://arxiv.org/abs/1510.07698)
- **Status:** `ready`
- **Sections served:** Sec 1, Sec 5, Sec 7 (caveats)
- **Role:** Bridge from anomaly language and effective field theory to topological response; motivates condensed-matter applications

### [10] Nakahara2003GeometryTopologyPhysics

- **Authors:** Nakahara, Mikio
- **Title:** *Geometry, Topology and Physics*
- **Venue:** CRC Press / Taylor & Francis, 2nd ed. (2003)
- **Link:** —
- **Status:** `in-bib-incomplete` (TODO: confirm preferred edition)
- **Sections served:** Sec 2 (2.3 bundles, 2.4 characteristic classes, 2.5 homotopy), Sec 3
- **Role:** Standard mathematical reference for bundles, characteristic classes, and homotopy

### [11] BaezMuniain1994GaugeFieldsKnotsGravity

- **Authors:** Baez, John; Muniain, Javier P.
- **Title:** *Gauge Fields, Knots and Gravity*
- **Venue:** (1994)
- **Link:** —
- **Status:** `in-bib-incomplete` (TODO: confirm edition/publisher)
- **Sections served:** Sec 2 (2.5 homotopy, 2.6 holonomy), Sec 4
- **Role:** Most readable source for geometry underlying CS and knot observables

### [12] TongQuantumHallLectures

- **Authors:** Tong, David
- **Title:** *Lectures on the Quantum Hall Effect*
- **Venue:** arXiv:1606.06687 (2016)
- **Link:** [arXiv:1606.06687](https://arxiv.org/abs/1606.06687)
- **Status:** `ready`
- **Sections served:** Sec 5 (5.1 Hall response, 5.2 fractional charge)
- **Role:** Pedagogical calculation source for Hall response, charge/statistics, and torus degeneracy

### [13] Schwartz2014QFT

- **Authors:** Schwartz, Matthew D.
- **Title:** *Quantum Field Theory and the Standard Model*
- **Venue:** Cambridge University Press (2014)
- **Link:** —
- **Status:** `not-in-bib` (cited in plan_of_attack.tex only)
- **Sections served:** Sec 1 (reader baseline), Sec 3 (Chapter 30 chiral anomaly)
- **Role:** Reader baseline; the paper assumes familiarity through Chapter 30

---

## Section 3: Chern-Simons Theory, Boundary, and Anomaly Inflow

> Classical CS theory, anomaly inflow, massive gauge fields, and boundary CFT. Sources from the CS literature expansion pass.

### [14] Freed1995ClassicalCSNotes

- **Authors:** Freed, Daniel S.
- **Title:** *Classical Chern-Simons Theory, Part 1*
- **Venue:** arXiv:hep-th/9206021
- **Link:** [arXiv:hep-th/9206021](https://arxiv.org/abs/hep-th/9206021)
- **Status:** `not-in-bib`
- **Sections served:** Sec 3 (3.4 CS action, global normalization), Sec 4 (invertible TQFTs)
- **Role:** Geometric meaning of the classical CS action, line bundles, global normalization issues

### [15] MooreTASICSNotes

- **Authors:** Moore, Gregory
- **Title:** *Introduction to Chern-Simons Theories*
- **Venue:** Rutgers TASI notes
- **Link:** [PDF](https://www.physics.rutgers.edu/~gmoore/TASI-ChernSimons-StudentNotes.pdf)
- **Status:** `not-in-bib`
- **Sections served:** Sec 3 (3.3 anomaly descent), Sec 4 (4.4 Wilson loops, framing)
- **Role:** Main pedagogical bridge for descent, canonical quantization, Wilson loops, and framing

### [16] CallanHarvey1985AnomalyInflow

- **Authors:** Callan, Curtis G.; Harvey, Jeffrey A.
- **Title:** *Anomalies and Fermion Zero Modes on Strings and Domain Walls*
- **Venue:** Nuclear Physics B **250** (1985) 427-436
- **Link:** DOI:10.1016/0550-3213(85)90489-4
- **Status:** `not-in-bib`
- **Sections served:** Sec 5 (5.3 anomaly inflow), Sec 7
- **Role:** Original anomaly inflow mechanism; framing for bulk-boundary correspondence

### [17] DeserJackiwTempleton1982MaxwellCS

- **Authors:** Deser, S.; Jackiw, R.; Templeton, S.
- **Title:** *Topologically Massive Gauge Theories*
- **Venue:** Annals of Physics **140** (1982) 372-411
- **Link:** DOI:10.1016/0003-4916(82)90164-6
- **Status:** `not-in-bib`
- **Sections served:** Sec 5 (5.5 Maxwell-Chern-Simons contrast)
- **Role:** Maxwell-CS contrast: how to distinguish genuine TQFT from "CS term added to dynamical gauge theory"

### [18] ChernSimons1974CharacteristicForms

- **Authors:** Chern, S.-S.; Simons, J.
- **Title:** *Characteristic Forms and Geometric Invariants*
- **Venue:** Annals of Mathematics **99** (1974) 48-69
- **Link:** DOI:10.2307/1971013
- **Status:** `not-in-bib`
- **Sections served:** Sec 3 (3.3 transgression forms)
- **Role:** Original source for transgression forms and the identity d CS_3 = tr(F wedge F)

---

## Section 4: Fractional Quantum Hall Effect — Theory

> Effective field theory, topological order, K-matrix, ground-state degeneracy, edge modes.

### [19] Wen1990TopologicalOrders

- **Authors:** Wen, X.-G.
- **Title:** *Topological Orders in Rigid States*
- **Venue:** International Journal of Modern Physics B **4** (1990) 239-271
- **Link:** —
- **Status:** `ready`
- **Sections served:** Sec 5 (5.3 edge modes, degeneracy)
- **Role:** Early formulation of topological order

### [20] Wen1995TopologicalOrdersEdgeExcitations

- **Authors:** Wen, X.-G.
- **Title:** *Topological Orders and Edge Excitations in Fractional Quantum Hall States*
- **Venue:** Advances in Physics **44** (1995) 405-473
- **Link:** [arXiv:cond-mat/9506066](https://arxiv.org/abs/cond-mat/9506066)
- **Status:** `ready`
- **Sections served:** Sec 1, Sec 5 (backbone), Sec 7 (caveats)
- **Role:** Best single source for bulk-edge logic, effective CS description, and what is experimentally measurable

### [21] Wen2019ChoreographedEntanglementDances

- **Authors:** Wen, X.-G.
- **Title:** *Choreographed Entanglement Dances: Topological States of Quantum Matter*
- **Venue:** Science **363** (2019) eaal3099
- **Link:** —
- **Status:** `ready`
- **Sections served:** Sec 5
- **Role:** High-level modern review of topological order

### [22] Laughlin1983AnomalousQHE

- **Authors:** Laughlin, R. B.
- **Title:** *Anomalous Quantum Hall Effect: An Incompressible Quantum Fluid with Fractionally Charged Excitations*
- **Venue:** Physical Review Letters **50** (1983) 1395-1398
- **Link:** DOI:10.1103/PhysRevLett.50.1395
- **Status:** `ready`
- **Sections served:** Sec 5 (5.1 Hall response, 5.2 fractional charge)
- **Role:** Foundational wavefunction paper for FQHE

### [23] ArovasSchriefferWilczek1984FractionalStatistics

- **Authors:** Arovas, D.; Schrieffer, J. R.; Wilczek, F.
- **Title:** *Fractional Statistics and the Quantum Hall Effect*
- **Venue:** Physical Review Letters **53** (1984) 722-723
- **Link:** DOI:10.1103/PhysRevLett.53.722
- **Status:** `ready`
- **Sections served:** Sec 5 (5.2 braiding)
- **Role:** Classic derivation of fractional statistics for Laughlin quasiholes

### [24] ZhangHanssonKivelson1989FQHE

- **Authors:** Zhang, S.-C.; Hansson, T. H.; Kivelson, S.
- **Title:** *Effective-Field-Theory Model for the Fractional Quantum Hall Effect*
- **Venue:** Physical Review Letters **62** (1989) 82-85
- **Link:** DOI:10.1103/PhysRevLett.62.82
- **Status:** `ready`
- **Sections served:** Sec 5 (5.1 Hall response from CS effective theory)
- **Role:** Key CS effective-field-theory paper connecting Laughlin states to Chern-Simons

### [25] WenZee1992AbelianQHClassification

- **Authors:** Wen, X.-G.; Zee, A.
- **Title:** *Classification of Abelian Quantum Hall States and Matrix Formulation of Topological Fluids*
- **Venue:** Physical Review B **46** (1992) 2290-2301
- **Link:** DOI:10.1103/PhysRevB.46.2290
- **Status:** `ready`
- **Sections served:** Sec 5 (5.4 K-matrix theory)
- **Role:** Standard K-matrix classification reference

### [26] WenNiu1990GroundStateDegeneracy

- **Authors:** Wen, X.-G.; Niu, Q.
- **Title:** *Ground-State Degeneracy of the Fractional Quantum Hall States in the Presence of a Random Potential and on High-Genus Riemann Surfaces*
- **Venue:** Physical Review B **41** (1990) 9377-9396
- **Link:** DOI:10.1103/PhysRevB.41.9377
- **Status:** `ready`
- **Sections served:** Sec 4 (4.5 GSD on high genus), Sec 5 (5.3 degeneracy)
- **Role:** Essential for topological ground-state degeneracy

### [27] HalperinSternNederRosenow2011FractionalCharge

- **Authors:** Halperin, B. I.; Stern, A.; Neder, I.; Rosenow, B.
- **Title:** *Fractional Charge and Fractional Statistics in the Quantum Hall Effects*
- **Venue:** Physical Review B **83** (2011) 155440
- **Link:** [arXiv:2102.08998](https://arxiv.org/abs/2102.08998) (note: arXiv date ordering is anomalous — confirm)
- **Status:** `ready`
- **Sections served:** Sec 5 (5.2 fractional charge)
- **Role:** Review of what "fractional charge" and "fractional statistics" mean operationally

### [28] Stern2008AnyonsQHEReview

- **Authors:** Stern, Ady
- **Title:** *Anyons and the Quantum Hall Effect — A Pedagogical Review*
- **Venue:** Annals of Physics **323** (2008) 204-249
- **Link:** [arXiv:0711.4697](https://arxiv.org/abs/0711.4697)
- **Status:** `ready`
- **Sections served:** Sec 1, Sec 5 (backbone review), Sec 7 (caveats)
- **Role:** Best source for a narrative organized around observables; main pedagogical review for anyons and QHE

---

## Section 5: FQHE and Anyon Experiments

> Interferometry, fractional charge, braiding statistics measurements.

### [29] TsuiStormerGossard1982FQHEDiscovery

- **Authors:** Tsui, D. C.; Stormer, H. L.; Gossard, A. C.
- **Title:** *Two-Dimensional Magnetotransport in the Extreme Quantum Limit*
- **Venue:** Physical Review Letters **48** (1982) 1559-1562
- **Link:** DOI:10.1103/PhysRevLett.48.1559
- **Status:** `ready`
- **Sections served:** Sec 5 (5.1)
- **Role:** Discovery of the fractional quantum Hall effect

### [30] Saminadayar1997FractionalCharge

- **Authors:** Saminadayar, L.; Glattli, D. C.; Jin, Y.; Etienne, B.
- **Title:** *Observation of the e/3 Fractionally Charged Laughlin Quasiparticle*
- **Venue:** Physical Review Letters **79** (1997) 2526-2529
- **Link:** DOI:10.1103/PhysRevLett.79.2526
- **Status:** `ready`
- **Sections served:** Sec 5 (5.2)
- **Role:** Classic fractional-charge shot-noise experiment

### [31] dePicciotto1997FractionalCharge

- **Authors:** de-Picciotto, R. et al.
- **Title:** *Direct Observation of a Fractional Charge*
- **Venue:** Nature **389** (1997) 162-164
- **Link:** DOI:10.1038/38241
- **Status:** `ready`
- **Sections served:** Sec 5 (5.2)
- **Role:** Another classic fractional-charge measurement

### [32] CaminoZhouGoldman2005ABSuperperiod

- **Authors:** Camino, F. E.; Zhou, W.; Goldman, V. J.
- **Title:** *Aharonov-Bohm Superperiod in a Laughlin Quasiparticle Interferometer*
- **Venue:** Physical Review Letters **95** (2005) 246802
- **Link:** DOI:10.1103/PhysRevLett.95.246802
- **Status:** `ready`
- **Sections served:** Sec 5 (5.2, 5.6 caveats)
- **Role:** Important interferometric precursor; early anyonic phase measurement

### [33] Nakamura2020AnyonicBraiding

- **Authors:** Nakamura, M. et al.
- **Title:** *Direct Observation of Anyonic Braiding Statistics*
- **Venue:** Nature Physics **16** (2020) 931-936
- **Link:** DOI:10.1038/s41567-020-1019-1
- **Status:** `ready`
- **Sections served:** Sec 5 (5.2 braiding evidence)
- **Role:** Major modern anyon-interferometry result at nu=1/3; confirms CS Wilson-loop prediction

### [34] Bartolomei2020AnyonCollisions

- **Authors:** Bartolomei, J. et al.
- **Title:** *Fractional Statistics in Anyon Collisions*
- **Venue:** Science **368** (2020) 173-177
- **Link:** DOI:10.1126/science.aaz5601
- **Status:** `ready`
- **Sections served:** Sec 5 (5.2)
- **Role:** Noise/collider-style evidence for anyonic statistics

### [35] VenkatachalamHartPfeifferWestYacobyGrapheneInterferometers

- **Authors:** Venkatachalam, V.; Hart, S.; Pfeiffer, L.; West, K. W.; Yacoby, A.
- **Title:** *Localized Electronic States in the Quantum Hall Regime and Discrete Charging in Graphene Interferometers*
- **Venue:** (TODO: add canonical venue, volume, pages, year)
- **Link:** —
- **Status:** `in-bib-incomplete` (needs venue, volume, pages, year)
- **Sections served:** Sec 5 (5.6 caveats)
- **Role:** Real experimental complications around interferometry

### [36] Werkmeister2024GrapheneInterferometer

- **Authors:** Werkmeister, S. et al.
- **Title:** *(Graphene interferometer braiding result)*
- **Venue:** (2024)
- **Link:** (TODO: confirm arXiv/DOI)
- **Status:** `not-in-bib`
- **Sections served:** Sec 5 (experimental evidence)
- **Role:** Graphene-based interferometer improvements and specific braiding claims

### [37] Andersen2023NonAbelianBraiding

- **Authors:** Andersen, T. I. et al.
- **Title:** *Non-Abelian braiding of graph vertices in a superconducting processor*
- **Venue:** (2023)
- **Link:** [arXiv:2210.10255](https://arxiv.org/abs/2210.10255)
- **Status:** `not-in-bib`
- **Sections served:** Sec 5 or Sec 7 (requires honesty box: synthetic emulation, not natural phase)
- **Role:** Non-abelian braiding on quantum hardware; must be framed as synthetic emulation

### [38] RosenowHalperinInterferometryPlaceholder

- **Authors:** Rosenow, A.; Halperin, B. I. et al.
- **Title:** *(QH interferometry / Coulomb-dominated regime)*
- **Venue:** —
- **Link:** —
- **Status:** `placeholder`
- **Sections served:** Sec 5 (5.6 caveats)
- **Role:** Coulomb-dominated regime complications for clean TQFT interpretation of interferometry

---

## Section 6: Non-Abelian Anyons and Topological Quantum Computation

> Non-abelian braiding, TQC, topological entanglement entropy, experimental braiding.

### [39] NayakSimonSternFreedmanDasSarma2008NonabelianAnyons

- **Authors:** Nayak, Chetan; Simon, Steven H.; Stern, Ady; Freedman, Michael; Das Sarma, Sankar
- **Title:** *Non-Abelian Anyons and Topological Quantum Computation*
- **Venue:** Reviews of Modern Physics **80** (2008) 1083-1159
- **Link:** [arXiv:0707.1889](https://arxiv.org/abs/0707.1889)
- **Status:** `ready`
- **Sections served:** Sec 1, Sec 5 (5.4 nonabelian states), Sec 7 (outlook)
- **Role:** Main review for nonabelian anyons, interferometry, and why braiding is the right observable

### [40] HalperinJain2020FQHENewDevelopments

- **Authors:** Halperin, B. I.; Jain, J. K. (eds.)
- **Title:** *Fractional Quantum Hall Effects: New Developments*
- **Venue:** World Scientific (2020)
- **Link:** —
- **Status:** `in-bib-incomplete` (TODO: add full volume metadata)
- **Sections served:** Sec 5
- **Role:** Sourcebook for modern experimental and theoretical FQHE directions

### [41] Kitaev2003FaultTolerant

- **Authors:** Kitaev, Alexei
- **Title:** *Fault-Tolerant Quantum Computation by Anyons*
- **Venue:** Annals of Physics **303** (2003) 2-30
- **Link:** [arXiv:quant-ph/9707021](https://arxiv.org/abs/quant-ph/9707021)
- **Status:** `not-in-bib`
- **Sections served:** Sec 5 (nonabelian states), Sec 7 (outlook on TQC)
- **Role:** Original anyonic quantum computation proposal; topological protection from local noise

### [42] KitaevPreskill2006TEE

- **Authors:** Kitaev, Alexei; Preskill, John
- **Title:** *Topological Entanglement Entropy*
- **Venue:** Physical Review Letters **96** (2006) 110404
- **Link:** [arXiv:hep-th/0510092](https://arxiv.org/abs/hep-th/0510092)
- **Status:** `not-in-bib`
- **Sections served:** Sec 5 (topological order diagnostics)
- **Role:** Topological entanglement entropy as a diagnostic for topological order

### [43] LevinWen2006DetectingTO

- **Authors:** Levin, Michael; Wen, Xiao-Gang
- **Title:** *Detecting Topological Order in a Ground State Wave Function*
- **Venue:** Physical Review Letters **96** (2006) 110405
- **Link:** [arXiv:cond-mat/0510613](https://arxiv.org/abs/cond-mat/0510613)
- **Status:** `not-in-bib`
- **Sections served:** Sec 5 (topological order diagnostics)
- **Role:** Alternative TEE formulation for detecting topological order

---

## Section 7: QCD Topology, Strong CP, and Axions

> Instantons, theta vacua, topological susceptibility, Witten-Veneziano, neutron EDM, axion searches.

### [44] tHooft1976BellJackiw

- **Authors:** 't Hooft, G.
- **Title:** *Symmetry Breaking Through Bell-Jackiw Anomalies*
- **Venue:** Physical Review Letters **37** (1976) 8-11
- **Link:** DOI:10.1103/PhysRevLett.37.8
- **Status:** `ready`
- **Sections served:** Sec 3 (3.1 anomalies), Sec 6 (6.1 theta vacua)
- **Role:** Fundamental anomaly/instanton reference

### [45] tHooft1976Pseudoparticle

- **Authors:** 't Hooft, G.
- **Title:** *Computation of the Quantum Effects Due to a Four-Dimensional Pseudoparticle*
- **Venue:** Physical Review D **14** (1976) 3432-3450
- **Link:** DOI:10.1103/PhysRevD.14.3432
- **Status:** `ready`
- **Sections served:** Sec 3 (3.2 instantons), Sec 6 (6.1)
- **Role:** Classic instanton paper

### [46] Witten1979U1GoldstoneBoson

- **Authors:** Witten, Edward
- **Title:** *Current Algebra Theorems for the U(1) "Goldstone Boson"*
- **Venue:** Nuclear Physics B **156** (1979) 269-283
- **Link:** DOI:10.1016/0550-3213(79)90031-2
- **Status:** `ready`
- **Sections served:** Sec 6 (6.2 Witten-Veneziano formula)
- **Role:** One half of the Witten-Veneziano mechanism: U(1)_A and the would-be Goldstone boson

### [47] Veneziano1979U1WithoutInstantons

- **Authors:** Veneziano, G.
- **Title:** *U(1) Without Instantons*
- **Venue:** Nuclear Physics B **159** (1979) 213-224
- **Link:** DOI:10.1016/0550-3213(79)90332-8
- **Status:** `ready`
- **Sections served:** Sec 6 (6.2)
- **Role:** Other half of Witten-Veneziano: large-N resolution of the U(1)_A problem

### [48] DiVecchiaVeneziano1980ChiralDynamics

- **Authors:** Di Vecchia, P.; Veneziano, G.
- **Title:** *Chiral Dynamics in the Large-N Limit*
- **Venue:** Nuclear Physics B **171** (1980) 253-272
- **Link:** DOI:10.1016/0550-3213(80)90370-3
- **Status:** `ready`
- **Sections served:** Sec 6 (6.1 vacuum energy vs theta)
- **Role:** Effective chiral Lagrangian treatment of theta-dependence; standard for E(theta) formula

### [49] Dine2000TASIStrongCP

- **Authors:** Dine, Michael
- **Title:** *TASI Lectures on the Strong CP Problem*
- **Venue:** arXiv:hep-ph/0011376
- **Link:** [arXiv:hep-ph/0011376](https://arxiv.org/abs/hep-ph/0011376)
- **Status:** `ready`
- **Sections served:** Sec 6 (6.3 strong CP)
- **Role:** Classic introduction to theta, strong CP, and axions

### [50] Hook2018TASIStrongCPAxions

- **Authors:** Hook, Anson
- **Title:** *TASI Lectures on the Strong CP Problem and Axions*
- **Venue:** PoS TASI2018 004 (2019)
- **Link:** [arXiv:1812.02669](https://arxiv.org/abs/1812.02669)
- **Status:** `ready`
- **Sections served:** Sec 6 (6.3 axion)
- **Role:** Best modern pedagogical source for strong CP and axions for a QFT reader

### [51] Marsh2016AxionCosmology

- **Authors:** Marsh, David J. E.
- **Title:** *Axion Cosmology*
- **Venue:** Physics Reports **643** (2016) 1-79
- **Link:** [arXiv:1510.07633](https://arxiv.org/abs/1510.07633)
- **Status:** `ready`
- **Sections served:** Sec 6 (6.3 axion phenomenology)
- **Role:** Standard broad review of axion phenomenology; mass-coupling plane, detection classes

### [52] Teper2000TopologyInQCD

- **Authors:** Teper, Mike
- **Title:** *Topology in QCD*
- **Venue:** Nuclear Physics B -- Proceedings Supplements **83** (2000) 146-150
- **Link:** [arXiv:hep-lat/9909124](https://arxiv.org/abs/hep-lat/9909124)
- **Status:** `ready`
- **Sections served:** Sec 6 (6.1 topological susceptibility)
- **Role:** Older review on susceptibility, eta', and lattice topology

### [53] CichyLatticeWittenVeneziano

- **Authors:** Cichy, K. et al.
- **Title:** *Non-perturbative Test of the Witten-Veneziano Formula from Lattice QCD*
- **Venue:** JHEP **09** (2015) 020
- **Link:** [arXiv:1504.07954](https://arxiv.org/abs/1504.07954)
- **Status:** `ready`
- **Sections served:** Sec 6 (6.2 lattice support for WV)
- **Role:** Lattice confirmation of Witten-Veneziano; connects topological susceptibility to eta' mass

### [54] AreanU1AHolographicQCD

- **Authors:** Arean, D. et al.
- **Title:** *U(1)_A axial anomaly, eta', and topological susceptibility in holographic QCD*
- **Venue:** arXiv:2105.00923 (2021)
- **Link:** [arXiv:2105.00923](https://arxiv.org/abs/2105.00923)
- **Status:** `ready`
- **Sections served:** Sec 6 (6.2)
- **Role:** Modern holographic perspective on topological susceptibility

### [55] Abel2020NeutronEDM

- **Authors:** Abel, C. et al. (nEDM Collaboration)
- **Title:** *Measurement of the Permanent Electric Dipole Moment of the Neutron*
- **Venue:** Physical Review Letters **124** (2020) 081803
- **Link:** DOI:10.1103/PhysRevLett.124.081803
- **Status:** `ready`
- **Sections served:** Sec 6 (6.3 nEDM bound)
- **Role:** Current world-limit paper for neutron EDM; constrains |theta-bar| < 10^{-10}

### [56] ADMXOverviewPlaceholder

- **Authors:** ADMX Collaboration
- **Title:** *(ADMX haloscope overview or flagship result)*
- **Venue:** —
- **Link:** —
- **Status:** `placeholder`
- **Sections served:** Sec 6 (6.3 axion experiments)
- **Role:** Haloscope phenomenology and realistic axion detection language

### [57] CASTIAXOOverviewPlaceholder

- **Title:** *(CAST / IAXO helioscope overview)*
- **Venue:** —
- **Link:** —
- **Status:** `placeholder`
- **Sections served:** Sec 6 (6.3)
- **Role:** Helioscope observables for axion searches

### [58] CASPErOverviewPlaceholder

- **Title:** *(CASPEr spin-precession proposal/overview)*
- **Venue:** —
- **Link:** —
- **Status:** `placeholder`
- **Sections served:** Sec 6 (6.3)
- **Role:** Spin-precession axion search observables

### [59] MADMAXOverviewPlaceholder

- **Title:** *(MADMAX dielectric haloscope overview)*
- **Venue:** —
- **Link:** —
- **Status:** `placeholder`
- **Sections served:** Sec 6 (6.3)
- **Role:** Dielectric-haloscope axion search observables

---

## Section 8: Monopoles, Defects, and Solitons

> Dirac quantization, 't Hooft-Polyakov monopoles, topological solitons, experimental searches.

### [60] Dirac1931QuantisedSingularities

- **Authors:** Dirac, P. A. M.
- **Title:** *Quantised Singularities in the Electromagnetic Field*
- **Venue:** Proceedings of the Royal Society A **133** (1931) 60-72
- **Link:** DOI:10.1098/rspa.1931.0130
- **Status:** `ready`
- **Sections served:** Sec 7 (7.1 monopoles)
- **Role:** Foundational charge quantization as topological consistency condition

### [61] tHooft1974MagneticMonopoles

- **Authors:** 't Hooft, G.
- **Title:** *Magnetic Monopoles in Unified Gauge Theories*
- **Venue:** Nuclear Physics B **79** (1974) 276-284
- **Link:** DOI:10.1016/0550-3213(74)90486-6
- **Status:** `ready`
- **Sections served:** Sec 7 (7.1)
- **Role:** Foundational nonabelian monopole paper

### [62] Polyakov1974ParticleSpectrum

- **Authors:** Polyakov, A. M.
- **Title:** *Particle Spectrum in Quantum Field Theory*
- **Venue:** JETP Letters **20** (1974) 194-195
- **Link:** —
- **Status:** `ready`
- **Sections served:** Sec 7 (7.1)
- **Role:** Foundational finite-energy soliton paper; smooth monopole solutions

### [63] MantonSutcliffeTopologicalSolitons

- **Authors:** Manton, N. S.; Sutcliffe, P.
- **Title:** *Topological Solitons*
- **Venue:** (TODO: add publisher and year)
- **Link:** —
- **Status:** `in-bib-incomplete`
- **Sections served:** Sec 2 (2.7 moduli spaces), Sec 7 (7.1 monopoles)
- **Role:** Best broad reference text on monopoles, skyrmions, vortices; soliton moduli-space logic

### [64] ShnirMagneticMonopoles

- **Authors:** Shnir, Y. M.
- **Title:** *Magnetic Monopoles*
- **Venue:** (TODO: add publisher and year)
- **Link:** —
- **Status:** `in-bib-incomplete`
- **Sections served:** Sec 7 (7.1)
- **Role:** Standard monopole monograph

### [65] WeinbergClassicalSolutionsQFT

- **Authors:** Weinberg, E. J.
- **Title:** *Classical Solutions in Quantum Field Theory*
- **Venue:** (TODO: add publisher and year)
- **Link:** —
- **Status:** `in-bib-incomplete`
- **Sections served:** Sec 2, Sec 7 (7.1)
- **Role:** Monopoles, instantons, and soliton moduli-space logic

### [66] Rajantie2024MonopoleTheoryOverview

- **Authors:** Rajantie, Arttu
- **Title:** *Magnetic Monopoles -- Theory Overview*
- **Venue:** arXiv:2411.05753 (2024)
- **Link:** [arXiv:2411.05753](https://arxiv.org/abs/2411.05753)
- **Status:** `ready`
- **Sections served:** Sec 7 (7.1)
- **Role:** Concise modern monopole review emphasizing physical viewpoint and experimental relevance

### [67] FairbairnMonopolesRevisited

- **Authors:** Fairbairn, M.; Douza, T.; Ellis, J. et al.
- **Title:** *Magnetic Monopoles Revisited: Models and Searches at Colliders and in the Cosmos*
- **Venue:** Physics Reports **942** (2021) 1-50
- **Link:** [arXiv:2005.05100](https://arxiv.org/abs/2005.05100)
- **Status:** `ready`
- **Sections served:** Sec 7 (7.1)
- **Role:** Best modern bridge between monopole theory and experiment

### [68] PDGMagneticMonopolesPlaceholder

- **Title:** *(PDG Magnetic Monopoles review, specific edition)*
- **Venue:** —
- **Link:** —
- **Status:** `placeholder`
- **Sections served:** Sec 7 (7.1)
- **Role:** Experimental monopole search status

---

## Section 9: Line Operators and Generalized Symmetries

> Wilson/'t Hooft lines, generalized symmetries, SymTFT, confinement diagnostics.

### [69] GaiottoKapustinSeibergWillett2015GeneralizedSymmetries

- **Authors:** Gaiotto, Davide; Kapustin, Anton; Seiberg, Nathan; Willett, Brian
- **Title:** *Generalized Global Symmetries*
- **Venue:** JHEP **02** (2015) 172
- **Link:** [arXiv:1412.5148](https://arxiv.org/abs/1412.5148)
- **Status:** `ready`
- **Sections served:** Sec 7 (7.1 line operators, generalized symmetries)
- **Role:** Foundational paper connecting Wilson/'t Hooft lines to modern symmetry language

### [70] KapustinWitten2007ElectricMagneticLanglands

- **Authors:** Kapustin, Anton; Witten, Edward
- **Title:** *Electric-Magnetic Duality and the Geometric Langlands Program*
- **Venue:** Communications in Number Theory and Physics **1** (2007) 1-236
- **Link:** [arXiv:hep-th/0604151](https://arxiv.org/abs/hep-th/0604151)
- **Status:** `ready`
- **Sections served:** Sec 7 (7.3 outlook — advanced pointer only)
- **Role:** Advanced outlook pointer for electric-magnetic duality and Langlands program

### [71] KapustinSaulinaLineOperatorsPlaceholder

- **Authors:** Kapustin, A.; Saulina, N.
- **Title:** *(Specific line/surface operator paper)*
- **Venue:** —
- **Link:** —
- **Status:** `placeholder`
- **Sections served:** Sec 7 (7.1)
- **Role:** Modern global-symmetry/operator perspective on Wilson/'t Hooft lines

### [72] FreedMooreTeleman2024TopologicalSymmetry

- **Authors:** Freed, Daniel S.; Moore, Gregory; Teleman, Constantin
- **Title:** *Topological Symmetry in Field Theory*
- **Venue:** (2024)
- **Link:** (TODO: confirm arXiv ID)
- **Status:** `not-in-bib`
- **Sections served:** Sec 7 (7.3 outlook, SymTFT pointer)
- **Role:** Topological symmetry perspective; used in outlook and generalized-symmetry context

### [73] Bhardwaj2023GeneralizedSymmetryLectures

- **Authors:** Bhardwaj, L. et al.
- **Title:** *Lectures on Generalized Symmetries*
- **Venue:** (2023)
- **Link:** (TODO: confirm arXiv ID)
- **Status:** `not-in-bib`
- **Sections served:** Sec 7 (generalized symmetries context)
- **Role:** Pedagogical lectures on generalized symmetries; cited in Ch 8 context and outlook

---

## Section 10: 2D TQFT, Frobenius Algebras, and Classification

> 2D TQFT classification theorem, cobordism generators, Frobenius algebra structure. (Note: these served the now-cut BSIEW Ch 4, but may still appear in Sec 4.2 of the current structure.)

### [74] Kock2004FrobeniusAlgebras2DTQFT

- **Authors:** Kock, Joachim
- **Title:** *Frobenius Algebras and 2D Topological Quantum Field Theories*
- **Venue:** Cambridge University Press (2004)
- **Link:** —
- **Status:** `not-in-bib`
- **Sections served:** Sec 4 (4.2 TQFT classes, if Frobenius example retained)
- **Role:** Standard reference for 2D TQFT classification; pair-of-pants generators and Frobenius axioms

### [75] DijkgraafWitten1990TwistedGauge

- **Authors:** Dijkgraaf, R.; Witten, E.
- **Title:** *Topological Gauge Theories and Group Cohomology*
- **Venue:** Communications in Mathematical Physics **129** (1990) 393-429
- **Link:** DOI:10.1007/BF02096988
- **Status:** `not-in-bib`
- **Sections served:** Sec 4 (4.2 TQFT classes, DW example)
- **Role:** Twisted finite-group gauge theories; group cohomology classifies actions

---

## Section 11: Spin Structure and Level Quantization

> Spin/non-spin refinements, global normalization, level quantization subtleties.

### [76] SeibergWitten2016Spin

- **Authors:** Seiberg, Nathan; Witten, Edward
- **Title:** *(Spin structure and level quantization refinement)*
- **Venue:** (2016)
- **Link:** (TODO: confirm exact paper — may be Gapped Boundary Phases of TQFTs, arXiv:1602.04251)
- **Status:** `not-in-bib`
- **Sections served:** Sec 3 (3.5 level quantization caveat paragraph)
- **Role:** Why level quantization is integer vs. half-integer; spin structure subtlety

---

## Appendix A: Placeholder Resolution Tracker

These 7 BibTeX stubs exist as `@misc{...Placeholder}` entries and need canonical papers identified.

| # | Placeholder key | Needs | Paper section | Guidance for lit search |
|---|----------------|-------|---------------|------------------------|
| 1 | `RosenowHalperinInterferometryPlaceholder` | 1-2 concrete QH interferometry / Coulomb-dominated regime papers | Sec 5 (5.6 caveats) | Look for Rosenow, Halperin, Stern papers on Coulomb blockade effects in FQH interferometers |
| 2 | `ADMXOverviewPlaceholder` | ADMX flagship experimental result or collaboration review | Sec 6 (6.3 axion) | ADMX Gen2 results or ADMX collaboration review paper |
| 3 | `CASTIAXOOverviewPlaceholder` | CAST results paper and/or IAXO design/status paper | Sec 6 (6.3 axion) | CAST collaboration final results; IAXO technical design report |
| 4 | `CASPErOverviewPlaceholder` | CASPEr proposal or status paper | Sec 6 (6.3 axion) | Budker et al. CASPEr proposal paper |
| 5 | `MADMAXOverviewPlaceholder` | MADMAX design or status paper | Sec 6 (6.3 axion) | MADMAX collaboration design report |
| 6 | `PDGMagneticMonopolesPlaceholder` | Specific PDG edition of Magnetic Monopoles review | Sec 7 (7.1 defects) | PDG Review of Particle Physics, Magnetic Monopoles chapter, most recent edition |
| 7 | `KapustinSaulinaLineOperatorsPlaceholder` | Specific Kapustin-Saulina paper on line/surface operators | Sec 7 (7.1 line operators) | Kapustin-Saulina on topological boundary conditions, surface operators in gauge theory |

---

## Appendix B: Section to Reference Cross-Index

| Paper section | Entry numbers | Key themes |
|---------------|---------------|------------|
| **Sec 1: Introduction** | 01, 02, 03, 05, 09, 13, 20, 28, 39 | Frame the problem, state the thesis, cite main reviews |
| **Sec 2: Mathematical Toolkit** | 01, 08, 10, 11, 63, 65 | Bundles, forms, homotopy, bordisms, moduli spaces |
| **Sec 3: Ordinary QFT to CS** | 03, 05, 06, 08, 10, 14, 15, 18, 44, 45 | Instantons, anomaly descent, transgression, CS action, level quantization |
| **Sec 4: TQFT and Observables** | 01, 02, 03, 04, 05, 06, 07, 08, 26, 74, 75 | Functorial definition, TQFT classes, CS observables, observable taxonomy |
| **Sec 5: Topological Response 2+1D** | 09, 12, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 40, 41, 42, 43 | FQHE, anyons, braiding, edge modes, K-matrix, experiments |
| **Sec 6: Topological Sectors 3+1D** | 44, 45, 46, 47, 48, 49, 50, 51, 52, 53, 54, 55, 56, 57, 58, 59 | Theta vacua, chi_t, eta', WV formula, nEDM, axion, experiment placeholders |
| **Sec 7: Defects, Caveats, Outlook** | 03, 05, 09, 16, 20, 28, 39, 60, 61, 62, 63, 64, 65, 66, 67, 68, 69, 70, 71, 72, 73 | Monopoles, line operators, gen symmetries, "when topological?", guide du routard |

---

## Summary Statistics

- **Total unique entries:** 76
- **Status breakdown:** 37 `ready`, 8 `in-bib-incomplete`, 7 `placeholder`, 14 `not-in-bib`
- **Entries needing .bib work:** 29 total (8 incomplete + 7 placeholder + 14 missing)
- **Entries needing canonical paper identification:** 7 (the placeholders in Appendix A)
