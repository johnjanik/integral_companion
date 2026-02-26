# A Companion to *Table of Integrals, Series, and Products*

A LaTeX reference document providing **physics and mathematics applications** for every section of Gradshteyn and Ryzhik's *Table of Integrals, Series, and Products* (7th edition, 2007).

## What This Is

Gradshteyn-Ryzhik (G&R) is the standard reference table of integrals used across physics, engineering, and mathematics. It tells you *what* an integral evaluates to. This companion tells you **why you might need it**---where each integral, identity, or special function arises in practice.

For each topic group in G&R, the companion provides:

- **Physics applications** (2--4 per group): concrete problems from quantum mechanics, electrodynamics, statistical mechanics, fluid dynamics, optics, general relativity, and more.
- **Mathematics applications** (1--3 per group): connections to analysis, algebra, number theory, topology, and combinatorics.
- **Index entries**: over 5,200 hierarchical entries linking concepts to the G&R sections where the relevant formulas appear.
- **Bibliography**: 33 references to foundational papers and textbooks.

## Coverage

| G&R Section | Topic | Companion File |
|-------------|-------|----------------|
| 0 | Introduction | `sections/sec00_introduction.tex` |
| 1 | Elementary Functions and Finite Sums | `sections/sec01_elementary.tex` |
| 2 | Indefinite Integrals of Elementary Functions | `sections/sec02_indefinite_elementary.tex` |
| 3--4 | Definite Integrals of Elementary Functions | `sections/sec0304_definite_elementary.tex` |
| 5 | Indefinite Integrals of Special Functions | `sections/sec05_indefinite_special.tex` |
| 6--7 | Definite Integrals of Special Functions | `sections/sec0607_definite_special.tex` |
| 8--9 | Special Functions | `sections/sec0809_special_functions.tex` |
| 10 | Vector Field Theory | `sections/sec10_vector_field.tex` |
| 11 | Algebraic Inequalities | `sections/sec11_algebraic_ineq.tex` |
| 12 | Integral Inequalities | `sections/sec12_integral_ineq.tex` |
| 13 | Matrices and Quadratic Forms | `sections/sec13_matrices.tex` |
| 14 | Determinants | `sections/sec14_determinants.tex` |
| 15 | Norms | `sections/sec15_norms.tex` |
| 16 | Ordinary Differential Equations | `sections/sec16_odes.tex` |
| 17 | Integral Transforms | `sections/sec17_transforms.tex` |
| 18 | Z-Transform | `sections/sec18_ztransform.tex` |

## Building the PDF

Requires a TeX Live (or equivalent) installation with `pdflatex`, `biber`, and `makeindex`.

```bash
pdflatex integrals_and_their_use.tex
biber integrals_and_their_use
makeindex integrals_and_their_use
pdflatex integrals_and_their_use.tex
pdflatex integrals_and_their_use.tex
```

The final PDF is approximately 370 pages. Three passes of `pdflatex` are needed for cross-references, bibliography back-references, and index page numbers to settle.

A pre-built PDF (`integrals_and_their_use.pdf`) is included in the repository for convenience.

## How to Use It

**As a G&R supplement.** When you look up an integral in G&R, check the corresponding section here to see where that integral appears in physics and mathematics. The index is the fastest entry point---search for a concept (e.g., "hydrogen atom", "Fourier transform", "Selberg integral") and follow the page references.

**As a survey of applications.** Each section can be read independently as a tour of how a particular class of integrals connects to research problems. For example, the section on definite integrals of exponentials (G&R 3.3--3.4) covers everything from Gaussian path integrals to the Sommerfeld expansion for degenerate electron gases.

**As a teaching resource.** The applications provide "why does this matter?" context for integral calculus, special functions, and mathematical methods courses.

## Project Structure

```
integrals_and_their_use.tex    Main document (inputs all sections)
references.bib                 Bibliography (33 entries)
sections/                      Per-section LaTeX files (16 files)
```

## License

This work is provided for educational and research purposes.

## References

- I. S. Gradshteyn and I. M. Ryzhik, *Table of Integrals, Series, and Products*, 7th ed., edited by A. Jeffrey and D. Zwillinger. Academic Press, 2007.
- NIST Digital Library of Mathematical Functions, https://dlmf.nist.gov/
