# Task 5.1 — Chapter 5 Addendum: Witten–Jones Bridge Subsection

- **Status:** done
- **Priority:** important
- **Owner:** Brian
- **Duration:** 4 hours
- **Stage:** [II](../stages/stage_II_partI_A.md) (appended to Chapter 5, which already exists as a standalone compile target)

## Goal

The current `paper/chern_simons_theory.tex` already states that Wilson-loop expectation values of $SU(2)$ Chern–Simons on $S^3$ reproduce the Jones polynomial, but does not derive the bridge. Gemini (P3) and the review packet flagged that omitting the Witten–Jones connection entirely is a mistake given that it is the single most celebrated result in the TQFT literature. This task adds a compact 3–5 page bridge subsection to Chapter 5 (or a short appendix, depending on budget) linking CS Wilson loops to the Kauffman bracket / Jones polynomial.

**Not a standalone chapter. Not a full surgery derivation. A review-level bridge.**

## Content

1. **Where the Wilson loop expectation value lives.** Revisit Proposition `prop:topological` of the current CS chapter: $\langle W_{R_1}(C_1)\cdots W_{R_n}(C_n)\rangle$ is a framed link invariant.
2. **The Kauffman-bracket skein relation.** State $\langle L_+ \rangle = A \langle L_0\rangle + A^{-1}\langle L_\infty\rangle$ with the unknot normalization. Do not derive from scratch; cite Kauffman 1987 and Witten 1989.
3. **Identification with CS Wilson loops.** The skein relation is the $R$-matrix acting on two strands; for $SU(2)_k$ in the fundamental representation, the crossing matrix is $q^{1/2} \mathbb{1} + q^{-1/2} \varepsilon$ with $q = \exp(2\pi i / (k+2))$. Cite the computation.
4. **Jones polynomial emerges.** The framed link invariant $\langle W_\square(L)\rangle_{S^3}$ divided by $\langle W_\square(\text{unknot})\rangle_{S^3}$ is the Jones polynomial of $L$ at $q = e^{2\pi i/(k+2)}$, up to normalization.
5. **One worked example.** The Hopf link: $\langle W_\square(H_+)\rangle = \frac{\sin(2\pi/(k+2))}{\sin(\pi/(k+2))}$. Show this emerges from the skein + unknot normalization.
6. **Pointers to what we skip.** Full surgery presentation of 3-manifolds, Reshetikhin–Turaev category-theoretic construction — cite and move on.

## Placement decision

Two options:
- **Option A:** append as a new Section 8 of the current CS chapter (inside `chern_simons_theory.tex`, after the current TQFT section, before the summary).
- **Option B:** put in Appendix C alongside other CS technicalities.

**Default: Option A.** The bridge is short enough to live in-chapter and it's what the existing forward pointers in the CS chapter already promise.

## Acceptance criteria

- 3–5 pages inserted into the CS chapter or Appendix C.
- Skein relation stated, Jones identification made, Hopf-link worked.
- No full surgery derivation; citation-based for the technical inputs.
- CS chapter's existing "detailed derivation via surgery presentations of links is postponed to the next chapter" sentence is either updated to point at this bridge, or replaced with "we give a compact bridge here and cite Witten 1989 for the surgery derivation".

## Risks

- **Scope creep.** The Jones polynomial is famously fun to write about; resist doing the whole Kauffman-bracket combinatorics.
- **Page budget impact.** Adds 3–5 pp to Chapter 5. The revised master plan has Chapter 5 at 20–24 pp, so this fits.
- **Cross-reference to unused Chapter 6.** The current CS chapter points forward to "Chapter on CS and knot invariants." Update that pointer to refer to this bridge instead. Handled by Task 14.6.

## References

- Witten 1989 (primary).
- Kauffman 1987, "State models and the Jones polynomial" (skein relation).
- Guadagnini–Martellini–Mintchev 1989 (early CS computation).

## Why this is "important" rather than "core"

The paper is grade-acceptable without this bridge (Chapter 5 already mentions the result). But in Gemini's judgment, and mine, omitting it sacrifices one of the two strongest selling points of a TQFT review paper (the other being the FQH experimental anchor). Add if the Stage II schedule holds; cut if it slips.
