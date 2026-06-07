# Fairness in Insurance Pricing

Code accompanying the master's thesis:

**Fairness in Insurance Pricing: Comparing Model-Based Fairness Metrics with Customer-Perceived Fairness Dimensions in Motor Insurance**

## Author
Reza Borzouei

## Overview
This repository contains the code used for the empirical analysis, fairness-metric computation, and figure generation in the thesis.

## Repository structure
- `notebooks/` or `code/`: main analysis scripts / notebooks
- `figures/`: generated figures used in the thesis
- `requirements.txt`: Python package requirements
- `data/`: not included if the original dataset cannot be shared

## Reproducibility
The empirical analysis is based on a synthetic enriched fairness setting built on top of a motor-insurance dataset.

If the original dataset is not publicly shareable, this repository provides the code and documentation, but not the raw data.

## How to run
1. Install the required packages from `requirements.txt`
2. Open the main notebook or script
3. Run the code in sequence to reproduce the analysis and figures

## Notes
The outputs in the thesis are predicted claim probabilities / pricing-relevant risk scores, not full commercial premiums.