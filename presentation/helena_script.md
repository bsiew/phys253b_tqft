---
created_at: "2026-05-05T22:53:35-04:00"
updated_at: "2026-05-05T22:53:35-04:00"
generated_by: "claude-code"
updated_by: "claude-code"
timestamp_source: hook
---
# Helena's Chalk-Talk Script (Minutes 25-50)

## Board Layout

```
+========================================================================+
|  [FROM BRIAN — STAYS]                    [FROM BRIAN — STAYS]           |
|                                                                        |
|  S_CS = (k/4pi) int a ^ da            +------------------+            |
|                                        |   k in Z         |            |
|                                        +------------------+            |
|                                                                        |
|------------------------------------------------------------------------+
|  [HELENA'S WORKSPACE — LEFT HALF]     | [HELENA'S WORKSPACE — RIGHT]   |
|                                        |                                |
|  (Erase Hopf link)                     |                                |
|  Physics picks k:                      |                                |
|    nu = 1/m  =>  U(1)_m CS            |                                |
|                                        |                                |
|  Effective action:                     |  Anyons:                       |
|    S[a;A] = (1/2pi) A^da              |    Q = (q/m) e                 |
|             - (m/4pi) a^da            |    phi_braid = 2pi/m           |
|                                        |                                |
|  EOM: da = (1/m) dA                   |  Experiments:                  |
|                                        |    Nakamura: 2pi/3 (+-0.07)   |
|  S_eff[A] = (1/4pi m) A^dA           |    Bartolomei: pi/3            |
|                                        |    Werkmeister: graphene       |
|  sigma_xy = e^2 / (mh)               |                                |
|                                        |                                |
+========================================================================+
```

Key: Brian's CS action (top-left) and k in Z (top-right, boxed) stay throughout.
Helena erases Brian's Hopf link (bottom-right) at the start and uses that space.

---

## Minute-by-Minute Script

---

### Min 0-3: Pickup — Physics Picks k

**[SAY]**
"Thank you Brian. So we have this beautiful abstract machine — Chern-Simons at level k gives us quantized observables, links, ground-state degeneracy, all topological. The question is: does nature use it? The answer is yes. The fractional quantum Hall effect at filling nu = 1/m is described by U(1) Chern-Simons at level k = m. And m is not a free parameter — it's fixed by the electron density and the magnetic field."

**[DO]** Erase Brian's Hopf link (bottom-right). Point to Brian's k in Z box.

**[SAY]**
"The Laughlin state at nu = 1/m — this is Laughlin '83 — has wavefunction..."

**[WRITE]** (bottom-left, below Brian's action)
$$\Psi_{1/m} = \prod_{i<j}(z_i - z_j)^m \, e^{-\sum|z_k|^2/4\ell_B^2}$$

**[SAY]**
"Each pair of electrons shares an m-fold zero. This keeps them apart — correlations do all the work because the kinetic energy is quenched by the magnetic field. The route to the effective theory is flux attachment: reinterpret each electron as carrying m flux quanta of a fictitious gauge field a. Integrate out the gapped composite fermions, and you get..."

**[WRITE]** (below, with a box around it)
$$S[a;A] = \int \left[ \frac{1}{2\pi} A \wedge da - \frac{m}{4\pi} a \wedge da \right]$$

**[SAY]**
"A is the electromagnetic background — a probe. Little a is the emergent gauge field from flux attachment. There's no Maxwell term, no metric anywhere — purely topological. This IS Brian's Chern-Simons, with k = m, derived from microscopic physics."

**[DO]** Draw arrow from boxed action up to Brian's k in Z. Write "k = m" next to arrow.

---

### Min 3-10: Hall Conductance from CS

**[SAY]**
"Now let's see what this predicts. The first thing we can do is integrate out a. Vary with respect to a — it's dynamical."

**[WRITE]** (new line below the action)
$$\frac{\delta S}{\delta a}: \quad \frac{1}{2\pi} dA - \frac{m}{2\pi} da = 0$$

**[SAY]**
"This gives the equation of motion..."

**[WRITE]**
$$da = \frac{1}{m} dA$$

**[SAY]**
"On a simply connected patch, a = A/m. Substitute back into the action."

**[DO]** Show substitution step verbally: "The mixed term gives (1/2pi)(A)(dA/m), the pure term gives -(m/4pi)(A/m)(dA/m) = -(1/4pi m) A dA. Together..."

**[WRITE]** (boxed)
$$S_{\text{eff}}[A] = \frac{1}{4\pi m} \int A \wedge dA$$

**[SAY]**
"This is a Chern-Simons term for the electromagnetic field itself. No metric — the Hall response is topological. Now read off the current."

**[WRITE]**
$$j^\mu = \frac{\delta S_{\text{eff}}}{\delta A_\mu} = \frac{1}{2\pi m} \epsilon^{\mu\nu\rho} \partial_\nu A_\rho$$

**[SAY]**
"The spatial component: j^i = (1/2pi m) epsilon^{ij} E_j. That's a transverse current proportional to the electric field — Hall conductance."

**[WRITE]** (large, boxed, underlined)
$$\sigma_{xy} = \frac{e^2}{mh}$$

**[SAY]**
"Restoring the units. For m = 3, sigma_xy = e^2/(3h). This is measured to parts in 10^9. And the derivation used nothing but: write the action, vary, substitute. The entire calculation is five lines. That's the power of the topological description — you can't smooth-deform away a quantized coefficient."

**[DO]** Pause. Let the audience absorb.

**[SAY]**
"Notice what we did NOT use: no Kubo formula, no linear response, no perturbation theory. The quantization follows from the topology of the gauge bundle — specifically from the large-gauge-transformation argument Brian showed you."

---

### Min 10-17: Anyons from Wilson Loops

**[SAY]**
"That was the ground state response. Now: excitations. Brian showed you Wilson loops as the observables of CS theory. In the FQHE context, a Wilson line endpoint is a quasiparticle."

**[DO]** Move to right half of board.

**[WRITE]** (right side, header)
**Quasiparticles = Wilson-line endpoints**

**[SAY]**
"Insert a Wilson line of charge q in the emergent gauge field a. The equation of motion gets a source."

**[WRITE]**
$$\frac{m}{2\pi} \epsilon^{\mu\nu\rho} \partial_\nu a_\rho = q \, \delta^{(2)}(\mathbf{x} - \mathbf{x}_0)$$

**[SAY]**
"The endpoint binds emergent flux. But the mixed coupling A wedge da converts emergent flux into electromagnetic charge. Integrate the induced density j^0 = (1/2pi) f_{12} over a region enclosing the source..."

**[WRITE]** (boxed)
$$Q = \frac{q}{m} \, e$$

**[SAY]**
"For q = 1, the elementary quasiparticle carries charge e/m. At nu = 1/3, that's e/3. This was confirmed by shot noise in 1997 — Saminadayar, de Picciotto."

**[DO]** Brief pause, then:

**[SAY]**
"Now the braiding. Brian computed the expectation of linked Wilson loops in U(1)_k. Two quasiparticles of charge 1 trace worldlines gamma_1, gamma_2. Their mutual phase is..."

**[WRITE]** (below Q, boxed)
$$\langle W_1(\gamma_1) W_1(\gamma_2) \rangle_{U(1)_m} = \exp\!\left(\frac{2\pi i}{m} \, \text{Lk}(\gamma_1,\gamma_2)\right)$$

**[SAY]**
"When one winds around the other once, Lk = 1, and the braiding phase is..."

**[WRITE]** (large)
$$\phi_{\text{braid}} = \frac{2\pi}{m}$$

**[SAY]**
"A full winding is two exchanges, so the statistical angle for a single exchange is theta = pi/m. For m = 1 that's pi — fermions. For m = 3, theta = pi/3 — neither boson nor fermion. These are anyons. They exist only in 2+1 dimensions because the braid group replaces the symmetric group."

**[DO]** Draw a quick picture: two particle worldlines braiding in 2+1d spacetime (a simple braid crossing).

**[SAY]**
"So for nu = 1/3 we have three predictions from one integer m = 3:"

**[WRITE]** (clear summary, boxed together)
$$\nu = 1/3: \quad \sigma_{xy} = \frac{e^2}{3h}, \quad Q = \frac{e}{3}, \quad \phi = \frac{2\pi}{3}$$

**[SAY]**
"One theory, one parameter, three predictions. All measured. Let me show you how."

---

### Min 17-23: Experiments

**[SAY]**
"Three experiments, in chronological order. Each probes a different observable, all controlled by m = 3."

**[DO]** Erase the equation-of-motion working (left side, middle). Keep the boxed effective action and sigma_xy. Use freed space for experiment summary.

#### Nakamura 2020 (min 17-19)

**[SAY]**
"Nakamura, Liang, Gardner, Manfra — 2020. A Fabry-Perot interferometer at nu = 1/3 in GaAs/AlGaAs. Two quantum point contacts define an island. Edge quasiparticles travel two paths around the island and interfere."

**[WRITE]** (sketch: two QPCs, island between them, edge currents going both ways)

**[SAY]**
"The conductance oscillates with magnetic flux — that's the Aharonov-Bohm part. But here's the key: when a bulk quasiparticle hops in or out of the island, it's a charge-e/3 event, and the interference pattern jumps by a discrete phase. That phase is the braiding phase — the edge quasiparticle has gone around the bulk one."

**[WRITE]**
$$G(\Phi) \sim \cos\!\left(\frac{2\pi e^* \Phi}{\Phi_0} + N_{\text{qp}} \cdot \frac{2\pi}{m}\right)$$

**[SAY]**
"They see telegraph-noise jumps in the fringe pattern. Each jump: one quasiparticle entering. The extracted phase:"

**[WRITE]**
$$\Delta\phi = (0.98 \pm 0.07) \times \frac{2\pi}{3}$$

**[SAY]**
"Consistent with 2pi/3. This is the FIRST direct observation of anyonic braiding — not inferred from charge, not from tunneling exponents. A discrete phase jump, topologically robust, seen directly."

#### Bartolomei 2020 (min 19-21)

**[SAY]**
"Same year, completely different technique. Bartolomei et al. built an anyon collider. Instead of one quasiparticle going around another, two quasiparticles collide at a beam splitter."

**[DO]** Quick sketch: two input beams, one QPC beam-splitter, two output ports.

**[SAY]**
"Like Hong-Ou-Mandel for photons: bosons bunch, fermions anti-bunch, anyons do something in between. The output noise correlations depend on the statistical angle theta."

**[WRITE]**
$$\theta_{\text{measured}} = (0.33 \pm 0.03)\pi$$

**[SAY]**
"pi/3. Exactly what U(1)_3 Chern-Simons predicts for a single exchange."

#### Werkmeister 2024 (min 21-23)

**[SAY]**
"Finally — and this is the one that makes it a topological invariant rather than a GaAs coincidence — Werkmeister et al. 2024. Same Fabry-Perot technique, but in graphene. Completely different band structure — Dirac fermions, not parabolic. Different disorder, different edge physics. But the same universal number."

**[WRITE]**
$$\Delta\phi_{\text{graphene}} = (1.00 \pm 0.05) \times \frac{2\pi}{3}$$

**[SAY]**
"The theory says the phase is a topological invariant — independent of microscopic details. Two radically different materials, same quantized answer. That's what 'topological' means experimentally."

**[DO]** Write summary table on right side:

**[WRITE]**
```
Experiment        Observable        Result
─────────────────────────────────────────────
Shot noise '97    charge            e/3
Nakamura '20      braiding phase    2pi/3
Bartolomei '20    exchange angle    pi/3
Werkmeister '24   braiding phase    2pi/3
```

**[SAY]**
"Four experiments, three types of measurement, two materials, one integer: m = 3."

---

### Min 23-25: Closing

**[SAY]**
"Let me close by connecting back to Brian's talk."

**[DO]** Point to Brian's action (top-left), then the boxed k in Z (top-right), then sigma_xy (left), then phi_braid (right), then the experiment table.

**[SAY]**
"The same theory operates at three levels. First — as a topological invariant. Brian showed you: Wilson loops, linking numbers, ground-state degeneracy. Mathematical structure independent of any physical realization."

"Second — as a Lagrangian. Chern-Simons at level m emerges as the effective theory of the Laughlin state at nu = 1/m. Flux attachment and integrating out composite fermions give you the action. From five lines of calculation: quantized Hall conductance, fractional charge, anyonic braiding."

"Third — as something measured. Interferometry, noise correlations, two different materials. The phase 2pi/3 is not a fit — it's a prediction of the integer m = 3 that also controls transport and charge."

**[DO]** Write, centered at bottom:

**[WRITE]**
$$\boxed{\text{Invariant} \longrightarrow \text{Lagrangian} \longrightarrow \text{Measured}}$$

**[SAY]**
"One integer k. Quantized by gauge invariance. Selected by the filling fraction. Confirmed in the lab. That's what it means for a topological field theory to govern real matter."

**[DO]** Pause. "Questions?"

---

## Anticipated Questions

### Q1: "Why can't the Nakamura phase jump be a Coulomb effect rather than a topological braiding phase?"

**Prepared answer:** "Great question. In Coulomb-dominated interferometers, adding charge e/3 to the island shifts the electrostatic potential, which does produce a phase shift — but that shift depends on the geometry: the capacitance, the distance to gates, the QPC transmission. Nakamura's device is specifically designed to suppress this: large area (~1 micron^2), trilayer screening wells that reduce bulk-edge coupling below the thermal scale. The signature that it's topological rather than electrostatic is that the measured phase is independent of where in the island the quasiparticle sits, and it matches 2pi/3 rather than a device-dependent value. The Werkmeister graphene result — completely different capacitances — giving the same number clinches it."

### Q2: "You showed abelian anyons. What about non-abelian? Has anyone seen those?"

**Prepared answer:** "Honest answer: no, not in a naturally occurring phase. The nu = 5/2 state is the best candidate — believed to be Moore-Read, which is SU(2)_2 Chern-Simons with Ising anyons. Thermal Hall measurements are consistent, but no one has demonstrated the non-abelian braiding itself. Google's 2023 processor experiment (Andersen et al.) verified the non-abelian braid algebra on hardware — twist defects in a surface code executing the Ising fusion rule sigma x sigma = 1 + psi — but that's a synthetic emulation, not a natural phase. The distinction matters: natural topological order gives you passive protection from the gap; the synthetic version requires active error correction."

### Q3: "The K-matrix generalizes this to other fillings. How does that work?"

**Prepared answer:** "For non-Laughlin fractions like nu = 2/5, you need multiple emergent gauge fields. Replace the integer m with an integer matrix K, and the charge coupling with a vector t. The action becomes S = (1/4pi) K_{IJ} a^I da^J + (1/2pi) t_I A da^I. Everything generalizes: sigma_xy = (e^2/h) t^T K^{-1} t, quasiparticle charge = e t^T K^{-1} l, braiding = 2pi l^T K^{-1} l'. GSD on the torus = |det K|. The Laughlin case is the 1x1 matrix K = (m). Every abelian FQH state fits this framework — Wen and Zee classified them in 1992."

---

## Coordination Notes with Brian's Segment

1. **Board inheritance:** Brian leaves CS action top-left and "k in Z" boxed top-right. Helena erases only the Hopf link (bottom-right). Everything else of Brian's stays visible throughout — reinforces the connection.

2. **Vocabulary alignment:** Brian introduces "level k", "Wilson loop", "linking number." Helena uses these phrases without re-defining them — treats them as established. The phrase "Brian showed you" or "as Brian computed" signals continuity.

3. **Transition moment:** Brian's closing line is "k controls level, links, GSD. All topological. Helena will show you k is measurable." Helena's first line is "Thank you Brian. So we have this beautiful abstract machine..." — immediate pickup, no reset.

4. **Cross-references during Helena's segment:**
   - Min 10: "Brian computed the expectation of linked Wilson loops" — refers back to his Hopf link calculation.
   - Min 23: "as Brian showed" — pointing to his k in Z box.
   - Closing: pointing to both halves of the board simultaneously.

5. **Pacing budget:**
   - Min 0-3 (3 min): Setup + Laughlin + effective action. Tight.
   - Min 3-10 (7 min): Hall conductance derivation. This is the mathematical core — take time, show every step.
   - Min 10-17 (7 min): Anyons. Wilson-loop braiding phase. Conceptual core.
   - Min 17-23 (6 min): Experiments. Three papers, keep brisk — one key number each.
   - Min 23-25 (2 min): Closing synthesis. Short, punchy.

6. **If running long:** Cut Bartolomei to one sentence ("and an independent collider experiment by Bartolomei confirmed pi/3 via noise correlations"). This saves ~90 seconds.

7. **If running short:** Expand the closing to discuss the non-abelian frontier (nu = 5/2, Moore-Read) or mention the K-matrix generalization as the "next chapter."

8. **Chalk colors (if available):**
   - White: equations, standard text
   - Yellow: boxed results (sigma_xy, Q, phi_braid)
   - Blue: experimental numbers
   - Keep consistent with whatever Brian used for his k in Z box
