---
created_at: "2026-05-05T22:53:52-04:00"
updated_at: "2026-05-05T22:53:52-04:00"
generated_by: "claude-code"
updated_by: "claude-code"
timestamp_source: hook
---
# Brian's Board Script: Chern-Simons as TQFT (Minutes 0-25)

## Board Layout

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                              CHALKBOARD                                      │
│                                                                             │
│  ┌─── PANEL LEFT (permanent) ───┐  ┌──── PANEL CENTER (working) ────┐      │
│  │                               │  │                                 │      │
│  │  CS action:                   │  │  [Level quantization argument]  │      │
│  │  S_CS = (k/4π) ∫ ω_CS(A)     │  │                                 │      │
│  │                               │  │  → erased min 11 →              │      │
│  │  ω_CS = Tr(A∧dA + ⅔A∧A∧A)   │  │                                 │      │
│  │                               │  │  [Wilson loops / linking]        │      │
│  │  Key point: NO METRIC         │  │                                 │      │
│  │                               │  │  → erased min 19 →              │      │
│  │  EOM: F = 0                   │  │                                 │      │
│  │  (flat connections only)      │  │  [Hilbert space / torus]        │      │
│  │                               │  │                                 │      │
│  └───────────────────────────────┘  └─────────────────────────────────┘      │
│                                                                             │
│  ┌─── PANEL RIGHT (permanent after min 4) ──┐                               │
│  │                                           │                               │
│  │  Gauge transf of action:                  │                               │
│  │  S[A^g] - S[A] = -2πk n(g)               │                               │
│  │                                           │                               │
│  │  e^{iS} invariant ⟺ k ∈ ℤ               │                               │
│  │                                           │                               │
│  │  TQFT functor:                            │                               │
│  │  Σ ↦ H_{G,k}(Σ)                          │                               │
│  │  M ↦ Z_k(M) ∈ ℂ                          │                               │
│  │                                           │                               │
│  └───────────────────────────────────────────┘                               │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Minute-by-Minute Script

### Minutes 0-3: Setup — The CS action and metric independence

**Min 0-1: Opening frame**

SAY: "Our paper asks: what does it mean for a gauge theory to be topological? The answer lives in three dimensions. Today I'll show you the theory — Chern-Simons — and Helena will show you where nature uses it."

WRITE (panel left, stays permanently):
$$S_{\text{CS}}[A] = \frac{k}{4\pi}\int_M \tr\left(A\wedge dA + \frac{2}{3}A\wedge A\wedge A\right)$$

SAY: "This is the Chern-Simons action. $M$ is a closed oriented 3-manifold, $G$ a compact Lie group, $A$ a connection one-form."

**Min 1-2: The metric-free point**

SAY: "Compare with Yang-Mills." WRITE (temporarily, upper center):
$$S_{\text{YM}} = -\frac{1}{2g^2}\int d^3x\; \tr F_{\mu\nu}F^{\mu\nu}$$

SAY: "Yang-Mills needs $g^{\mu\nu}$ twice to contract indices. But in the CS action" — *tap the CS action* — "we use only the wedge product, the exterior derivative, and the trace. The Levi-Civita tensor $\varepsilon^{\mu\nu\rho}$ replaces the metric. No metric means observables can't see geometry — only topology."

ERASE the YM action.

**Min 2-3: Equations of motion**

WRITE (panel left, permanent):
$$\delta S_{\text{CS}} = \frac{k}{2\pi}\int_M \tr(\delta A \wedge F) \quad \Longrightarrow \quad F = 0$$

SAY: "Varying the action gives flatness. No propagating degrees of freedom — the classical solutions are flat connections. This already smells topological: the theory has no local excitations, only global data."

---

### Minutes 4-10: Level Quantization (showpiece argument)

**Min 4-5: Setting up the question**

SAY: "So far $k$ is a real number. I'll now show you that quantum consistency forces $k$ to be an integer. This is the most important structural result."

SAY: "Under a gauge transformation $g: M \to G$, the CS form shifts. From our Proposition 5.2 in the paper:"

WRITE (center board):
$$\omega_{\text{CS}}(A^g) = \omega_{\text{CS}}(A) - \frac{1}{3}\tr\bigl((g^{-1}dg)^{\wedge 3}\bigr) + d(\text{exact})$$

SAY: "On a closed manifold, the exact piece integrates to zero by Stokes. What remains is the Wess-Zumino three-form — a topological quantity that detects the winding of $g$."

**Min 5-7: The winding number integral**

SAY: "For $G = SU(2) \cong S^3$, a gauge transformation $g: M \to S^3$ has an integer-valued degree. The degree has an integral formula:" 

WRITE (center):
$$n(g) = \frac{1}{24\pi^2}\int_M \tr\bigl((g^{-1}dg)^{\wedge 3}\bigr)$$

SAY: "The normalization $24\pi^2$ — we verify this by explicit computation with Euler angles in the paper. The point is: this integral is always an integer."

WRITE (below, building the chain):
$$\therefore \quad S_{\text{CS}}[A^g] - S_{\text{CS}}[A] = -\frac{k}{12\pi}\cdot 24\pi^2 \cdot n(g) = -2\pi k\, n(g)$$

*Circle this result.*

**Min 7-9: The punchline**

SAY: "Now. The path integral weight is $e^{iS}$. Gauge invariance of the quantum theory requires:"

WRITE (panel right, permanent):
$$e^{iS_{\text{CS}}[A^g]} = e^{iS_{\text{CS}}[A]}$$
$$\Longleftrightarrow \quad e^{-2\pi i k\, n(g)} = 1 \quad \forall\, n \in \mathbb{Z}$$

SAY: "Since maps $g: S^3 \to S^3$ achieve every integer degree, this holds for all $n$ if and only if..."

WRITE (panel right, box it):
$$\boxed{k \in \mathbb{Z}}$$

SAY: "Level quantization. A continuous classical coupling is forced to be discrete by the topology of the gauge group. The path integral simply doesn't make sense otherwise."

**Min 9-10: Scope and generalization**

SAY: "For general compact simple simply-connected $G$, the same argument works once you normalize $\tr$ so the three-form generates $H^3(G, \mathbb{Z})$. For $U(1)$ it's a separate story — $\pi_3(U(1)) = 0$, so the large-gauge mechanism is different. The abelian quantization comes from summing over nontrivial bundles."

*Pause. Take a breath. Check the room.*

---

### Minutes 11-18: Wilson Loops, the Hopf Link, and the Jones Polynomial

**Min 11-12: Wilson loop definition**

ERASE center board.

SAY: "Now for observables. The action isn't gauge-invariant as a number — it shifts by $2\pi k n$. But Wilson loops are honest observables."

WRITE (center):
$$W_R(C)[A] = \tr_R\, \mathcal{P}\exp\oint_C A$$

SAY: "Path-ordered exponential around a closed curve $C$, traced in representation $R$. Gauge-invariant because on a closed loop the conjugation cancels in the trace."

SAY: "And because the action is metric-free, these expectation values are topological invariants of the link $C_1 \cup \cdots \cup C_n$ in $M$. They don't change under smooth deformations that don't cross curves through each other."

**Min 12-14: Abelian linking computation**

SAY: "Simplest case: $U(1)$, two loops $C_1, C_2$ on $S^3$, charges $q_1, q_2$."

WRITE:
$$\langle W_{q_1}(C_1)\, W_{q_2}(C_2)\rangle_{S^3} = \exp\!\left(-\frac{2\pi i\, q_1 q_2}{k}\,\text{Lk}(C_1, C_2)\right)$$

SAY: "The answer is purely topological — it depends only on the linking number of the two curves. The method is completing the square in the Gaussian path integral."

*Draw a quick sketch of two linked circles (Hopf link).*

SAY: "For the Hopf link, $\text{Lk} = 1$. With $q_1 = q_2 = 1$ and $k = 3$ — the Laughlin $\nu = 1/3$ state — this gives a braiding phase $e^{2\pi i/3}$. Helena will tell you this has been measured."

**Min 14-16: Non-abelian case and Witten's result**

SAY: "For the non-abelian theory, Witten showed something remarkable. Take $G = SU(2)$, level $k$, fundamental representation. The Wilson loop expectation value on any link $L \subset S^3$ gives:"

WRITE:
$$\langle W_\square(L)\rangle_{S^3} \longleftrightarrow \text{Jones polynomial } V_L(q) \text{ at } q = e^{2\pi i/(k+2)}$$

SAY: "A gauge-theory path integral reproduces a classical knot invariant. The shifted level $k+2$ — that's $k + h^\vee$ with $h^\vee = 2$ for $SU(2)$ — is a one-loop quantum correction."

**Min 16-18: Hopf link from the modular S-matrix**

SAY: "Let me show you the Hopf link value explicitly. The modular $S$-matrix for $SU(2)_k$:"

WRITE:
$$S_{ab} = \sqrt{\frac{2}{k+2}}\,\sin\!\left(\frac{(a+1)(b+1)\pi}{k+2}\right)$$

WRITE:
$$\langle W_{\square,\square}(\text{Hopf})\rangle_{S^3} = \frac{S_{11}}{S_{00}} = \frac{\sin(4\pi/(k+2))}{\sin(\pi/(k+2))}$$

SAY: "Normalized by the unknot value, the Hopf link gives $2\cos(2\pi/(k+2))$. This is the Jones polynomial of the Hopf link evaluated at the appropriate root of unity."

---

### Minutes 19-23: Hilbert Space on Surfaces

**Min 19-20: The canonical analysis**

ERASE center board.

SAY: "I've shown you the action and observables on closed 3-manifolds. Now cut spacetime open: put the theory on $\mathbb{R}_t \times \Sigma$ where $\Sigma$ is a closed surface. How many quantum states live on $\Sigma$?"

WRITE (center):
$$S_{\text{CS}} = \frac{k}{4\pi}\int dt\int_\Sigma \tr\left(-A_\Sigma \wedge \partial_t A_\Sigma + 2A_0 F_\Sigma\right)$$

SAY: "$A_0$ has no time derivative — it's a Lagrange multiplier. Varying it gives the constraint $F_\Sigma = 0$. Physical states live on flat connections modulo gauge."

WRITE:
$$\mathcal{M}_G(\Sigma) = \{A \mid F_\Sigma = 0\}/\mathcal{G} \;\cong\; \text{Hom}(\pi_1(\Sigma), G)/G$$

**Min 20-22: The torus, worked out**

SAY: "The cleanest example: $G = U(1)$, $\Sigma = T^2$. A flat $U(1)$ connection on the torus is specified by two holonomies:"

WRITE:
$$A_\Sigma = u\, dx + v\, dy, \qquad u, v \in [0, 2\pi)$$

SAY: "Substituting into the action, only the kinetic term survives since $F = 0$:"

WRITE:
$$L_{\text{red}} = \frac{k}{2\pi}\, v\dot{u}$$

SAY: "So $u$ is a coordinate on $S^1$ and its conjugate momentum is $p_u = kv/2\pi$. Since $v$ also has period $2\pi$, we get $p_u \sim p_u + k$. Quantizing:"

WRITE:
$$\psi_r(u) = e^{iru}, \quad r = 0, 1, \ldots, k-1$$

*Box the result:*
$$\boxed{\dim\, \mathcal{H}_{U(1),k}(T^2) = k}$$

SAY: "Exactly $k$ states. No local excitations, just $k$ topologically protected ground states. For the Laughlin $\nu = 1/k$ state, this is the $k$-fold ground-state degeneracy on the torus — the hallmark of topological order."

**Min 22-23: The TQFT functor**

SAY: "This is the full TQFT structure. Chern-Simons defines a functor:"

WRITE (panel right, permanent):
$$\Sigma \longmapsto \mathcal{H}_{G,k}(\Sigma), \qquad M_{\text{closed}} \longmapsto Z_k(M) \in \mathbb{C}$$

SAY: "Surfaces get finite-dimensional Hilbert spaces, closed 3-manifolds get complex numbers, and cobordisms compose correctly. Gauge invariance + metric-free action + Hilbert-space finiteness — all three signatures of a TQFT, all consequences of writing $\varepsilon^{\mu\nu\rho}$ instead of $g^{\mu\nu}$."

WRITE (below):
$$\dim\, \mathcal{H}_{SU(2),k}(T^2) = k+1$$

---

### Minutes 23-25: Handoff to Helena

**Min 23-24: Summary and bridge**

SAY: "Let me collect what we've established." *Gesture at the three permanent panels.*

"One: the CS action uses no metric, so the theory is topological. Two: quantum consistency forces integer level — a discrete, nonperturbative constraint. Three: Wilson loops give topological invariants — linking numbers for abelian theory, the Jones polynomial for $SU(2)$. Four: the Hilbert space on a surface is finite-dimensional, with dimension fixed by the topology and the level."

**Min 24-25: Handoff**

SAY: "All of this is the internal structure of the theory. But why should a physicist care? Because nature uses it. The same level $k$ that quantizes the gauge coupling also fixes the Hall conductance, the anyon braiding phase, and the ground-state degeneracy. Helena will now show you exactly how the effective theory connects to experiment."

*Step aside. Hand chalk to Helena.*

---

## Anticipated Questions with Prepared Answers

### Q1: "Why does the cubic term vanish for $U(1)$?"

**Answer:** For $G = U(1)$, the connection is just a real-valued 1-form — there are no nonabelian structure constants. Algebraically, $A \wedge A = 0$ because a 1-form wedged with itself vanishes when there's no Lie-algebra matrix structure to absorb the antisymmetry (or equivalently, $[A, A] = 0$). So the CS form reduces to $A \wedge dA$, and $F = dA$ (no quadratic term). The level quantization then comes from a different mechanism — summing over nontrivial bundles rather than large gauge transformations wrapping $\pi_3$.

### Q2: "What's the physical meaning of the shifted level $k+2$ (or $k + h^\vee$)?"

**Answer:** The shift $k \to k + h^\vee$ (with $h^\vee = 2$ for $SU(2)$, $= N$ for $SU(N)$) is a one-loop quantum renormalization. At the classical level the action has coefficient $k$. When you regulate the path integral — specifically, when you account for the framing anomaly of the Wilson loop — the effective coupling that enters physical observables is the shifted level. This is why the Jones polynomial appears at $q = e^{2\pi i/(k+2)}$ rather than $e^{2\pi i/k}$. In the quantum Hall context, this shift is typically absorbed into the definition of the effective theory, so it doesn't appear explicitly.

### Q3: "How does the finite Hilbert space dimension relate to the Atiyah-Segal axioms from Ch. 3?"

**Answer:** The Atiyah-Segal axioms require that a TQFT assigns a finite-dimensional vector space to each spatial slice. We proved in Ch. 3 (Corollary 3.1) that finite-dimensionality is not an extra assumption — it follows from the snake identities / duality axiom. The existence of evaluation and coevaluation maps built from the cylinder cobordism forces $Z(\Sigma)$ to be finite-dimensional. CS theory satisfies this: the constraint $F_\Sigma = 0$ kills all local modes, leaving a finite-dimensional quantization of the flat-connection moduli space. So the physical mechanism (flatness constraint) and the axiomatic requirement (duality forces finiteness) are two sides of the same coin.

---

## Timing Notes

| Section | Minutes | Pace notes |
|---------|---------|------------|
| Setup | 0-3 | **Normal pace.** Establish notation clearly. Don't rush the metric-free point — it's the conceptual core. |
| Level quantization | 4-10 | **Slow down at min 5-7** during the winding-number chain. This is the technical showpiece; give the audience time to absorb each line. **Speed up slightly at min 9-10** for the generalization remarks — these are informational, not essential to follow. |
| Wilson loops | 11-18 | **Normal pace min 11-14.** The abelian linking formula is straightforward. **Slow down at min 14-16** for the Jones polynomial bridge — state it as a punchline, not a derivation. **Can speed through min 16-18** (the $S$-matrix formula) if running behind; this is optional detail. |
| Hilbert space | 19-23 | **Fastest writing section** — the canonical analysis is clean and sequential. Slow down at **min 22** for the boxed result and its physical interpretation. This is the line that connects directly to Helena's material. |
| Handoff | 23-25 | **Deliberate, summary pace.** No new equations. Gesture at the board. End cleanly. |

**If running short:** Cut min 16-18 (the $S$-matrix computation) and simply state the Hopf link result. This saves 2 minutes.

**If running long:** The generalization remarks at min 9-10 can be condensed to one sentence ("Same argument for any simple $G$ with the right trace normalization"). This saves 1 minute.

**Buffer:** The handoff section (23-25) has built-in flexibility — the summary can expand or contract depending on remaining time.
