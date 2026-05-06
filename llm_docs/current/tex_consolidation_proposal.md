---
created_at: "2026-05-05T00:00:00-04:00"
updated_at: "2026-05-05T18:05:19-04:00"
generated_by: "claude-code"
timestamp_source: "agent_clock"
updated_by: "claude-code"
---

# TeX Consolidation Proposal

## The Problem

`tex_docs/` currently has **three overlapping layers** of files:

1. **`ch*` files** (ch02–ch16 + chern_simons_body + app_e_tee) — the active chapter drafts from the BSIEW plan. These contain real content (600–1800 lines each for ch02–ch13; stubs with outlines for ch14–16).

2. **`part*` files** (part1_01 through part2_07) — the older 7-section structure from the May 1–2 reorganization. These are mostly subsection-plan headers (57–301 lines). `part2_05_response_2plus1d.tex` (301 lines) was the source that got migrated INTO `ch11_fqhe.tex` on May 4.

3. **`compile_*` wrappers** (compile_ch02 through compile_ch13 + compile_app_e_tee) — thin preamble+input wrappers that let each chapter compile standalone for proofing.

Plus `source_tex/` now holds Brian's unedited originals for provenance.

## The Redundancy

| `part*` file | Overlaps with | Status |
|---|---|---|
| `part1_01_introduction.tex` (57 lines) | No ch* counterpart | Pure TODO stub |
| `part1_02_mathematical_toolkit.tex` (118 lines) | `ch02_forms.tex` (781 lines) | Stub; ch02 is the real content |
| `part1_03_ordinary_to_chern_simons.tex` (111 lines) | `chern_simons_body.tex` (1780 lines) | Stub; body has all content |
| `part1_04_tqft_and_observables.tex` (119 lines) | `ch03_axiomatic.tex` + `ch04_frobenius.tex` | Stub; ch03/04 have content |
| `part2_05_response_2plus1d.tex` (301 lines) | `ch11_fqhe.tex` (529 lines) | **Source already migrated** into ch11 |
| `part2_06_sectors_3plus1d.tex` (116 lines) | `ch14_sectors_3plus1d.tex` (126 lines) | **Literal copy** with renumbering |
| `part2_07_defects_caveats_outlook.tex` (149 lines) | `ch15_defects_synthesis.tex` + `ch16_outlook.tex` | Split into ch15+16 on May 4 |

The `part*` files are **100% superseded**. Their content either:
- Was migrated into a `ch*` file (part2_05 → ch11), or
- Was copied verbatim (part2_06 → ch14, part2_07 → ch15+ch16), or
- Is just a subsection plan that the `ch*` file now contains in its header comments (part1_02–04)

The one exception is `part1_01_introduction.tex` — there's no `ch01_*` file. But the content is just a TODO stub.

## Proposed Solution

### Move `part*` files to archive

```
tex_docs/archive_part_files/
  part1_01_introduction.tex
  part1_02_mathematical_toolkit.tex
  part1_03_ordinary_to_chern_simons.tex
  part1_04_tqft_and_observables.tex
  part2_05_response_2plus1d.tex
  part2_06_sectors_3plus1d.tex
  part2_07_defects_caveats_outlook.tex
  tex_docs_main_wrapper_20260501.tex   (references the old part* structure)
```

### Keep in `tex_docs/` (the active working set)

```
tex_docs/
├── ch02_forms.tex                      Part I content
├── ch03_axiomatic.tex
├── ch04_frobenius.tex
├── ch05_chern_simons.tex               (16-line wrapper → chern_simons_body.tex)
├── chern_simons_body.tex               (the big 1780-line chapter)
├── ch06_bf.tex
├── ch07_dw.tex
├── ch08_gensym.tex
├── ch09_topological_order.tex          Part II content
├── ch10_anyons.tex
├── ch11_fqhe.tex
├── ch12_experiments.tex
├── ch13_tqc.tex
├── ch14_sectors_3plus1d.tex
├── ch15_defects_synthesis.tex
├── ch16_outlook.tex
├── app_e_tee.tex                       Appendix
├── compile_ch*.tex                     Standalone compile wrappers
├── tex_docs_ch02_ch13_app_e_wrapper_20260505.tex   Active full-paper wrapper
├── tqft_observables_unresolved_refs.bib
└── figures/
```

### The `chern_simons_body.tex` / `ch05_chern_simons.tex` situation

Currently `ch05_chern_simons.tex` is a 16-line stub that just says "this is the wrapper." The real content is in `chern_simons_body.tex`. Two options:

**Option A (rename):** Rename `chern_simons_body.tex` → `ch05_chern_simons.tex` (replacing the stub). This makes the naming consistent with ch02–ch16.

**Option B (keep split):** Leave as-is — the body file predates the chapter numbering scheme and some compile wrappers reference it directly. Less disruption but the naming inconsistency persists.

Recommend **Option A** after verifying which compile targets reference `chern_simons_body.tex`.

### What about `source_tex/`?

`source_tex/` stays as-is — it holds Brian's unedited originals for provenance diffs. No overlap with active `tex_docs/` after the `part*` archive.

## Decision Points

1. **Archive the `part*` files?** (Recommended: yes — they're fully superseded)
2. **Rename `chern_simons_body.tex` → `ch05_chern_simons.tex`?** (Cosmetic but makes the naming consistent)
3. **Create a `ch01_introduction.tex`?** The introduction stub currently lives only in `part1_01_introduction.tex`. If we archive the part files, we should create a `ch01_introduction.tex` (even if empty) so the numbering sequence isn't missing a file.
4. **Keep compile wrappers in the same dir or move to `tex_docs/compile/`?** They add clutter but are actively used.
