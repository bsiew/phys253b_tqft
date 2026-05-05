# Task 11.2 — Chapter 11 §11.2 Laughlin State and Effective $U(1)_m$ Chern–Simons

- **Status:** pending
- **Owner:** Helena
- **Duration:** 2 hours
- **Stage:** [IV](../stages/stage_IV_partII_A.md)

## Goal

From the Laughlin wavefunction $\Psi_{1/m} = \prod_{i<j}(z_i - z_j)^m \exp(-\sum |z_i|^2/4\ell_B^2)$, derive the effective long-wavelength theory as $U(1)_m$ Chern–Simons. Explicitly verify $\sigma_{xy} = e^2/(mh)$ by integrating out the emergent gauge field against an external background.

## Content

1. **Laughlin wavefunction** for $\nu = 1/m$, $m$ odd.
2. **Composite-fermion / flux-attachment argument.** Each electron is dressed with $m$ flux quanta, giving free composite fermions at effective $\nu = 1$, then re-introducing the flux as an emergent $U(1)$ gauge field at CS level $m$.
3. **Effective Lagrangian** $\mathcal{L} = (m/4\pi) a \wedge da + (1/2\pi) a \wedge dA_{\text{ext}}$ where $a$ is the emergent gauge field and $A_{\text{ext}}$ is the physical electromagnetic field.
4. **Integrating out $a$** (the equation of motion gives $a = -A_{\text{ext}}/m$, plug back in):
   $\mathcal{L}_{\text{eff}} = -(1/4\pi m) A_{\text{ext}} \wedge dA_{\text{ext}}$
   which yields Hall conductance $\sigma_{xy} = e^2/(mh)$.
5. **Cross-reference CS chapter.** The $U(1)_k$ action with $k = m$ is the CS chapter's Example `ex:U1-action`.

## Acceptance criteria

- Derivation in full; $\sigma_{xy}$ emerges from the calculation.
- Cross-reference CS chapter.
- ~3 pages.

## References

- Laughlin 1983, Tong *QHE* Ch 3.
- CS chapter Example `ex:U1-action`.
