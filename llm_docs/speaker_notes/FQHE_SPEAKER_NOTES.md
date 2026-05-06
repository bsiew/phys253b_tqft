---
created_at: "2026-05-05T17:48:13-04:00"
updated_at: "2026-05-05T17:48:13-04:00"
generated_by: "claude-code"
updated_by: "claude-code"
timestamp_source: hook
---
# Speaker Notes: The Fractional Quantum Hall Effect as a Topological Field Theory

## Target: ~12-15 minutes. Audience: anyone who's done a year of QFT.

---

## [SLIDE 1] The Setup — What You Measure (1 min)

Take a 2D electron gas — GaAs/AlGaAs heterostructure, electrons confined to move in a plane. Apply a strong perpendicular magnetic field B ~ 10 T. Cool to T ~ 50 mK.

Measure the Hall conductance: drive a current I_x along the sample, measure the transverse voltage V_y. The Hall conductivity is

$$\sigma_{xy} = I_x / V_y$$

**What you see:** Plateaux. Not a smooth function of B. The conductivity locks onto discrete values and refuses to move.

For the **integer** quantum Hall effect (IQHE), the plateaux sit at:

$$\sigma_{xy} = n \frac{e^2}{h}, \quad n = 1, 2, 3, \ldots$$

For the **fractional** quantum Hall effect (FQHE), discovered by Tsui, Störmer, and Gossard in 1982, the plateaux sit at:

$$\sigma_{xy} = \nu \frac{e^2}{h}, \quad \nu = \frac{1}{3},\, \frac{2}{5},\, \frac{5}{2},\, \ldots$$

These numbers are measured to one part in 10^9. They don't drift with temperature, disorder, sample shape, or impurity concentration. Something is protecting them.

---

## [SLIDE 2] Integer QHE — The Easy Case (2 min)

The integer case is single-particle physics. A charged particle in a magnetic field has discrete energy levels — Landau levels — spaced by the cyclotron energy ℏω_c = ℏeB/m.

Each Landau level has a huge degeneracy: the number of states per level equals the number of flux quanta threading the sample, N_φ = BA/(h/e). The filling fraction is:

$$\nu = N_e / N_\phi$$

At ν = n (integer), you fill exactly n Landau levels. The gap to the next level is ℏω_c. This is just a band insulator in disguise — filled bands don't conduct longitudinally, but the Hall conductance is quantized because the Chern number of each filled band is 1.

**Key point for what follows:** The integer QHE is a single-particle phenomenon. No interactions needed. The gap is the cyclotron gap. The quantization is topological (Chern number of the band), but the mechanism is boring — it's just filling bands.

---

## [SLIDE 3] The Fractional Problem — Why It's Hard (2 min)

Now set ν = 1/3. You have one-third as many electrons as there are available states in the lowest Landau level. A single partially-filled Landau level with Coulomb interactions. The single-particle energies are all degenerate — the kinetic energy is frozen — so Coulomb interactions dominate.

This is a genuinely strongly-correlated many-body problem. There is no small parameter. You cannot do perturbation theory.

And yet: the Hall conductance is σ_{xy} = (1/3)(e²/h), measured to extraordinary precision. The excitations carry charge e/3. Exchanging two excitations gives a phase e^{iπ/3} — neither bosonic nor fermionic. These are anyons.

**The question:** What structure is rigid enough to produce these universal numbers, immune to all the microscopic complexity?

**The answer:** The low-energy effective theory is a topological field theory — specifically, Chern-Simons theory. And the universal numbers are controlled by a single integer.

---

## [SLIDE 4] The Effective Action — Writing It Down (2 min)

We do not solve the microscopic problem. We can't — it's ~10^11 interacting electrons. Instead we write an effective field theory valid at energies below the gap.

The logic: the FQHE state is gapped. Below the gap, the correct description is whatever action is consistent with the symmetries and the topology. For ν = 1/m, that action is:

$$S[a; A] = \int \left[ \frac{1}{2\pi} A \wedge da - \frac{m}{4\pi} a \wedge da \right]$$

Here:
- **A** is the electromagnetic gauge field (external probe, background).
- **a** is an *emergent* U(1) gauge field — a collective mode packaging electron correlations.
- **m** is an odd integer (odd because electrons are fermions).

There is no Maxwell term ∫F∧⋆F. No metric anywhere. The action is purely topological: it depends only on the topology of the gauge field configuration, not on the geometry of the sample. This is a Chern-Simons theory.

**Why no metric = why the observable is protected:** If the action doesn't see the metric, then smooth deformations of the sample, impurities, gentle perturbations — anything that changes the local geometry without closing the gap — cannot change the answer.

---

## [SLIDE 5] Derivation 1: Hall Conductance (2 min)

Vary with respect to a (it's dynamical):

$$\frac{\delta S}{\delta a} = 0 \implies \frac{1}{2\pi} dA - \frac{m}{2\pi} da = 0$$

So on-shell: da = dA/m. On a simply-connected patch, a = A/m. Substitute back:

$$S_{\text{eff}}[A] = \frac{1}{4\pi m} \int A \wedge dA$$

This is a Chern-Simons action for the background field. The current is:

$$j^\mu = \frac{\delta S_{\text{eff}}}{\delta A_\mu} = \frac{1}{2\pi m} \epsilon^{\mu\nu\rho} \partial_\nu A_\rho$$

Read off the spatial components: j^i = (1/2πm) ε^{ij} E_j. This is a Hall current! The conductivity is:

$$\boxed{\sigma_{xy} = \frac{1}{2\pi m} = \frac{e^2}{h} \cdot \frac{1}{m}}$$

(restoring e, ℏ in the last step). For m = 3: σ_{xy} = (1/3)(e²/h). Done.

**Why m must be an integer:** Put the theory on S² × S¹ with one flux quantum through S². A large gauge transformation winding once around S¹ shifts the action by ΔS = 2πm. Requiring exp(iS) to be single-valued forces m ∈ ℤ. This is the same argument that quantizes the Chern-Simons level — gauge invariance under large gauge transformations. The quantization of conductance is a consistency condition, not a fitting parameter.

---

## [SLIDE 6] Derivation 2: Fractional Charge (2 min)

Insert a static quasihole at the origin. This is a point source for the emergent gauge field:

$$S_{\text{source}} = \int a \wedge J, \quad J = 2\pi\, \delta^{(2)}(\mathbf{x})\, dt$$

The equation of motion now picks up a delta function:

$$m\, f_{12}(\mathbf{x}) = 2\pi\, \delta^{(2)}(\mathbf{x})$$

where f = da is the emergent field strength. Each quasihole carries emergent flux 2π/m. The mixed term A∧da converts emergent flux to electric charge density. Reading j⁰ = f₁₂/(2π) from varying with respect to A₀:

$$Q_{\text{qh}} = \int d^2x\, j^0 = \frac{1}{2\pi} \int f_{12}\, d^2x = \frac{1}{m}$$

In units of e:

$$\boxed{Q_{\text{qh}} = \frac{e}{m}}$$

For m = 3, the quasihole carries charge e/3. The electron hasn't split — the Chern-Simons duality has redistributed the charge through the mixed coupling. This was measured via shot noise experiments by Saminadayar et al. (1997) and de-Picciotto et al. (1997).

---

## [SLIDE 7] Derivation 3: Anyonic Statistics (1.5 min)

Two quasiholes = two Wilson loops in the emergent gauge field. Quasihole 1 carries unit a-charge. Quasihole 2 carries emergent flux 2π/m (from the flux attachment we just derived).

Aharonov-Bohm: take quasihole 1 around quasihole 2. The phase is:

$$\text{(charge)} \times \text{(enclosed flux)} = 1 \times \frac{2\pi}{m} = \frac{2\pi}{m}$$

A full winding = two exchanges. So a single exchange gives:

$$\boxed{\theta_{\text{exchange}} = \frac{\pi}{m}}$$

For m = 3: θ = π/3. Not 0 (bosons), not π (fermions). These are anyons.

**The key structural point:** The same integer m that gave us σ_{xy} = e²/(mh) and Q = e/m now gives θ = π/m. One number controls everything. That's the power of the topological effective theory.

This was measured in 2020 by Nakamura et al. using a Fabry-Pérot interferometer at ν = 1/3. The observed phase shift is consistent with 2π/3 for a full winding.

---

## [SLIDE 8] Edge Modes and Anomaly Inflow (1.5 min)

Real samples have boundaries. On a manifold with boundary, the Chern-Simons action is NOT gauge-invariant:

$$\delta S_{\text{CS}} \supset -\frac{m}{4\pi} \int_{\partial M} A \wedge \delta A$$

This boundary term is an anomaly. Gauge invariance of the full system requires a boundary degree of freedom whose anomalous variation cancels this. That boundary theory is a chiral boson:

$$S_{\text{edge}} = \frac{m}{4\pi} \int_{\partial M} (\partial_t \phi\, \partial_x \phi - v\, (\partial_x \phi)^2)\, dt\, dx$$

The edge propagates in one direction only (chiral). This is anomaly inflow: the bulk topological theory "pushes" its would-be gauge anomaly onto the boundary, which responds by supporting a gapless chiral mode.

**What's universal:** The chirality and the anomaly coefficient (central charge c = 1 for all Laughlin states). **What's not:** The edge velocity v, equilibration lengths, tunneling exponents — these are non-universal.

---

## [SLIDE 9] Ground-State Degeneracy (1 min)

Put the system on a torus (periodic boundary conditions in both directions). The equations of motion set da = 0 (flat connection). Flat U(1) connections on a torus are parameterized by two holonomies:

$$u = \oint_\alpha a, \quad v = \oint_\beta a, \quad u, v \sim u + 2\pi$$

The Chern-Simons action on this space reduces to quantum mechanics on the torus of holonomies with symplectic form:

$$\Omega = \frac{m}{2\pi}\, du \wedge dv$$

Geometric quantization: one state per 2π of phase-space area. Total phase-space area = (2π)² × m/(2π) = 2πm. Number of states:

$$\boxed{\dim \mathcal{H} = m}$$

For ν = 1/3 on a torus: three degenerate ground states. This degeneracy is topological — it cannot be lifted by any local perturbation. It was one of Wen's original definitions of topological order.

---

## [SLIDE 10] What's Really Topological and What Isn't (1.5 min)

Not everything called "topological" in the QHE literature is actually protected:

| Observable | Status |
|-----------|--------|
| σ_{xy} = νe²/h | Protected: changes only at phase transitions |
| Quasihole charge e/m | Protected: set by the level |
| Exchange phase π/m | Protected: topological (linking number) |
| Edge chirality | Protected: anomaly coefficient |
| Ground-state degeneracy on torus | Protected: topological |
| Edge velocity | NOT protected: depends on confining potential |
| Tunneling exponents | NOT protected: depends on interactions |
| Interferometer visibility | NOT protected: Coulomb effects, area fluctuations |

The topological effective theory gives you the left column for free. The right column requires microscopic modeling. The worst confusion in the experimental literature comes from conflating the two — claiming a measurement tests the topological prediction when it actually tests the non-topological periphery.

---

## [SLIDE 11] The Experimental Score (1 min)

Where do we stand?

- **σ_{xy} quantization:** Measured to 1 part in 10⁹. Unambiguous.
- **Fractional charge e/3:** Measured via shot noise (1997) and tunneling. Clean.
- **Anyonic phase 2π/3:** Measured by Nakamura et al. (2020) using Fabry-Pérot interferometry at ν = 1/3. The measured phase accumulation per quasiparticle is consistent with the prediction. This is the most direct evidence for anyonic statistics in a natural (non-engineered) system.
- **Non-abelian braiding (ν = 5/2):** NOT conclusively demonstrated in a condensed-matter system. Andersen et al. (2023) demonstrated non-abelian braiding on a superconducting quantum processor — but that is a synthetic emulation, not a natural topological phase. The Moore-Read state at ν = 5/2 is still an open experimental question.

---

## [SLIDE 12] One Sentence Summary

The fractional quantum Hall effect is the proof of concept that topological field theory governs real macroscopic matter: a single integer in a metric-free action simultaneously predicts the quantized conductance, the fractionalized charge, the anyonic exchange statistics, the chiral edge mode, and the topological ground-state degeneracy — and experiment confirms all of them.

---

## Timing Summary

| Section | Time |
|---------|------|
| Setup / what you measure | 1 min |
| Integer QHE | 2 min |
| Why fractional is hard | 2 min |
| The effective action | 2 min |
| Hall conductance derivation | 2 min |
| Fractional charge derivation | 2 min |
| Anyonic statistics derivation | 1.5 min |
| Edge modes / anomaly inflow | 1.5 min |
| Ground-state degeneracy | 1 min |
| What's topological and what isn't | 1.5 min |
| Experimental score | 1 min |
| **Total** | **~17.5 min** |

If you need to trim to 12 minutes: cut Slide 2 (integer QHE) to 30 seconds of "band insulator, Chern number, moving on," compress Slide 8 (edges) to one sentence ("anomaly inflow forces a chiral edge"), and skip Slide 9 (GSD). That gets you to ~12.
