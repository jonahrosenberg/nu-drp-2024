# Numbered Increasing (1,2)-Trees and the Euler Zigzag Numbers

An expository write-up produced for the **Directed Reading Program (DRP)** at
**Northwestern University**, in collaboration with graduate mentor **Noah Wisdom**
(Spring 2024).

## Overview

The note proves a clean combinatorial identity: the number of *numbered
increasing (1,2)-trees* on $n$ vertices equals the $n$-th **Euler zigzag number**
$E_n$ (OEIS [A000111](https://oeis.org/A000111): $1, 1, 1, 2, 5, 16, 61, 272, \dots$).

A *numbered increasing (1,2)-tree* is an increasing rooted tree in which every
non-leaf vertex has one or two children, with vertices labeled $1, 2, \dots, n$
so that labels strictly increase along every root-to-leaf path (trees equivalent
under reorientation are identified).

### Main result

$$f(n) = E_n,$$

where $f(n)$ counts the distinct numbered increasing (1,2)-trees on $n$ vertices.

The proof sets up the exponential generating function

$$y = \sum_{n \ge 1} f(n)\,\frac{x^n}{n!},$$

splits a tree by the structure at its root to derive the differential equation

$$y' = 1 + y + \tfrac{1}{2}y^2,$$

and verifies that $y = \sec x + \tan x - 1$ is its solution — recovering the
classical generating function $\sec x + \tan x$ for the Euler numbers.

## Files

| File | Description |
| --- | --- |
| [`drp.tex`](drp.tex) | LaTeX source of the typeset write-up |
| [`drp.pdf`](drp.pdf) | Compiled PDF of the write-up |
| [`handwritten-drp-notes.pdf`](handwritten-drp-notes.pdf) | Scanned handwritten working notes, including the small tree examples |

## Building

Compile the LaTeX source with any standard TeX distribution:

```sh
pdflatex drp.tex
```

The source uses only common packages (`geometry`, `amsmath`, `amssymb`,
`amsthm`, `enumitem`), so no extra setup is required.

## Acknowledgments

Written as part of the Northwestern University Directed Reading Program, with
mentorship from Noah Wisdom.
