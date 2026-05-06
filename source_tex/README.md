---
created_at: "2026-05-05T18:03:27-04:00"
updated_at: "2026-05-05T18:03:27-04:00"
generated_by: "claude-code"
updated_by: "claude-code"
timestamp_source: hook
---
# Source TeX (Brian's Legacy Standalone Drafts)

These are the original TeX files Brian brought into the project as standalone compilable documents. They predate the reorganized `tex_docs/` chapter structure.

## Contents

| File | Lines | Relationship to active `tex_docs/` |
|------|-------|-------------------------------------|
| `chern_simons_theory.tex` | 1835 | Original standalone version. Active working copy is `tex_docs/chern_simons_body.tex` (1780 lines, slightly trimmed). |
| `chern_simons_theory.bib` | 157 | Subset of `tex_docs/tqft_observables_unresolved_refs.bib`. |
| `main.tex` | 69 | Original multi-chapter skeleton with `\include` calls. Superseded by `tex_docs/tex_docs_ch02_ch13_app_e_wrapper_20260505.tex`. |
| `preamble.tex` | 152 | Original shared preamble. Conventions may differ from compile wrappers in `tex_docs/`. |
| `appB_frobenius.tex` | 61 | Short appendix draft with material not all present in `tex_docs/ch04_frobenius.tex`. Use for appendix task AA_1. |
| `appD_bf_zn.tex` | 64 | Short appendix draft with BF/Z_N lattice material. Use for appendix task AD_1. |

## When to consult these

- When resolving notation discrepancies between `tex_docs/chern_simons_body.tex` and the rest of the paper (this is the unedited original).
- When writing appendices B and D — the short drafts here may have content not yet migrated.
- For provenance: if you need to know "what did Brian's original document look like before any reorganization."

## Do not edit these files

They are archival. All active writing happens in `tex_docs/`.
