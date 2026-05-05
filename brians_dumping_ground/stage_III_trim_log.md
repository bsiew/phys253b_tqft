# Stage III Trim Log

Use this file to record what was cut from Chapters 6-8, especially Chapter 8, and where any overflow material was moved.

## Chapter 2 trim (Task 2.7, 2026-05-04)

Compiled at 20 pp on Overleaf — about 2× the 10-page target. Trim applied by user agreement:

1. **Theorem 2.5.6 ($F^g = g^{-1}Fg$) full proof cut** — four-step "Step 1 / Step 2 / Step 3 / Step 4" derivation replaced with a one-paragraph `\begin{proof}[Sketch]` that names the three mixed-term cancellations and points forward to the CS chapter (where the $\omega_{CS}$ version is derived in full). Saves ~60 lines.
2. **Proposition 2.5.8 (non-abelian Bianchi) cut entirely** — no downstream `\ref` from any chapter. The identity is still stated in §2.3 as eq.~\ref{eq:nonabelian-bianchi} for completeness, but no derivation. Saves ~35 lines.
3. **Remark 2.5.7 ("four mixed terms") cut** — it was commentary on the proof we just cut. Saves ~5 lines.
4. **§2.5 "Bianchi identity" subsection cut** (the subsection heading itself). Saves 1 line.
5. **Step-N scaffolding purged globally** from Ch 2 (per user feedback that the "Step 1 / Step 2 / ..." pattern reads AI-generated).

Forward-pointer in §2.3 ("we will derive Bianchi in §2.5") rewritten to "we record it for completeness and move on".

File metrics:
- Before: 884 lines, 9136 words.
- After: 603 lines, 8394 words.
- Cut: 281 lines / 742 words / ~32% reduction.

Verification-matrix status:
- C.2.26 ($F^g = g^{-1}Fg$) changed from `derived-here` to `derived-elsewhere` (full derivation lives in CS chapter).
- C.2.27 (non-abelian Bianchi) changed from `derived-here` to `cut`.

Overleaf re-compile expected to land around 14 pp (20 pp × ~0.7, reflecting the 32% line reduction adjusted for the fact that line cuts are slightly less dense than page cuts). If still > 12 pp, next trims in priority order:
1. Merge §2.4.2 + §2.4.3 into a single subsection.
2. Shorten §2.3 conventions narrative.
3. Cut Example 2.1.4 ($\mathbb{R}^3$ divergence).



## Stage II label-conflict notes (feeds integration Tasks 14.4 / 14.11)

During Task 2.1 drafting, four labels in `paper/ch02_forms.tex` collided with identical labels in the archival `paper/chern_simons_body.tex` (Chapter 5). Ch 2's labels were renamed with a `ch2-` prefix to unblock the compile.

These collisions reflect real content duplication — both chapters derive the graded Leibniz rule and $d^2=0$. The final integration pass (Task 14.11 or 14.4) must resolve this, in one of two ways:

1. **Preferred:** rewrite Ch 5's §2 to cite Ch 2's results. Ch 5 becomes shorter; no duplicated proofs.
2. **Fallback:** leave Ch 5 standalone and strip the redundant proofs from Ch 2, keeping only the wedge-graded-commutativity and the Maxwell-Bianchi worked example. Ch 2 stays short but still provides a chapter-length home for the primer.

### Citation tightening opportunity (Task 14.10)

All Nakahara citations in `paper/ch02_forms.tex` are currently chapter-agnostic (`\cite{Nakahara2003GTP}` alone). The book does have clearly named chapters on differential forms, integration/Stokes, and de Rham theory, but the exact chapter numbers in the 2003 second edition were not verified at drafting time (PDF tool unavailable). Task 14.10 should open `references/textbook/Nakahara_GeometryTopologyandPhysics.pdf` and add `[Ch.~X]` qualifiers to the six Nakahara cites in `ch02_forms.tex` once verified. This is taste-work: the citations are correct as is, but chapter pointers help the reader.

### Affected labels currently in `paper/ch02_forms.tex`:

| Current (Ch 2) | Original that collided (CS body §2.1) |
|---|---|
| `eq:ch2-graded-comm` | `eq:graded-comm` |
| `lem:ch2-leibniz-nilpotent` | `lem:leibniz-nilpotent` |
| `eq:ch2-leibniz` | `eq:leibniz` |
| `eq:ch2-nilpotent` | `eq:nilpotent` |

### Content duplication between Ch 2 §2.3 and CS body §2.3 (2026-05-04)

The anti-Hermitian-convention setup, $A \wedge A = \tfrac{1}{2}[A_\mu, A_\nu]dx^\mu\wedge dx^\nu$ derivation, and $F_{\mu\nu} = \partial_\mu A_\nu - \partial_\nu A_\mu + [A_\mu, A_\nu]$ component formula are now in both `ch02_forms.tex` §2.3 and `chern_simons_body.tex` §2.3 (the "Lie-algebra-valued forms" subsection of the CS chapter). The Ch 2 version is the more careful exposition (Proposition 2.3.2 with named conventions, full proof of $A\wedge A$ via symmetric-antisymmetric decomposition, explicit Schwartz-comparison derivation).

Preferred integration: in the final pass, replace the CS-body §2.3 material with a short "we use the conventions of Chapter~\ref{ch:forms} §\ref{sec:anti-hermitian-conv}" pointer. This removes ~30 lines of duplication without touching any proof.

No new label collisions as of 2026-05-04, but the Ch 2 labels chosen in §2.3 deliberately avoid the CS-body names (`eq:A-components` vs CS's `eq:A-def`; `eq:F-nonabelian-components` vs CS's `eq:F-components`). These pairs can be unified in the integration pass once one version wins.

### Ch 2 §2.5 duplication with CS body (2026-05-04)

The gauge-transformation law $A^g = g^{-1}Ag + g^{-1}dg$, the identity $dg^{-1} = -g^{-1}(dg)g^{-1}$, the Maurer-Cartan equation $d\theta + \theta\wedge\theta = 0$, and the derivation $F^g = g^{-1}Fg$ now all appear in both `ch02_forms.tex` §2.5 and `chern_simons_body.tex` §2. The Ch 2 version is more thorough: Theorem~\ref{thm:F-transformation} works with every mixed term visible and the Bianchi identity is proved as Proposition~\ref{prop:nonabelian-bianchi}.

Integration-pass resolution: replace the CS body's §2.5 block with a pointer "we use the conventions and the transformation law established in §\ref{sec:gauge-transf}" and keep only the CS-specific $\omega_{\CS}$ gauge transformation (Proposition~\ref{prop:CS-gauge} in the CS body). This saves ~40 lines.

Deliberate label differentiations:

| Current (Ch 2) | CS body counterpart |
|---|---|
| `eq:gauge-A-2` | `eq:gauge-A` |
| `eq:F-transformation` | `eq:gauge-F` |
| `eq:dginv-lemma` | `eq:dginv` |
| `lem:maurer-cartan` | `lem:MC` |
| `eq:maurer-cartan` | `eq:MC` |
| `thm:F-transformation` | (no CS counterpart; CS only has the formula) |
| `prop:nonabelian-bianchi` | (no CS counterpart) |
