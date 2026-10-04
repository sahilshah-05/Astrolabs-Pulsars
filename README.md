# Astrolabs-Pulsars: Pulsar Timing Analysis

Time-series analysis of pulsar pulse times-of-arrival (TOAs) to search for periodic timing anomalies that could indicate a planetary-mass companion.

![Python](https://img.shields.io/badge/Python-3.x-blue) ![SciPy](https://img.shields.io/badge/SciPy-non--linear%20least%20squares-orange) ![Status](https://img.shields.io/badge/status-completed-green)

## Overview

Pulsars are rapidly rotating neutron stars whose pulses arrive with extraordinary regularity. A planet orbiting a pulsar makes the star wobble around the system's centre of mass, which shows up as a small, periodic variation in the pulse arrival times. This project analyses just over a year of TOA data to look for that signature.

**Goal:** identify periodic anomalies in the timing residuals and fit a model that describes them.

**Key results:** Orbital Period, P = 0.09070627837842128 ± 0.00000001425450874, Reduced Chi Squared χ2 = 2.283

## Methods

1. **Data processing:** Handled over a year of TOA data for PSR J1719-143 using Tempo2 to produce timing residuals against a baseline timing model.
2. **Phase-folding:** Folded the residuals at candidate periods to reveal periodic structure, with wrap-around functions to correct systematic timing discrepancies across phase boundaries.
3. **Model fitting:** Fitted a periodic model to the residuals using non-linear least-squares minimisation (`scipy.optimize`), recovering parameters with uncertainties.
4. **Interpretation:** The sharpness of the minima curve suggests a well-constrained orbital period and compared with the actual orbital period thevalue does not overlap with the optimal period. This could be a consequence of assuming a Kelperian orbit. Periodic waves occur when the body orbits in circular motion, not accounting for imperfect orbits (elliptical) with eccentricity. 

## Repository structure

```
Astrolabs-Pulsars/
├── Data/          # Input TOA data and timing files  [describe the files, e.g. .tim / .par]
├── Submissions/   # Analysis scripts, figures and write-up  [describe, e.g. main notebook/script]
└── README.md
```

## Getting started

### Requirements

- Python 3.9+
- [Tempo2](https://bitbucket.org/psrsoft/tempo2) (only needed to regenerate residuals from raw TOAs)
- Python packages: `numpy`, `scipy`, `matplotlib`

```bash
git clone https://github.com/sahilshah-05/Astrolabs-Pulsars.git
cd Astrolabs-Pulsars
pip install numpy scipy matplotlib
```


## Skills demonstrated

- Time series analysis and periodicity detection
- Non-linear least-squares model fitting (SciPy)
- Data cleaning and transformation pipelines
- Scientific visualisation (Matplotlib)
- Working with astronomical timing data and Tempo2

## Context

Completed as part of Space Research/Astro Project module at the University of Birmingham (October-December 2025).

## Author

**Sahil Shah**, [GitHub](https://github.com/sahilshah-05) · [LinkedIn](https://linkedin.com/in/sms-sahilshah/)
