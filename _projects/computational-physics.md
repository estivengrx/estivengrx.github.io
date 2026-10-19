---
title: "Numerical physics notebooks"
category: "Numerical methods"
tags: ["Numerical methods"]
featured: true
status: "selected personal work"
summary: "Numerical studies of PDEs and quantum systems from my own work inside a larger computational-physics course repository."
image: "/assets/images/finite-difference-grid.svg"
image_alt: "Schematic finite-difference grid with Dirichlet boundary values."
caption: "A schematic of the finite-difference grid used in the Laplace notebook; the portfolio does not copy course figures."
repo: "https://github.com/estivengrx/computational_physics"
tools: ["Python", "NumPy", "Matplotlib", "Finite differences", "Fourier methods", "FEM"]
---
## Context

The public repository is a forked course archive. This page refers only to the
notebooks under `Estudiantes/Castrillon_0656`, not to other students' work or
course materials.

## Approach

One representative notebook solves a two-dimensional Laplace boundary-value
problem with a Jacobi finite-difference method, Dirichlet conditions, and a
Fourier-series comparison. The same personal folder includes work on diffusion,
the Schrodinger equation, finite elements, and FFT methods.

## Results

The finite-difference study compares numerical convergence with a series-based
reference and explores tolerance and iteration choices. The portfolio uses a
schematic figure here because the original notebooks contain course-context
material that should not be redistributed without a separate rights review.

The governing equation for the representative Laplace problem is

$$
\nabla^2 \phi =
\frac{\partial^2\phi}{\partial x^2}
\frac{\partial^2\phi}{\partial y^2}=0,
$$

and the Jacobi update replaces each interior value with the mean of its four
nearest neighbours:

$$
\phi_{i,j}^{(n+1)}
=\frac{1}{4}\left(
\phi_{i+1,j}^{(n)}+\phi_{i-1,j}^{(n)}
\phi_{i,j+1}^{(n)}+\phi_{i,j-1}^{(n)}
\right).
$$

## What I learned

These notebooks strengthened my understanding of discretization, boundary
conditions, convergence, and the practical role of visual diagnostics in
numerical physics.
