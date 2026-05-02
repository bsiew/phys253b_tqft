# 253b Final Paper Writing Style Guide

## Target Voice

The target style is a mathematically explicit physics review: the prose should be physically motivated, but the arguments should not hand-wave the differential-geometric steps. The model is the Brian Chern-Simons draft's best mode: definitions before use, explicit calculations when signs or normalizations matter, and short interpretive paragraphs after equations that explain why the computation is physically doing work.

## Local Rules

- Begin each major section with the physical question it answers.
- Keep section and subsection titles short: 2-4 word topic labels when possible, with 5 words as the normal maximum.
- Do not put the explanation, thesis, or pedagogical sentence in the title; put it in the opening paragraph.
- Introduce mathematical machinery only when it earns its place in the physics.
- Prefer "we compute" and then actually compute; avoid "one can show" for sign-sensitive or normalization-sensitive claims.
- Use theorem-like language sparingly: statement, calculation, consequence.
- Keep equations close to the prose that explains them.
- Preserve convention warnings around orientation, trace normalization, framing, boundary terms, and spin-structure caveats.
- Separate global structure from local algebra: first tell the reader what object is being controlled, then do the local computation.
- Do not let polish erase the causal chain from action to observable.

## Section Shape

1. Physical motivation.
2. Definitions and conventions.
3. Calculation or derivation.
4. Interpretation.
5. Scope caveat or forward pointer.

## Citation Style

Use prose citations for standard background. Reserve source notes or footnotes for imported formulas, convention-sensitive identities, or historical claims.

## Density Target

Dense is good when it is useful density: every displayed equation should either define an object, prove a structural fact, compute an observable, or fix a convention. Decorative equations should be cut.

## Expansion Target

For the 253b final paper, do not let modularization become summarization. A module may be shorter than a source draft only when it has intentionally delegated material to another module. Across the full `tex_docs` set, the output should preserve the source reviews' useful derivation density: component/form translations, gauge-transformation algebra, level-quantization normalization, torus quantization, Wilson-loop Gaussian integration, framing, anomaly inflow, and K-matrix response.

When expanding, add:

- one explicit calculation for every convention-sensitive claim,
- one physical interpretation paragraph after every major calculation,
- one caveat paragraph when a result depends on compactness, spin structure, trace normalization, orientation, or boundary conditions,
- one cross-reference to the module where the same object reappears physically.

## Pedagogical Rewrite Target

The preferred dense style is teacherly rather than encyclopedic. Each derivation should tell the reader what is being computed, perform the calculation with enough intermediate structure to track signs and normalizations, and then explain what the result buys physically. Avoid repeated derivations: keep one worked version and point to it from shorter appearances.

Flag figures directly in TeX with comments of the form `% FIGURE FLAG [F-id]: ...`, and mirror serious candidates into the figure inventory.
