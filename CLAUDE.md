# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A LaTeX mathematical reference document structured as a companion to the Gradshteyn-Ryzhik (G&R) table of integrals. The main document covers 19 sections (0–18) spanning finite sums, integrals, special functions, vector field theory, matrices, ODEs, and integral transforms.

## Build Commands

Full compilation requires three tools run in sequence (run twice for cross-references to settle):

```bash
pdflatex integrals_and_their_use.tex
biber integrals_and_their_use
makeindex integrals_and_their_use
pdflatex integrals_and_their_use.tex
pdflatex integrals_and_their_use.tex
```

## Key Files

- `integrals_and_their_use.tex` — Main source document (~1450 lines)
- `references.bib` — Bibliography (25 entries, BibTeX format)
- `integrals_and_their_use_NOEDITS.tex` — Earlier backup version of the main document

## LaTeX Architecture

- **Document class:** `article`
- **Bibliography:** `biblatex` with `biber` backend, `alphabetic` citation style, sorted by name-year-title
- **Index:** `imakeidx` package, hierarchical 2-column index
- **Section numbering:** Automatic numbering is suppressed (`secnumdepth=-1`); sections use explicit G&R-style numbering in heading text (e.g., `\section{0\quad Introduction}`, `\subsection{2.1\quad ...}`)
- **Page breaks:** Custom `\@afterheading` override with `\raggedbottom` to allow breaks between consecutive headings without vbox overflow
- **Math packages:** `amsmath`, `amssymb`, `bm`
- **Hyperlinks:** `hyperref` for PDF cross-references
