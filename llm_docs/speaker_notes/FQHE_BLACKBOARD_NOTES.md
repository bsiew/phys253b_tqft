---
created_at: "2026-05-05T18:13:35-04:00"
updated_at: "2026-05-05T18:13:35-04:00"
generated_by: "claude-code"
updated_by: "claude-code"
timestamp_source: hook
---
# FQHE Blackboard Talk — Prepared Lecture Notes (v2)

## Format
- **[WRITE]** = put on the board exactly as shown
- **[DRAW]** = hand-draw diagram
- **[SAY]** = spoken only (motivation, intuition, narration)
- **[BOX]** / **[UNDERLINE]** / **[CIRCLE]** = board emphasis

---

## BOARD 1: The Experiment (1.5 min)

**[DRAW]** Rectangle labeled "2DEG". ×'s inside for B into page. Arrow along long edge: I_x. Arrow perpendicular: V_y. Temperature label: T ~ 50 mK. Field label: B ~ 10 T.

**[SAY]** "Two-dimensional electron gas. GaAs/AlGaAs heterostructure — electrons confined to a plane. Strong perpendicular B-field. Cooled to millikelvin. We drive a current this way, measure the transverse voltage."

**[WRITE]**
```
σ_xy = I_x / V_y
```

**[DRAW]** Staircase plot: σ_xy (vertical) vs ν (horizontal). Flat plateaux at ν = 1, 2, 3, and fractional plateaux at ν = 1/3, 2/5, 2/3. The plateaux are FLAT — emphasize with horizontal lines.

**[WRITE]**
```
Integer:     σ_xy = n (e²/h),       n = 1, 2, 3, ...
Fractional:  σ_xy = ν (e²/h),       ν = 1/3, 2/5, 5/2, ...
```

**[SAY]** "Measured to one part in 10⁹. Does not drift with temperature, disorder, sample shape. These are the most precisely measured constants in condensed matter. Something deeply rigid is protecting them."

---

## BOARD 2: Integer QHE — Quick (1.5 min)

**[WRITE]**
```
Landau levels:   E_n = ℏω_c(n + 1/2),     ω_c = eB/m

Degeneracy/level:  N_φ = BA / (h/e) = (total flux)/(flux quantum)

Filling fraction:  ν = N_e / N_φ
```

**[DRAW]** Energy ladder: horizontal lines. Shade bottom n levels. Gap above.

**[SAY]** "Charged particle in a B-field: energy quantized into Landau levels, massively degenerate. At integer filling, you fill exactly n complete levels. Single-particle gap above. It's a band insulator. Hall conductance quantized by the Chern number of the filled bands. This is single-particle physics — no interactions required. Solved."

**[WRITE]**
```
Integer QHE: band insulator + Chern number. DONE.
```

**[SAY]** "Now. Set ν = 1/3. Everything changes."

---

## BOARD 3: Why Fractional is Hard + What Survives (2.5 min)

**[WRITE]**
```
ν = 1/m  (start with m = 3):

  N_e = N_φ / m     (lowest Landau level 1/m filled)

  All electrons in ONE Landau level:
    → single-particle energies are IDENTICAL
    → kinetic energy completely quenched
    → Coulomb interaction is the ONLY energy scale
    → no small parameter, not perturbative
```

**[SAY]** "This is the key physical point. The magnetic field has taken away the kinetic energy. Normally in a many-body problem you have kinetic energy competing with interactions and you can perturb in the ratio. Here the kinetic energy is gone — it's been absorbed into the Landau level degeneracy. Coulomb is the whole story. 10¹¹ electrons interacting with no small parameter. You can't solve it microscopically."

**[SAY]** "But Laughlin figured out something remarkable. The ground state is gapped — there's an energy gap above it, set by the Coulomb scale. And below that gap, the fluid is incompressible: no density waves, no phonons, no local order parameter."

**[WRITE]**
```
Below the gap:
  • incompressible quantum liquid
  • no local order parameter (not Landau symmetry-breaking)
  • no low-energy local modes

What survives:
  • response to external electromagnetic probes
  • braiding/exchange of localized defects
  • global topological data (genus dependence)
```

**[SAY]** "Once all local degrees of freedom are gapped out, the only remaining universal information is topological. Response, braiding, global structure. This is exactly the regime where a topological field theory is the correct effective description."

**[SAY]** "So the question becomes: what is the most general topological action I can write in 2+1 dimensions for a charged fluid?"

---

## BOARD 4: The Effective Action (2.5 min)

**[SAY]** "We need the low-energy effective action. The rules:"

**[WRITE]**
```
Rules for the effective action:
  (i)   gauge fields are 1-forms (A, a ∈ Ω¹)
  (ii)  action is ∫(3-form)   [spacetime is 2+1 dim]
  (iii) no metric (topological — can't use Hodge star ⋆)
  (iv)  gauge invariant (up to boundary terms)

Metric-free 3-forms built from 1-forms:
  A ∧ dA       ← background self-coupling
  a ∧ da       ← emergent self-coupling
  A ∧ da       ← mixed coupling (response)
```

**[SAY]** "In 2+1 dimensions, with one-form gauge fields, the only things you can write WITHOUT a metric are wedge products of the fields and their exterior derivatives. These three terms exhaust the possibilities at leading order. The action is almost forced on you."

**[WRITE]** (large, centered, clean — THE action)
```
┌─────────────────────────────────────────────────────────────┐
│                                                             │
│  S[a; A] = ∫ [ (1/2π) A ∧ da  −  (m/4π) a ∧ da ]         │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

**[SAY]** pointing at each term:
- "A is the external electromagnetic field. We put it in by hand as a probe — we don't path-integrate over it."
- "a is the emergent U(1) gauge field. It's the low-energy collective degree of freedom of the electron fluid. Same conceptual status as a phonon for a crystal — it packages the correlations."
- "This mixed term" [A∧da] "tells me how the fluid responds to electromagnetism."
- "This pure CS term" [a∧da] "gives the dynamics and the self-statistics."
- "m is an integer. Odd for fermions."

**[WRITE]** (to the side, with big ✗)
```
✗  No F ∧ ⋆F  (no Maxwell term → no propagating modes)
✗  No metric  (→ observables immune to geometry)
```

**[SAY]** "The absence of a Maxwell term means there are no propagating gauge bosons in the bulk. The absence of the metric means the action literally cannot see smooth deformations of the sample. Disorder, impurities, gentle perturbations — they cannot change the observables. Only closing the gap can. That's the protection mechanism."

---

## BOARD 5: Derivation — Hall Conductance (3 min)

**[WRITE]**
```
═══════════════════════════════════
  DERIVATION 1: Hall conductance
═══════════════════════════════════
```

**[SAY]** "We integrate out the dynamical field a. Vary with respect to a:"

**[WRITE]**
```
δS/δa = 0:

  (1/2π) dA  −  (m/2π) da  =  0
```

**[SAY]** "This is algebraic — a is determined on-shell by A."

**[WRITE]**
```
  da = (1/m) dA

On simply-connected patch:
  a = (1/m) A
```

**[SAY]** "Plug back into the action. Both terms contribute."

**[WRITE]**
```
S_eff[A] = (1/2π) ∫ A ∧ d(A/m)  −  (m/4π) ∫ (A/m) ∧ d(A/m)

         = (1/2πm) ∫ A ∧ dA  −  (1/4πm) ∫ A ∧ dA

         = (1/4πm) ∫ A ∧ dA
```

**[BOX]** the final line.

**[SAY]** "This is a pure Chern-Simons term for the electromagnetic background at level 1/m. It's the generating functional for the electromagnetic response."

**[WRITE]**
```
Current:
  j^μ = δS_eff / δA_μ = (1/2πm) ε^{μνρ} ∂_ν A_ρ

Components:
  j⁰ = (1/2πm) B         ← charge density ~ magnetic field
  j^i = (1/2πm) ε^{ij} E_j   ← Hall current
```

**[SAY]** "The first equation says charge density is proportional to B — that's the Streda formula. The second says current is perpendicular to E-field — that's a Hall current."

**[WRITE]** (large, boxed)
```
┌────────────────────────────────────────────┐
│  σ_xy = 1/(2πm)                            │
│                                            │
│  Restoring e, ℏ:   σ_xy = (1/m)(e²/h)    │
└────────────────────────────────────────────┘
```

**[SAY]** "For m=3: σ_xy = (1/3)(e²/h). First universal number derived."

**[SAY]** "Now. Why must m be an integer? This is the level quantization argument."

**[WRITE]**
```
Level quantization:

  Place theory on S² × S¹.
  Thread 1 magnetic flux quantum through S²:
    (1/2π) ∫_{S²} dA = 1

  Large gauge transformation of a, winding once around S¹:
    a₀ → a₀ + 2π/β    (β = length of S¹)

  Action shifts:
    ΔS = (m/4π) · 2π · (2π · 1) / (2π) = ... 

  More directly: gauge transf on S³ changes S_CS by
    ΔS = 2πm · (winding number)

  e^{iS} single-valued  ⟹  m ∈ ℤ
```

**[SAY]** "The same argument you've seen for any Chern-Simons theory: large gauge invariance forces the coefficient to be an integer. For fermions, m must be odd. The quantization of Hall conductance is not a fit — it's a consistency condition of the quantum theory."

---

## BOARD 6: Derivation — Fractional Charge (2.5 min)

**[WRITE]**
```
═══════════════════════════════════
  DERIVATION 2: Quasihole charge
═══════════════════════════════════
```

**[SAY]** "What are the excitations? A quasihole is a localized defect in the incompressible fluid. In the effective theory, it's the endpoint of a Wilson line of the emergent gauge field a."

**[WRITE]**
```
Wilson line:  W(C) = exp(i ∫_C a)

  → worldline of a particle carrying unit a-charge.
  → endpoint = localized source for a.
```

**[SAY]** "Same reason exp(ie∫A) is the worldline of an electron in QED. A Wilson line endpoint is where Gauss's law sees a source."

**[WRITE]**
```
Static quasihole at x₀:

  Source: S_source = ∫ a ∧ J,    J = 2π δ²(x − x₀) dt

EOM for a with source:

  (m/2π) ε^{μνρ} ∂_ν a_ρ = δ²(x − x₀) δ^μ₀

Spatial (μ=0) component:

  (m/2π) f₁₂(x) = δ²(x − x₀)
```

**[WRITE]**
```
  m f₁₂ = 2π δ²(x − x₀)

  ⟹ ∫ f₁₂ d²x = 2π/m     (emergent flux bound to quasihole)
```

**[DRAW]** Dot at x₀ with concentric circles indicating flux. Label: "Φ_a = 2π/m"

**[SAY]** "Each quasihole is a charge-flux composite of the emergent field: it carries unit a-charge AND it binds 2π/m units of a-flux. This is flux attachment — the field-theoretic version of the Jastrow factor in Laughlin's wavefunction."

**[SAY]** "Now convert to electric charge. The mixed term A∧da is what couples the emergent field to electromagnetism."

**[WRITE]**
```
Charge density (vary S w.r.t. A₀):

  j⁰ = (1/2π) f₁₂

Electric charge of quasihole:

  Q = e ∫ j⁰ d²x = (e/2π) ∫ f₁₂ d²x = (e/2π) · (2π/m)
```

**[WRITE]** (boxed)
```
┌──────────────────┐
│   Q_qh = e/m    │
└──────────────────┘
```

**[SAY]** "For m=3: charge e/3. The electron hasn't split. The CS coupling has redistributed charge: a-flux → electric charge through the mixed term. Same m, second observable."

**[SAY]** "Measured directly: shot-noise experiments by Saminadayar and by de-Picciotto, both in 1997. They measure the Fano factor of tunneling current and extract the carrier charge."

---

## BOARD 7: Derivation — Anyonic Statistics (3 min)

**[WRITE]**
```
═══════════════════════════════════════
  DERIVATION 3: Exchange statistics
═══════════════════════════════════════
```

**[SAY]** "Each quasihole is both an a-charge and an a-flux. When one goes around another, there's an Aharonov-Bohm phase."

**[DRAW]** Two quasiholes. Label each: "q = 1 (a-charge), Φ = 2π/m (a-flux)". Draw one looping around the other with an arrow showing direction.

**[WRITE]**
```
Quasihole 1: charge q₁ = 1 under a
Quasihole 2: carries a-flux Φ₂ = 2π/m

Full braid (1 goes around 2):

  φ_braid = q₁ · Φ₂ = 1 · (2π/m) = 2π/m
```

**[SAY]** "That's the Aharonov-Bohm effect. Charge times enclosed flux. Nothing fancy."

**[DRAW]** Below: show that a full loop = two exchanges. Two worldlines: draw them as braids. One crossing = one exchange. Two crossings (full wind) = full loop.

**[WRITE]**
```
Topologically: full braid = 2 exchanges

  ⟹ exchange phase = (1/2)(2π/m) = π/m
```

**[WRITE]** (boxed)
```
┌──────────────────────────┐
│   θ_exchange = π/m       │
└──────────────────────────┘
```

**[SAY]** "For m=1: θ = π, fermions. For m=3: θ = π/3. Neither boson nor fermion. These particles obey braid group statistics — anyons."

**[SAY]** "In Chern-Simons language, this has a beautiful restatement."

**[WRITE]**
```
Wilson loop correlator in U(1)_m CS:

  ⟨W₁(γ₁) W₁(γ₂)⟩ = exp( (2πi/m) Lk(γ₁, γ₂) )

  Lk = linking number of the two worldlines

  Lk = 1 (linked once) ⟹ phase = 2π/m  ✓
```

**[SAY]** "The expectation value of two Wilson loops in abelian Chern-Simons is the exponential of the linking number divided by the level. Braiding is linking. The topological invariant IS the physical observable."

**[CIRCLE]** all three boxed results (σ, Q, θ) if visible.

**[SAY]** "One integer m. Three universal observables: σ_xy = (1/m)(e²/h), Q = e/m, θ = π/m. That's the entire content of the topological effective theory at this level. Gauge invariance forces m to be an integer. Everything else follows."

**[SAY]** "Nakamura et al., 2020. Fabry-Pérot interferometer at ν = 1/3. Measure phase accumulation as quasiparticles enter the interferometer. Observed: 2π/3 per additional quasiparticle. Consistent with the linking number prediction. First direct measurement of anyonic statistics in a natural condensed matter system."

---

## BOARD 8: Global Structure — Edge + Torus (2.5 min)

**[WRITE]**
```
════════════════════════════════════════════
  GLOBAL STRUCTURE: two tests of topology
════════════════════════════════════════════
```

**[SAY]** "The conductance, charge, and statistics are response measurements — you poke the system and read off numbers. But topological order also has structural signatures that require global topology to reveal."

**[WRITE]**
```
(A) EDGE (boundary):

  On manifold M with ∂M ≠ ∅:

  δS_CS = (bulk EOM) − (m/4π) ∫_∂M a ∧ δa

  Boundary term is NOT gauge invariant!
  → bulk CS alone is inconsistent on ∂M

  Gauge invariance requires boundary DOF:
    chiral boson φ on ∂M

  S_edge = (m/4π) ∫_∂M (∂_t φ ∂_x φ − v(∂_x φ)²) dt dx

  → propagates in one direction (chiral)
  → central charge c = 1  (topological)
  → velocity v            (NOT topological)
```

**[SAY]** "This is anomaly inflow. You've seen the 4d version: axial anomaly in the bulk cancels the boundary fermion anomaly. Here: the bulk CS anomaly forces a chiral edge mode into existence. Its chirality and central charge are topological data; its speed is not."

**[WRITE]**
```
(B) TORUS (ground-state degeneracy):

  On T², EOM: da = 0  (flat connections only)
  
  Flat U(1) connections on T²:
    parameterized by holonomies
    u = ∮_α a,   v = ∮_β a

  Define operators:
    T₁ = e^{iu},   T₂ = e^{iv}

  CS commutation relation:
    [u, v] = 2πi/m

  ⟹   T₁ T₂ = e^{2πi/m} T₂ T₁
```

**[SAY]** "The holonomies don't commute. The commutator is fixed by the CS level m. This is a finite Heisenberg algebra."

**[WRITE]**
```
  T₁ T₂ = e^{2πi/m} T₂ T₁  cannot be satisfied on a 
  1-dimensional Hilbert space.

  Minimum faithful representation: dimension m.

  ⟹  dim H(T²) = m
```

**[BOX]** dim H(T²) = m.

**[SAY]** "For ν = 1/3: three degenerate ground states on a torus. No local perturbation can lift this — it's not a symmetry degeneracy, it's topological. Threading a flux quantum through one cycle rotates you through the three sectors. This was Wen's definition of topological order."

---

## BOARD 9: What's Protected / What's Not (1.5 min)

**[SAY]** "Let me be precise about what the topological theory actually controls versus what requires microscopic input."

**[WRITE]**
```
TOPOLOGICAL DATA                  │  NON-UNIVERSAL (mesoscopic)
(set by m alone, protected)       │  (depends on microscopic details)
──────────────────────────────────│──────────────────────────────────
σ_xy = (1/m)(e²/h)               │  Edge velocity v
Q_qh = e/m                       │  Tunneling exponents
θ_exchange = π/m                  │  Equilibration lengths
Edge chirality, c = 1             │  Interferometer visibility
dim H(T²) = m                    │  Coulomb-dominated interference
Linking: ⟨WW⟩ ~ exp(2πi Lk/m)   │  Quasiparticle localization
```

**[SAY]** "Left column: universal. Cannot change without closing the gap. Right column: depends on confining potential, interaction details, device geometry. Experimental care: you must verify you're measuring a quantity in the left column. Early interferometry experiments were fooled by Coulomb charging effects masquerading as braiding phases. Nakamura 2020 was careful — verified Aharonov-Bohm regime first."

---

## BOARD 10: Summary (1.5 min)

**[SAY]** "Let me close by writing the whole logical chain."

**[WRITE]**
```
THE LOGICAL CHAIN:

  Strong B-field
    → Landau level degeneracy
      → kinetic energy quenched
        → Coulomb creates gapped incompressible liquid
          → no local low-energy modes
            → effective theory must be topological
              → CHERN-SIMONS

  S = ∫ [(1/2π) A∧da − (m/4π) a∧da]

  One action, one integer m, five consequences:

    σ_xy = (1/m)(e²/h)      ✓  (10⁻⁹ precision)
    Q = e/m                  ✓  (shot noise 1997)
    θ = π/m                  ✓  (interferometry 2020)
    chiral edge, c = 1       ✓  (tunneling)
    GSD = m on torus         ✓  (flux threading)
```

**[SAY]** "The fractional quantum Hall effect is the proof of concept that topological field theory describes real macroscopic matter. The fact that one integer — forced to be integer by gauge invariance — simultaneously controls five independently measurable quantities is not an accident. It's the physical content of having a topological effective theory."

**[SAY]** (if time remains) "The open frontier: ν = 5/2. Believed to be the Moore-Read Pfaffian state — SU(2)₂ Chern-Simons theory. Non-abelian: exchanging quasiparticles executes unitary matrices on a degenerate ground state, not just phases. If confirmed, this gives topological qubits. Not yet observed in a natural condensed matter system. Open problem."

---

## Timing

| Board | Content | Time |
|-------|---------|------|
| 1 | Experiment + staircase | 1.5 min |
| 2 | Integer QHE (quick) | 1.5 min |
| 3 | Why fractional is hard + what survives | 2.5 min |
| 4 | Effective action + why CS is forced | 2.5 min |
| 5 | Hall conductance derivation | 3 min |
| 6 | Fractional charge derivation | 2.5 min |
| 7 | Anyonic statistics + linking number | 3 min |
| 8 | Global structure: edge + torus | 2.5 min |
| 9 | Honesty table | 1.5 min |
| 10 | Summary + logical chain | 1.5 min |
| **TOTAL** | | **~22 min** |

**To hit 20 min:** Slightly compress Boards 5 and 7 (skip writing intermediate steps of the S_eff substitution; skip writing the explicit linking formula).

**To hit 15 min:** Board 2 in 30s verbal. Boards 8+9 merged into 2 min verbal + table.

---

## Equations to Know Cold

Write these from memory on the board live:

1. **Action:** S = ∫ [(1/2π)A∧da − (m/4π)a∧da]
2. **EOM:** (1/2π)dA − (m/2π)da = 0  ⟹  da = (1/m)dA
3. **Integrated out:** S_eff = (1/4πm) ∫ A∧dA
4. **Current:** j^μ = (1/2πm) ε^{μνρ} ∂_ν A_ρ
5. **Streda:** j⁰ = (1/2πm) B
6. **Flux attachment:** m f₁₂ = 2π δ²(x)  ⟹  ∫f₁₂ = 2π/m
7. **Charge:** Q = (e/2π)∫f₁₂ = e/m
8. **AB phase:** φ = q·Φ = 1·(2π/m) = 2π/m
9. **Exchange:** θ = π/m  (half of full braid)
10. **Linking:** ⟨W(γ₁)W(γ₂)⟩ = exp(2πi·Lk(γ₁,γ₂)/m)
11. **Commutator:** T₁T₂ = e^{2πi/m} T₂T₁  ⟹  dim H = m
12. **Edge boundary term:** δS ⊃ −(m/4π) ∫_∂M a∧δa

---

## Potential Questions

**Q: Why odd m?**
Electrons are fermions. m=1 gives θ=π (fermion). The quasihole at m=1 IS the electron. Odd m ↔ fermionic constituents. Even m ↔ bosonic (exist but not the electron QHE).

**Q: Where does the emergent gauge field come from physically?**
Flux attachment (Zhang-Hansson-Kivelson 1989): attach m flux quanta to each electron → composite bosons. The emergent a implements that statistical transmutation. It's the same conceptual move as introducing a phonon field for a crystal — a collective degree of freedom that survives at low energy.

**Q: What about ν = 2/5, 2/3?**
K-matrix generalization. Multiple emergent gauge fields a^I, integer matrix K_{IJ}:
  S = ∫ [(1/4π) K_{IJ} a^I∧da^J + (1/2π) t_I A∧da^I]
Then σ_xy = t^T K⁻¹ t · (e²/h). Laughlin is K=(m), t=(1).

**Q: Why not Maxwell-Chern-Simons?**
Adding a Maxwell term F∧⋆F reintroduces the metric, gives a massive gauge boson (topological mass m_CS = ke²/2π), and creates propagating modes. It's NOT a TQFT — observables depend on geometry. The purity of CS is essential. This is why I emphasized "no Hodge star."

**Q: How is the torus degeneracy measured?**
Not on an actual torus. On an annulus (Corbino geometry), thread external flux through the hole. The system cycles through degenerate sectors with period h/e — that periodicity is the signature.

**Q: What's the connection to the Jones polynomial / knot invariants?**
In non-abelian CS (e.g., SU(2)_k), Wilson loop expectation values on S³ give the Jones polynomial of the knot. For abelian U(1)_m, it reduces to the linking number formula I wrote. The FQHE is the physical realization of this mathematics.

**Q: Is the fractional charge "real" — has an electron split?**
No. The electron is intact. The Chern-Simons duality redistributes electromagnetic charge: a unit source for a binds fractional a-flux, and the mixed term converts that to fractional electric charge. It's a collective effect, not fission.
