# Build Route

Canonical compile route for the paper. Decided 2026-05-03 (Task 1.10).

## Route: Overleaf (browser), source lives locally

- **Source of truth:** the local repo at `c:\Users\sjybr\Documents\Harvard\Academics\Junior spring\Physics 253b\Physics 253b final project\`.
- **Authoring:** Brian works entirely in `.tex` files locally. Claude and Codex edit these files directly.
- **Compilation and preview:** Overleaf in the browser. The project is uploaded there and recompiled when a visual check is needed.
- **Handoff medium:** `.tex` files. Brian and Helena exchange tex rather than PDF.

## Owner

Brian. Helena mirrors via shared Overleaf project (once created) or by being emailed the tex files.

## Bibliography route

`paper/tqft_review.bib` lives in the same Overleaf project as `paper/main.tex`. Overleaf compiles with `latexmk` by default, which runs `pdflatex -> bibtex -> pdflatex -> pdflatex` automatically. No separate `bibtex` invocation required.

## Local fallback

None at the moment. `pdflatex`, `latexmk`, and `biber` are not on this machine's PATH. If Overleaf is unavailable, the fallback is to install MiKTeX locally, but that is an emergency-only path.

## Known tool limitations

1. **No local compile check before upload.** An error in a `.tex` file is caught when Overleaf recompiles, not at edit time. Mitigation: commit small edits, upload often.
2. **Claude cannot validate compilation.** All Claude / Codex editing steps write `.tex` source; actual correctness of the PDF output is confirmed by Brian running the Overleaf compile.
3. **No automated `biber --validate-datamodel`** step available locally. Treat Task 14.5's "bibliography validation clean" acceptance criterion as "Overleaf compiles without bibliography errors in its log."

## Typical compile loop (what "compile" means in this plan)

1. Brian edits `.tex` files locally.
2. Brian drags the project folder (or a modified subtree) into Overleaf, or uses Overleaf's GitHub integration / dropbox sync if enabled later.
3. Overleaf runs `latexmk` automatically.
4. Brian reads the compiled PDF in the Overleaf browser view; reads the log if there are errors.
5. If errors: Brian returns to local editing and describes the log message to Claude / Codex for a fix, or fixes directly.

## Acceptance-criteria interpretation

Whenever a later task says "compile cleanly" or "no undefined references," read it as: **Overleaf's `latexmk` compile produces a PDF with no error-level messages in its log, and zero `LaTeX Warning: Reference ... undefined` warnings.**

## Helena sync

Helena receives `.tex` files from Brian by email or shared Overleaf link. She edits in whatever she prefers (probably also Overleaf) and returns `.tex`. No binary assets (PDFs of drafts) are the canonical handoff — source only.

## Figure assets

Per `paper/figures/README.md`, scanned hand-drawn figures live as `.pdf` in `paper/figures/` and are uploaded to Overleaf alongside the tex. TikZ figures are inline source in the relevant chapter `.tex` file or sourced via `\input{figures/<name>}`.
