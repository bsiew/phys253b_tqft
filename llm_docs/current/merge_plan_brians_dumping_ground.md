---
created_at: "2026-05-05T00:00:00-04:00"
updated_at: "2026-05-05T18:07:21-04:00"
generated_by: "claude-code"
timestamp_source: "agent_clock"
updated_by: "claude-code"
---

# Merge Plan: `brians_dumping_ground/` → `253b_final_paper/`

**Status: EXECUTED 2026-05-05.** `brians_dumping_ground/` no longer exists.

Goal: eliminate `brians_dumping_ground/` as a separate namespace. Everything useful moves into the shared project structure; provenance-only material goes to a single archive folder.

## What was done

- `plan/` → top-level `253b_final_paper/plan/` (as-is, with archive subdir from earlier pruning)
- `references/` → `253b_final_paper/literature/` (textbook PDFs, style refs, placeholder dirs)
- `paper_to_implement/` substantive files → `253b_final_paper/source_tex/` (6 files + README)
- `paper_to_implement/` placeholders → `plan/archive/paper_to_implement_placeholders/`
- Empty dirs + old READMEs removed
- `brians_dumping_ground/` deleted

## Next step: tex_docs consolidation

See `llm_docs/current/tex_consolidation_proposal.md` for the plan to resolve the `part*` vs `ch*` file overlap inside `tex_docs/`.

---

## 1. Destination Map

After the merge, `253b_final_paper/` looks like:

```
253b_final_paper/
├── tex_docs/                      (unchanged — active chapters + figures)
├── llm_docs/                      (unchanged — current + archive + logs + reference)
├── style_guide_docs/              (unchanged)
├── plan/                          ← NEW top-level home for all planning
│   ├── plan_of_attack.tex         ← the master plan document
│   ├── tasks/                     ← active task prompts (stages VI, VII, appendices, ch14-16)
│   ├── stages/                    ← active stage files (VI, VII, IVb)
│   ├── notes/                     ← verification_matrix, author_split, bib shopping list, trim log
│   ├── presentation/              ← scripts + cheat cards (when written)
│   └── archive/                   ← completed task/stage files + guide
├── references/                    ← NEW top-level home for PDFs + style refs
│   ├── textbook/                  ← 25 PDFs from Brian's dump
│   ├── style/                     ← hdr.tex/bib, springer.tex/bib
│   ├── experiments/               ← (placeholder, for future PDFs)
│   └── reviews/                   ← (placeholder)
├── source_tex/                    ← NEW: Brian's legacy standalone TeX (provenance)
│   ├── chern_simons_theory.tex    ← 1835-line standalone (differs from chern_simons_body.tex)
│   ├── chern_simons_theory.bib
│   ├── main.tex                   ← Brian's original multi-chapter skeleton
│   ├── preamble.tex
│   ├── appB_frobenius.tex         ← 61-line appendix draft (differs from ch04)
│   ├── appD_bf_zn.tex             ← 64-line appendix draft
│   └── README.md                  ← explains provenance
├── CLAUDE.md
├── README.md
├── BSIEW_README.md
└── REORGANIZATION_SUMMARY.md
```

---

## 2. Move Operations

### 2a. `plan/` — the active planning tree

The entire `brians_dumping_ground/plan/` directory becomes `253b_final_paper/plan/`.

```
mv brians_dumping_ground/plan  →  plan/
```

No file edits needed. The `COMPLETED_WORK_GUIDE.md` already explains the archive subdirectories.

### 2b. `references/` — PDFs and style docs

```
mv brians_dumping_ground/references/textbook/   →  references/textbook/
mv brians_dumping_ground/references/style references/  →  references/style/
mv brians_dumping_ground/references/experiments/ →  references/experiments/
mv brians_dumping_ground/references/reviews/     →  references/reviews/
```

The `style_guide_docs/` directory at the project root already contains Helena's style examples (`pspec.tex`, `gt.md`, etc.) — keep that separate. The `references/style/` folder holds Brian's `hdr.tex`/`springer.tex` formatting references, which are a different thing (citation formatting + math conventions to match).

### 2c. `source_tex/` — Brian's legacy standalone TeX

These are the original standalone drafts Brian brought in. They differ slightly from what's now in `tex_docs/` (the `chern_simons_theory.tex` is 1835 lines vs `chern_simons_body.tex` at 1780; `appB_frobenius.tex` has 61 lines of content not in ch04; `appD_bf_zn.tex` has 64 lines not elsewhere).

```
mv brians_dumping_ground/paper_to_implement/chern_simons_theory.tex  →  source_tex/
mv brians_dumping_ground/paper_to_implement/chern_simons_theory.bib  →  source_tex/
mv brians_dumping_ground/paper_to_implement/main.tex                 →  source_tex/
mv brians_dumping_ground/paper_to_implement/preamble.tex             →  source_tex/
mv brians_dumping_ground/paper_to_implement/appB_frobenius.tex       →  source_tex/
mv brians_dumping_ground/paper_to_implement/appD_bf_zn.tex           →  source_tex/
```

The remaining `paper_to_implement/` files are 5-line placeholders (`ch01_intro.tex`, `ch14_outlook.tex`, `appA_category.tex`, `appC_cs_level.tex`, `appE_tee.tex`) and `tqft_review.bib` (363 lines — a subset of the 545-line active bib). These can be deleted outright.

### 2d. `figures/` — empty placeholder

`brians_dumping_ground/figures/` contains only a README pointing to `paper/figures/README.md` (which itself doesn't exist in this tree). Active figures already live in `tex_docs/figures/`. Delete.

### 2e. Top-level READMEs

- `brians_dumping_ground/README.md` — archive into `source_tex/README.md` (provenance context).
- `brians_dumping_ground/paper_to_implement/README.md` — fold into `source_tex/README.md`.

### 2f. Delete `brians_dumping_ground/`

After all moves complete, the directory should be empty and can be removed.

---

## 3. Files to Delete (pure duplicates or empty placeholders)

| File | Reason |
|------|--------|
| `paper_to_implement/ch01_intro.tex` | 5-line placeholder; `tex_docs/part1_01_introduction.tex` supersedes |
| `paper_to_implement/ch14_outlook.tex` | 5-line placeholder; `tex_docs/ch16_outlook.tex` supersedes |
| `paper_to_implement/appA_category.tex` | 5-line placeholder |
| `paper_to_implement/appC_cs_level.tex` | 5-line placeholder |
| `paper_to_implement/appE_tee.tex` | 5-line placeholder; `tex_docs/app_e_tee.tex` supersedes |
| `paper_to_implement/tqft_review.bib` | Subset of `tex_docs/tqft_observables_unresolved_refs.bib` |
| `figures/README.md` | Points to nonexistent path; active figs in `tex_docs/figures/` |
| `references/README.md` | Will be replaced by new `references/README.md` |

---

## 4. Conflicts / Decisions Needed

### 4a. `chern_simons_theory.tex` (1835 lines) vs `chern_simons_body.tex` (1780 lines)

These are different versions of the same document. The `REDUNDANCY_AND_IMPROVEMENT_PLAN.md` recommends gutting Sections 2-3 of the CS body (the forms re-derivation). The 1835-line source version preserves Brian's original standalone document.

**Decision:** Keep both for now. `source_tex/chern_simons_theory.tex` is the unedited original; `tex_docs/chern_simons_body.tex` is the active working copy. When the redundancy fix happens (Phase 1 of the improvement plan), the source version is the provenance reference.

### 4b. `appB_frobenius.tex` and `appD_bf_zn.tex`

These have 61 and 64 lines respectively — short appendix drafts that may contain material not yet in `ch04_frobenius.tex` or `ch06_bf.tex`. Worth preserving in `source_tex/` for the appendix-writing tasks (AA_1, AD_1).

### 4c. Style references vs style_guide_docs

Two different things:
- `references/style/hdr.tex` + `springer.tex` = Brian's formatting/math convention examples
- `style_guide_docs/` = Helena's prose examples (pspec, gt, qft, qhe problem-set style)

Keep both, separate locations.

---

## 5. Execution Order

1. Create destination dirs: `plan/`, `references/`, `source_tex/`
2. `mv brians_dumping_ground/plan/ plan/`
3. `mv brians_dumping_ground/references/textbook/ references/textbook/`
4. `mv brians_dumping_ground/references/style\ references/ references/style/`
5. `mv` experiment/review placeholder dirs into `references/`
6. Move 6 substantive TeX files into `source_tex/`
7. Write `source_tex/README.md` (combine both legacy READMEs)
8. Delete the 8 pure-placeholder files
9. Verify `brians_dumping_ground/` is empty; remove it
10. Update `CLAUDE.md` if any paths are referenced (check)
11. Update `migration_plan_2026-05-04.md` references to `brians_dumping_ground/plan/tasks/`

---

## 6. Post-Merge State

After this merge:
- **One planning tree** at `253b_final_paper/plan/` containing all active tasks + notes + archived completed work
- **One reference library** at `253b_final_paper/references/` with all PDFs
- **Brian's original TeX** preserved in `source_tex/` for provenance diffs
- **No more `brians_dumping_ground/`** namespace — everything is under the shared project
- The `REDUNDANCY_AND_IMPROVEMENT_PLAN.md` recommendations can be acted on from this merged state
