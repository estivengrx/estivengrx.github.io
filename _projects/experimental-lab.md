---
title: "Experimental physics measurements"
category: "Laboratory"
tags: ["Laboratory"]
featured: true
status: "public repository"
summary: "Selected undergraduate laboratory work covering counting, sensors, electronics, and statistical analysis of measurements."
image: "/assets/images/sound-speed-binned.png"
image_alt: "Binned measurements from a sound-speed and temperature experiment."
caption: "Binned output from the sound-speed and temperature measurement project."
repo: "https://github.com/estivengrx/physics-lab-experiments"
tools: ["Python", "Jupyter", "Arduino", "FPGA", "Sensors", "Statistical analysis"]
---
## Context

This is a collection of experimental-physics work at Universidad de Antioquia.
The portfolio view is intentionally narrower than the repository: it focuses on
measurement, acquisition, analysis, and particle-counting evidence rather than
reproducing an entire course archive.

## Approach

The repository contains work on Geiger counting, the photoelectric effect, Hall
magnetic-field measurements, sound-speed/temperature measurements, FPGA capacitor
charging, and sensor-based experiments. Data are acquired with laboratory
instrumentation or microcontrollers and then analyzed in Python notebooks.

## Results

The figure shows binned measurements from the sound-speed project. Other
experiments provide complementary evidence: counting statistics, calibration,
time-series analysis, and electronics interfacing. Exact values and uncertainty
claims belong to the corresponding notebooks, not to a generalized portfolio
summary.

For the temperature comparison, the classical ideal-gas model gives the
reference relationship

$$
v_{\mathrm{s}}(T)=\sqrt{\frac{\gamma R T}{M}},
$$

where the measured data are compared with the model rather than being treated
as an exact identity.

## What I learned

Experimental work taught me to keep acquisition choices, units, calibration,
uncertainty, and plots connected. It also showed why a clear data trail matters
as much as a final graph.
