# Paper Structure Visual Roadmap

## Narrative Arc

```
┌─────────────────────────────────────────────────────────────────┐
│                    THE STORY THIS PAPER TELLS                    │
└─────────────────────────────────────────────────────────────────┘

    You already know QFT (Schwartz-level)
                  ↓
    Topological structure appears: instantons, θ-term, anomalies
           [Section II: Ordinary QFT]
                  ↓
    What if topology became CENTRAL instead of peripheral?
                  ↓
    Need language: differential forms, gauge connections
           [Section III: Minimal toolkit]
                  ↓
    Chern-Simons action emerges from anomaly descent
           [Section IV: CS from anomalies]
                  ↓
    ┌──────────────────────────────────────────┐
    │     HEART: Chern-Simons Theory          │
    │  [Sections V-VI: Classical + Quantum]   │
    │                                          │
    │  V: Flat connections, level k∈ℤ,       │
    │     Wilson loops                         │
    │  VI: Quantization → H(Σ), functorial    │
    │      emergence                           │
    └──────────────────────────────────────────┘
                  ↓
    This is a TQFT: formalize with Atiyah-Segal axioms
           [Section VII: Functorial TQFT]
                  ↓
    ┌──────────────────────────────────────────┐
    │   PAYOFF: Physical Applications         │
    │   [Section VIII: FQHE, anyons, edges]   │
    │                                          │
    │   Shows WHY topological reformulation   │
    │   makes physics computable              │
    └──────────────────────────────────────────┘
                  ↓
    What is and isn't topological? Clarify boundaries
           [Section IX: Contrasts]
                  ↓
    Why should you care? What does TQFT enable?
           [Section X: Outlook]
```

## The 10 Sections

```
┌──────────────────────────────────────────────────────────────────┐
│ I. INTRODUCTION                                    [2-3 pages]    │
│    Status: WRITE LAST                                            │
│    Purpose: Frame physics problem, state 3 key questions         │
└──────────────────────────────────────────────────────────────────┘
                               ↓
┌──────────────────────────────────────────────────────────────────┐
│ II. TOPOLOGICAL STRUCTURES IN ORDINARY QFT       [10-15 pages]   │
│     Status: NEW WRITING NEEDED                                   │
│     Purpose: Bridge from Schwartz - you know this already        │
│     Content: Instantons, θ-term, anomalies, Wilson loops,       │
│              monopoles → "but theory still has local dynamics"   │
└──────────────────────────────────────────────────────────────────┘
                               ↓
┌──────────────────────────────────────────────────────────────────┐
│ III. MATHEMATICAL TOOLKIT                         [~5 pages]     │
│      Status: EXTRACT minimal from topology_review.tex            │
│      Purpose: Brief conventions, not mini-textbook               │
│      Content: Forms, Lie groups, connections (just basics)       │
│      Note: Detailed treatments moved to sections where used      │
└──────────────────────────────────────────────────────────────────┘
                               ↓
┌──────────────────────────────────────────────────────────────────┐
│ IV. CHERN-SIMONS FROM ANOMALY DESCENT            [15-20 pages]   │
│     Status: REORGANIZE from differential_forms_v2.tex            │
│     Purpose: Show how CS emerges physically                      │
│     Content: Anomaly descent → transgression → CS action         │
│     Sources: v2 (base) + Brian (rigor) + anomalies_boundaries   │
└──────────────────────────────────────────────────────────────────┘
                               ↓
┌──────────────────────────────────────────────────────────────────┐
│ V. CLASSICAL SOLUTIONS, LEVEL QUANTIZATION       [15-20 pages]   │
│    Status: MERGE from synthesis + dense + Brian                 │
│    Purpose: Global structure of CS theory                        │
│    Four layers:                                                  │
│      1. Classical: F_A = 0                                       │
│      2. Global: π₃(G) → k ∈ ℤ                                   │
│      3. Phase space: M_flat(M,G)                                │
│      4. Observables: Wilson loops, linking                       │
└──────────────────────────────────────────────────────────────────┘
                               ↓
┌──────────────────────────────────────────────────────────────────┐
│ VI. QUANTIZATION AND FUNCTORIAL EMERGENCE        [10-15 pages]   │
│     Status: EXTRACT from Brian + dense torus calculation         │
│     Purpose: Show H(Σ) assignment → functorial structure         │
│     Content: Phase space on Σ, quantization, torus example,     │
│              functorial perspective emerging                     │
└──────────────────────────────────────────────────────────────────┘
                               ↓
┌──────────────────────────────────────────────────────────────────┐
│ VII. FUNCTORIAL TQFT (ATIYAH-SEGAL)              [2-3 pages]    │
│      Status: WRITE NEW (brief!)                                  │
│      Purpose: Formalize what CS already does                     │
│      Content: Bordism category, functor axioms, "this codifies  │
│               what we computed in Section VI"                    │
└──────────────────────────────────────────────────────────────────┘
                               ↓
┌──────────────────────────────────────────────────────────────────┐
│ VIII. PHYSICAL APPLICATIONS (FQHE)              [25-30 pages]   │
│       Status: REORGANIZE using FQHE_v2.tex as backbone          │
│       Purpose: CASH OUT THE FORMALISM - show explanatory power  │
│       Five parts:                                                │
│         1. FQHE puzzle and Laughlin response                    │
│         2. Fractional charge and anyonic braiding               │
│         3. Anomaly inflow and edge modes                        │
│         4. Torus degeneracy and K-matrix                        │
│         5. Nonabelian roadmap (brief)                           │
│       Note: THIS IS THE HEART - longest section                 │
└──────────────────────────────────────────────────────────────────┘
                               ↓
┌──────────────────────────────────────────────────────────────────┐
│ IX. CONTRASTS AND LIMITS                          [8-10 pages]   │
│     Status: EXTRACT Maxwell-CS + WRITE comparisons              │
│     Purpose: Clarify "topological QFT" vs "topological features"│
│     Content: CS is TQFT; Maxwell-CS is NOT; YM+θ is NOT;       │
│              instantons/monopoles are topological objects       │
│              but in non-topological theories                     │
│     Slogan: "Ordinary QFT + topological sectors ≠ TQFT"        │
└──────────────────────────────────────────────────────────────────┘
                               ↓
┌──────────────────────────────────────────────────────────────────┐
│ X. OUTLOOK                                        [3-5 pages]    │
│    Status: WRITE LAST                                            │
│    Purpose: Why should QFT student care?                         │
│    Content: What TQFT enables, broader landscape, open questions│
│    Message: TQFT reorganizes gauge theory, makes protected      │
│             observables computable, provides organizing language │
└──────────────────────────────────────────────────────────────────┘
```

## Migration Priority Flowchart

```
START HERE: Review planning documents
     ↓
┌────────────────────────────────────────┐
│ PRIORITY 1: Strongest existing content │
└────────────────────────────────────────┘
     ↓
┌─────────────────────┬─────────────────────┬────────────────────┐
│ Section VIII        │ Section IV          │ Sections V & VI    │
│ (FQHE)              │ (CS from anomalies) │ (Classical+Quant)  │
│ Use FQHE_v2         │ Use diff_forms_v2   │ Merge 3 sources    │
│ ~25-30 pages        │ ~15-20 pages        │ ~25-35 pages total │
└─────────────────────┴─────────────────────┴────────────────────┘
     ↓
┌────────────────────────────────────────┐
│ PRIORITY 2: Extraction/reorganization   │
└────────────────────────────────────────┘
     ↓
┌──────────────────────────┬──────────────────────────┐
│ Section III              │ Section IX               │
│ (Minimal toolkit)        │ (Contrasts)              │
│ Extract from topo_review │ Extract MCS + write comp │
│ ~5 pages                 │ ~8-10 pages              │
└──────────────────────────┴──────────────────────────┘
     ↓
┌────────────────────────────────────────┐
│ PRIORITY 3: New writing (short pieces) │
└────────────────────────────────────────┘
     ↓
┌──────────────────────────┬──────────────────────────┐
│ Section II               │ Section VII              │
│ (Topo structures in QFT) │ (Functorial TQFT)        │
│ Survey, new content      │ Brief, 2-3 pages         │
│ ~10-15 pages             │ ~2-3 pages               │
└──────────────────────────┴──────────────────────────┘
     ↓
┌────────────────────────────────────────┐
│ PRIORITY 4: Bookends (write last)      │
└────────────────────────────────────────┘
     ↓
┌──────────────────────────┬──────────────────────────┐
│ Section I                │ Section X                │
│ (Introduction)           │ (Outlook)                │
│ Frame after content done │ Synthesize organizing    │
│ ~2-3 pages               │ power, ~3-5 pages        │
└──────────────────────────┴──────────────────────────┘
     ↓
┌────────────────────────────────────────┐
│ Quality control + integration + compile │
└────────────────────────────────────────┘
```

## Content Flow: From Archive to New Structure

```
ARCHIVED FILES:                    NEW SECTIONS:

topology_review.tex         →  III (minimal) + distribute rest
                                 to V (π₃), VI (symplectic), 
                                 VII (bordisms)

differential_forms_v2.tex   →  IV (main content base)

chern_simons_synthesis.tex  →  V (pedagogical narrative)

dense_derivation.tex        →  V, VI (calculations) + throughout
                                 (worked examples)

anomalies_boundaries.tex    →  IV (anomaly inflow) + 
                                 VIII (FQHE applications) +
                                 IX (Maxwell-CS contrast)

FQHE_throughline_v2.tex     →  VIII (main backbone)

brian_chern_simons.tex      →  V, VI (mathematical rigor) +
                                 throughout (supplements)

chern_simons_review.tex     →  VIII (K-matrix) + IX (contrasts)
```

## Page Budget (target ~100-120 pages total)

```
Section   Pages    Type                  Status
───────────────────────────────────────────────────────────
I         2-3      Bookend              Write last
II        10-15    New survey           New writing
III       5        Minimal toolkit      Extract
IV        15-20    Reorganize           Strong source
V         15-20    Merge                Strong sources
VI        10-15    Extract              Strong sources
VII       2-3      New brief section    New writing
VIII      25-30    Reorganize           HEART, strong source
IX        8-10     Extract + write      Good source
X         3-5      Bookend              Write last
───────────────────────────────────────────────────────────
Total     95-121   ✓ Within target
```

## Key Relationships

```
        MOTIVATES
II ──────────────→ IV ──────────────→ V, VI
    "Topological      "CS emerges"      "CS structure"
     structure in
     ordinary QFT"
                           ↓
                      FORMALIZES
                           ↓
                         VII
                    "Functorial
                     TQFT"
                           ↓
                       APPLIES
                           ↓
                        VIII
                   "FQHE, anyons,
                    edge modes"
                           ↓
                      CLARIFIES
                           ↓
                         IX
                  "What is/isn't
                   topological"

    I (Intro) frames the entire arc
    X (Outlook) synthesizes the payoff
```

## Timeline Visual

```
Week 1-3: Priority 1 (strong content migration)
│████████████████████│ Section VIII (FQHE backbone)
│████████████████│    Section IV (CS from anomalies)
│██████████████████│  Sections V, VI (merge multiple sources)

Week 3-4: Priority 2 (extraction/reorganization)
│████████│            Section III (minimal toolkit)
│████████│            Section IX (contrasts)

Week 4: Priority 3 (new writing)
│██████│              Section II (survey)
│██│                  Section VII (brief functorial)

Week 4-5: Priority 4 (bookends)
│███│                 Section I (intro)
│███│                 Section X (outlook)

Week 5: Quality control
│████│                Notation audit, cross-refs, figures, compile

Week 5-6: Integration
│██│                  Wrapper, bibliography, final compile
```

## Status Check Visual

```
✅ COMPLETE:
├─ Structure created (10 stub files)
├─ Old files archived
├─ Planning documents written
└─ Migration instructions prepared

⏳ IN PROGRESS:
└─ [Next: Begin Priority 1 migration]

⬜ TODO:
├─ Priority 1 sections
├─ Priority 2 sections
├─ Priority 3 new writing
├─ Priority 4 bookends
├─ Quality control
└─ Final integration
```

You are here: ⬆ Ready to begin Priority 1 content migration
