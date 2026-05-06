---
created_at: "2026-05-05T23:10:54-04:00"
updated_at: "2026-05-05T23:10:54-04:00"
generated_by: "claude-code"
updated_by: "claude-code"
timestamp_source: hook
---
# Helena — Cheat Card (Min 25-50)

## Board Layout

```
┌─ TOP (keep Brian's) ──────────────────────────────────────────────────────────┐
│  S_CS = (k/4π)∫ω_CS  [left]              k∈ℤ  [right, boxed]                 │
├─ BOTTOM-LEFT (your workspace) ────────────┬─ BOTTOM-RIGHT (erase Hopf link) ──┤
│ Laughlin ψ, effective action S[a;A]       │ Anyons: Q = (q/m)e               │
│ EOM: da = (1/m)dA                         │ φ_braid = 2π/m                   │
│ S_eff[A] = (1/4πm) A∧dA                  │ Experiment table                  │
│ σ_xy = e²/(mh)  ← BIG, BOXED            │ Nakamura / Bartolomei / Werkm.    │
└───────────────────────────────────────────┴────────────────────────────────────┘
```

## Minute Checkpoints

| By min | You should be at |
|--------|-----------------|
| 28 (m3) | Laughlin ψ written, effective action boxed, "k = m" arrow drawn |
| 32 (m7) | EOM derived, substitution done, **σ_xy = e²/(mh) boxed** |
| 35 (m10) | Hall conductance discussion wrapped, moving to right board |
| 39 (m14) | Fractional charge Q = e/3 boxed, starting braiding |
| 42 (m17) | φ = 2π/3 on board, summary triplet boxed, starting experiments |
| 46 (m21) | Nakamura + Bartolomei done, starting Werkmeister |
| 48 (m23) | Experiment table complete, starting closing |
| 50 (m25) | "Invariant → Lagrangian → Measured" on board. "Questions?" |

**If behind:** Cut Bartolomei to one sentence. Saves 90 sec.

## 3 Hardest Questions + Answers

**Q1: Is topological quantum computation actually feasible with abelian anyons?**
> No — abelian anyons (like ν=1/3 quasiparticles) give only phase gates, which aren't computationally universal. You need non-abelian anyons (e.g. ν=5/2 Moore-Read state, Ising anyons) for universal topological quantum computation. The abelian case demonstrates the principle — topologically protected information — but fault-tolerant computing requires the richer braid group representations of non-abelian theories.

**Q2: How robust are the experimental results — could the measured phases be non-topological artifacts?**
> The key control is universality: Nakamura (GaAs, Fabry-Perot) and Werkmeister (graphene, same geometry) get the same 2π/3 despite completely different band structures, disorder, and capacitances. A Coulomb artifact would depend on device geometry; a topological invariant doesn't. Additionally, the phase is discrete (jumps by exactly 2π/3 per quasiparticle), not continuously tunable — that discreteness is the hallmark of topological protection.

**Q3: Why use CS effective theory rather than solving the microscopic Hamiltonian directly?**
> The microscopic problem is an exponentially hard many-body Hamiltonian — no closed-form solution beyond Laughlin's trial wavefunction. The CS theory is the universal low-energy description: it captures all topological observables (Hall conductance, charge, braiding) in five lines of algebra, independent of microscopic details. It's the same logic as Landau theory — you don't need to solve the Ising model to predict universal critical exponents. The price is that non-universal quantities (gap size, edge velocity) require microscopic input.

## Safety Phrases

- "That's a great point — let me distinguish what the topological theory guarantees from what requires microscopic input..."
- "The honest answer is [X]. The theoretical expectation is [Y], and what's been measured is [Z]."
- "Brian's formalism gives the mathematical structure; what I'm showing is the physical instantiation."
- "We discuss that in detail in Section [N] of the paper — happy to elaborate after."
