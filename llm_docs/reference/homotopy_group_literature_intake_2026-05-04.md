---
created_at: "2026-05-04T20:08:48-04:00"
updated_at: "2026-05-04T20:08:48-04:00"
generated_by: "codex"
timestamp_source: "agent_clock"
project: "QFT"
source_note: "/Users/helenabrittain/Downloads/Homotopy Group Paper Search.md"
integration_target:
  - "PROJECTS/QFT/253b_final_paper/tex_docs/part1_02_mathematical_toolkit.tex"
  - "PROJECTS/QFT/253b_final_paper/tex_docs/part1_03_ordinary_to_chern_simons.tex"
---

# Homotopy Group Literature Intake

This note normalizes the reading list from `/Users/helenabrittain/Downloads/Homotopy Group Paper Search.md` into a helper-friendly intake batch for the QFT final paper. The main writing target is the chain

1. `\pi_3(G)` for compact simple simply connected Lie groups,
2. large gauge transformations on closed 3-manifolds,
3. winding-number shifts of the Chern-Simons action,
4. level quantization and its caveats.

## Primary non-arXiv sources

### Raoul Bott (1956)

**Title:** An application of the Morse theory to the topology of Lie-groups
**Why it matters:** Primary source for the corollary that `\pi_3(G)` is free abelian and equals `\mathbb{Z}` for compact connected simply connected simple `G`.
**Read depth:** close
**Links:** Numdam https://www.numdam.org/item/10.24033/bsmf.1472.pdf
**What to extract:**
- Exact wording of the `\pi_3(G)` corollary.
- How Bott passes from information about `\Omega G` to `\pi_3(G)`.
- Any assumptions on compactness, connectedness, simple versus semisimple, and simple connectedness.

### Raoul Bott (1954)

**Title:** On Torsion in Lie Groups
**Why it matters:** Short announcement preceding the 1956 paper; useful as a historical bridge if the review wants one sentence on the earlier result.
**Read depth:** skim
**Links:** PMC https://pmc.ncbi.nlm.nih.gov/articles/PMC527999/
**What to extract:**
- Whether it states the torsion-free or low-homology consequence in a compact way.
- Whether it is worth citing directly or only mentioning through Bott 1956.

### John Milnor (1963)

**Title:** Morse Theory, Part IV / Lie-group sections
**Why it matters:** Textbook-level explanation of Bott's Morse-theoretic method, useful for exposition even if not quoted as the main theorem source.
**Read depth:** targeted
**Links:** PDF mirror https://luis.impa.br/aulas/topdif/Milnor_MorseTheory.pdf
**What to extract:**
- A pedagogical sentence explaining why loop-space Morse theory sees `\pi_3(G)`.
- Any clean formulation suitable for a remark box or parenthetical explanation.

### Bott-Samelson (1958)

**Title:** The space of loops on a Lie group
**Why it matters:** Further development of the loop-space picture behind Bott's computation.
**Read depth:** skim
**Links:** Project Euclid landing page https://projecteuclid.org/journals/michigan-mathematical-journal/volume-5/issue-1/The-space-of-loops-on-a-Lie-group/10.1307/mmj/1028998010.full
**What to extract:**
- Whether this gives a cleaner citation for `H_*(\Omega G)` than Bott 1956.
- Whether it adds any language useful for the final-paper review.

### Bott-Samelson (1958)

**Title:** Applications of the theory of Morse to symmetric spaces
**Why it matters:** Natural sequel if the section wants one forward-looking sentence on the Bott-Samelson program beyond the compact group case.
**Read depth:** skim
**Links:** JSTOR landing page https://www.jstor.org/stable/2372843
**What to extract:**
- One sentence on the symmetric-space generalization, only if it strengthens the narrative.

### Garland-Raghunathan (1975)

**Title:** A Bruhat decomposition for the loop space of a compact group
**Why it matters:** Modernizes Bott's result via Bruhat decomposition and provides a bridge toward affine Grassmannians and loop groups.
**Read depth:** targeted
**Links:** PMC https://pmc.ncbi.nlm.nih.gov/articles/PMC388799/
**What to extract:**
- A one-sentence bridge from Bott to affine-Grassmannian language.
- Whether this is worth citing in the paper body or only keeping in reserve.

## arXiv / modern-adjacent sources

### Magyar (2007)

**Title:** Notes on Schubert classes of a loop group
**Why it matters:** Clean modern loop-group perspective on the Bott picture.
**Read depth:** targeted
**Links:** arXiv:0705.3826 https://arxiv.org/abs/0705.3826
**What to extract:**
- A short explanation of how `\Omega K` is reinterpreted via affine Grassmannians or Schubert cells.
- Any statement that clarifies why Bott's theorem still matters conceptually.

### Yun-Zhu (2009)

**Title:** Integral homology of loop groups via Langlands dual groups
**Why it matters:** Advanced modern reference on integral homology of loop groups.
**Read depth:** reserve
**Links:** arXiv:0909.5487 https://arxiv.org/abs/0909.5487
**What to extract:**
- Only use if the review wants a modern citation beyond Bott and Bott-Samelson.

### Jeffrey-Mare (2009)

**Title:** Real loci of based loop groups
**Why it matters:** Adjacent Bott-Samelson-style loop-group paper; more likely background than a main citation.
**Read depth:** reserve
**Links:** arXiv:0903.0840 https://arxiv.org/abs/0903.0840
**What to extract:**
- Only keep if it sharpens the based-loop-group narrative.

### Hepworth (2009)

**Title:** String Topology for Lie Groups
**Why it matters:** Continuation from Bott's loop-space story into free-loop-space/string-topology language.
**Read depth:** reserve
**Links:** arXiv:0905.1199 https://arxiv.org/abs/0905.1199
**What to extract:**
- Possible outlook sentence; probably not a core citation.

### Grbic-Terzic (2007)

**Title:** The integral Pontrjagin homology of the based loop space on a flag manifold
**Why it matters:** Based-loop-space homology in a nearby homogeneous-space setting.
**Read depth:** reserve
**Links:** arXiv:math/0702113 https://arxiv.org/abs/math/0702113
**What to extract:**
- Use only if the review expands from groups to flag manifolds.

### Jones-Rumynin-Thomas (2021)

**Title:** Compact Lie Groups and Complex Reductive Groups
**Why it matters:** Useful dictionary for compact/simple/simply connected language and normalization conventions.
**Read depth:** targeted
**Links:** arXiv:2109.13702 https://arxiv.org/abs/2109.13702
**What to extract:**
- Any compact statement clarifying the compact-group versus complexified-group dictionary.

### Stegemeyer (2021)

**Title:** On the String Topology Coproduct for Lie Groups
**Why it matters:** Recent string-topology continuation; likely background only.
**Read depth:** reserve
**Links:** arXiv:2109.10190 https://arxiv.org/abs/2109.10190
**What to extract:**
- Keep only if a recent continuation citation is wanted.

### Gotchev-Tsankov (2009)

**Title:** Simply connected compact Lie groups
**Why it matters:** Background on the structure of simple simply connected compact Lie groups.
**Read depth:** targeted
**Links:** arXiv:0901.2157 https://arxiv.org/abs/0901.2157
**What to extract:**
- Any compact structural statement useful for caveats around simple versus semisimple.

### Dobarro-Unal et al. (2025)

**Title:** Semi-Riemannian metrics on compact simple Lie groups
**Why it matters:** Not a core source, but explicitly restates the Bott theorem and may provide a very recent citation trail.
**Read depth:** reserve
**Links:** arXiv:2505.10635 https://arxiv.org/abs/2505.10635
**What to extract:**
- Only use if a contemporary citation is helpful; do not let it replace the primary sources.

## Integration priority

The likely paper-facing use of this batch is:

1. Chapter 2 `Homotopy and Winding`: add the `SU(2) \simeq S^3` generator story and state the Bott corollary for compact simple simply connected groups.
2. Chapter 3 `Yang-Mills Vacua and Large Gauge Transformations`: use `\pi_3(G)` to label large gauge sectors on closed 3-manifolds.
3. Chapter 3 `Level Quantization from Large Gauge Invariance`: make the assumptions and caveats explicit instead of writing `\pi_3(G)=\mathbb{Z}` with no qualifiers.
