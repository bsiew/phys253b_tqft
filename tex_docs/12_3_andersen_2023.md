# Task 12.3 — Chapter 12 §12.3 Andersen 2023: Non-Abelian Braiding on a Superconducting Processor (Honesty Box)

- **Status:** pending
- **Owner:** Helena
- **Duration:** 90 min
- **Stage:** [V](../stages/stage_V_partII_B.md)

## Goal

Summarize the Andersen et al 2023 Google superconducting-processor experiment that implements non-abelian braiding of graph-vertex anyons. Frame correctly: this is a synthetic emulation on hardware, not a discovery of a natural non-abelian phase.

## Content

1. **Platform.** Superconducting qubit array programmed to realize the $\mathbb{Z}_2$ toric code + defects that carry non-abelian (Ising-like) braiding.
2. **What was demonstrated.** Initialization, braiding, and measurement of non-abelian anyons (specifically, graph vertices that realize Ising fusion rules).
3. **What was not demonstrated.** This is not a natural topologically ordered phase of matter; the Hamiltonian is programmed in software. Decoherence limits the fidelity of the braiding.

## Required honesty box

A tcolorbox or clearly-marked paragraph stating:

> This experiment realizes the braid-group algebra of non-abelian anyons on a quantum processor, but it is not a discovery of non-abelian topological order in a natural material. The distinction matters: natural topological order would provide passive protection from decoherence, whereas the synthetic realization relies on active error correction during the braiding protocol.

## Acceptance criteria

- Honesty box is prominent.
- Platform and demonstration described correctly.
- ~2 pages.

## References

- Andersen et al 2023, *Nature*.

## Risks

- **Mis-framing.** The public discourse around this experiment sometimes conflates emulation with discovery. Our honesty box is the corrective.
