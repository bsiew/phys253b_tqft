---
created_at: "2026-05-05T23:10:54-04:00"
updated_at: "2026-05-05T23:10:54-04:00"
generated_by: "claude-code"
updated_by: "claude-code"
timestamp_source: hook
---
# Brian — Cheat Card (Min 0-25)

## Board Layout

```
┌─ LEFT (permanent) ─────┐  ┌─ CENTER (erase twice) ──┐  ┌─ RIGHT (permanent after m4) ─┐
│ S_CS = (k/4π)∫ω_CS     │  │ [level quant. m4-10]     │  │ S[A^g]-S[A] = -2πk n(g)      │
│ ω_CS = Tr(A∧dA+⅔A³)   │  │ [Wilson loops m11-18]    │  │ e^{iS} inv ⟺ k∈ℤ            │
│ NO METRIC              │  │ [Hilbert space m19-23]   │  │ Σ ↦ H_{G,k}(Σ)              │
│ EOM: F = 0             │  │                          │  │ M ↦ Z_k(M)                   │
└─────────────────────────┘  └──────────────────────────┘  └───────────────────────────────┘
```

## Minute Checkpoints

| By min | You should be at |
|--------|-----------------|
| 3 | CS action written, metric-free point made, EOM on board |
| 5 | Gauge-transf shift written, winding number integral starting |
| 9 | **k∈ℤ boxed on right panel** — punchline landed |
| 12 | Wilson loop defined, starting abelian linking |
| 16 | Jones polynomial stated (don't derive, state as result) |
| 18 | S-matrix formula done — *skip this block if behind* |
| 22 | dim H(T²) = k boxed — connects to Helena's GSD |
| 25 | Handoff complete, chalk passed |

**If behind:** Cut min 16-18 (S-matrix). State Hopf result verbally. Saves 2 min.

## 3 Hardest Questions + Answers

**Q1: Level quantization for non-simply-connected G, or why π₃(G)=ℤ isn't the whole story?**
> The argument uses π₃(G)=ℤ for simple simply-connected G. For non-simply-connected groups (e.g. SO(3)=SU(2)/ℤ₂), the level quantization condition tightens — k must be even — because the allowed gauge transformations form a restricted subset. The key input is always H³(G,ℤ), which classifies the possible Chern-Simons terms.

**Q2: How exactly does the Jones polynomial emerge — is it a rigorous derivation?**
> Witten's 1989 argument is a physicist's derivation via path-integral surgery and the Verlinde formula — not a proof. The rigorous construction (Reshetikhin-Turaev '91) bypasses the path integral entirely, using the representation category of the quantum group U_q(sl₂) at q = e^{2πi/(k+2)}. The two approaches give the same invariant; the RT construction proves existence, Witten's gives physical intuition.

**Q3: Do you need a spin structure for CS theory?**
> For integer-level SU(N) on an oriented 3-manifold, no spin structure is needed — the action is well-defined with orientation alone. For U(1) CS at odd level, or for theories with fermions coupled, you do need a spin structure (technically a spin^c structure) to define the half-integer flux sectors. In the FQHE context Helena discusses, the underlying electrons provide the spin structure implicitly.

## Safety Phrases

- "That's a great question — let me state what the theory guarantees and flag where the subtlety lives..."
- "The short answer is [X]; the full story involves [Y] which we discuss in Section [N] of the paper."
- "Helena will address the physical side of that in her segment."
- "Let me write down the precise statement so we can be careful about it."
