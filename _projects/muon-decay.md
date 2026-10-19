---
title: "Muon decay electron spectrum"
category: "HEP · Monte Carlo"
tags: ["HEP", "Monte Carlo"]
featured: true
status: "public repository"
summary: "A Monte Carlo study of the electron-energy spectrum in free negative-muon decay, with and without an order-alpha radiative correction."
image: "/assets/images/muon-spectrum-radiative.png"
image_alt: "Histogram of the simulated electron energy spectrum with radiative corrections."
caption: "Project output: simulated electron-energy spectrum with the radiative term enabled."
repo: "https://github.com/estivengrx/monte-carlo-particle-decay"
tools: ["Python", "NumPy", "SciPy", "Matplotlib", "Monte Carlo", "pytest", "LaTeX"]
math: true
---
## Context

The project studies the electron-energy distribution from free negative-muon decay,
\(\mu^- \rightarrow e^- + \bar{\nu}_e + \nu_\mu\). It compares the leading spectrum
with a spectrum that includes the documented order-\(\alpha\) radiative contribution.

## Approach

The analysis uses acceptance-rejection sampling. The main driver performs repeated
sampling runs for both correction settings and combines the accepted events for
histograms. The repository includes the analysis script, notebook, report, plots,
and test-oriented code.

## Results

The output shows a visible change in the simulated electron-energy distribution
when the radiative term is included. The repository README reports historical
histogram-bin summaries, not fitted peak estimates. This is a free-muon
calculation: it is not a complete bound-muon or nuclear model, and the global
envelope used by the rejection sampler still requires the verification described
in the source README.

## What I learned

This project made the connection between a differential decay spectrum, a
sampling algorithm, numerical diagnostics, and reproducible figure generation
concrete. It also made the limits of a result part of the result.

