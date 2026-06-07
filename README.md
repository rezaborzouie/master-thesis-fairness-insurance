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


## Data

The empirical analysis is based on a local CSV version of the French motor third-party liability frequency dataset `freMTPL2freq`, which is widely used in actuarial and insurance-pricing research. The dataset is documented in the `CASdatasets` collection and is also available through public mirrors such as Kaggle. The original source is a French motor third-party liability portfolio and provides a realistic empirical base for an insurance-pricing application.

For the purposes of this thesis, the original dataset is transformed into a **synthetic enriched fairness setting**. This means that the base insurance dataset is real, but the protected attribute and fairness structure used in the empirical analysis are synthetically constructed for methodological illustration.

The repository does not necessarily include the original local CSV file. If data-sharing restrictions apply, the repository contains the code and documentation needed to understand and reproduce the workflow, but not the raw dataset itself.

### Data notes
- Base dataset: `freMTPL2freq`
- Format used in the thesis: local CSV version
- Protected attribute: synthetic
- Fairness setting: synthetic enriched fairness setting
- Raw dataset in repository: not included if sharing restrictions apply
