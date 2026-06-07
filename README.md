# Fairness in Insurance Pricing

Code accompanying the master's thesis:

**Fairness in Insurance Pricing: Comparing Model-Based Fairness Metrics with Customer-Perceived Fairness Dimensions in Motor Insurance**

## Author
Reza Borzouei

## Thesis Overview
This repository contains the code used for the empirical analysis, fairness-metric computation, and figure generation for the master's thesis.

The thesis examines fairness in motor-insurance pricing from both a **model-based** and a **customer-oriented** perspective. Its main contribution is conceptual and methodological: it develops a structured framework for interpreting model-based fairness metrics in light of customer-perceived fairness dimensions such as:

- controllability
- logical relevance
- solidarity
- privacy
- transparency

The empirical analysis is used as an **illustrative application** of this framework in a **synthetic enriched fairness setting**.

## Empirical Design
The empirical analysis compares three model classes:

- **Restricted GLM**: parsimonious and more interpretable actuarial benchmark
- **Extended GLM**: richer but still structured actuarial specification
- **Boosting model**: more flexible machine-learning benchmark

For each model, the analysis compares three benchmark pricing schemes:

- **Best-estimate pricing**
- **Unawareness pricing**
- **Aware pricing**

The code evaluates predictive performance and model-based fairness outcomes across these specifications.

## Main Outputs
The repository reproduces the key empirical components of the thesis, including:

- data preparation for the synthetic enriched fairness setting
- estimation of restricted GLM, extended GLM, and boosting models
- construction of benchmark pricing schemes
- predictive-performance metrics:
  - AUC
  - log loss
  - Brier score
- fairness-related metrics and diagnostics:
  - demographic parity difference
  - Wasserstein distance
  - unawareness--aware gap
  - proxy-detectability diagnostic
  - equalized-odds ratio (secondary robustness metric)
- figure generation for the thesis

## Important Interpretation Note
The outputs in this repository are interpreted as **predicted claim probabilities** or **pricing-relevant risk scores**, **not** as full commercial premiums.

Although the thesis uses pricing terminology such as best-estimate, unawareness, and aware pricing, the empirical implementation is based on a binary fairness setting and should be interpreted accordingly.

## Data
The empirical analysis is based on a local CSV version of the French motor third-party liability frequency dataset `freMTPL2freq`, which is widely used in actuarial and insurance-pricing research. The dataset is documented in the `CASdatasets` collection and is also available through public mirrors such as Kaggle.

The original source is a French motor third-party liability portfolio and provides a realistic empirical base for an insurance-pricing application.

For the purposes of this thesis, the original dataset is transformed into a **synthetic enriched fairness setting**. This means:

- the **base motor-insurance dataset is real**
- the **protected attribute is synthetically constructed**
- the fairness structure is intentionally stylized for methodological illustration
- the empirical analysis is designed to study how model-based fairness metrics behave in a controlled setting

### Data Notes
- Base dataset: `freMTPL2freq`
- Format used in the thesis: local CSV version
- Main synthetic protected attribute: `SexVP`
- Main fairness-analysis target: `ClaimsVP`
- Weight variable: `Exposure`
- Raw dataset in repository: not included if sharing restrictions apply

If the original local CSV file is not publicly shareable, this repository provides the code and documentation, but not the raw dataset itself.

## Repository Structure
Typical repository contents include:

- `code/` or `notebooks/` — main analysis scripts / notebooks
- `figures/` — generated figures used in the thesis
- `requirements.txt` — Python package requirements
- `README.md` — repository overview and documentation

If a `data/` folder is absent, this means the original dataset is not redistributed through the repository.

## Reproducibility
The repository is intended to support transparency and reproducibility of the thesis workflow.

To reproduce the analysis:

1. Install the required Python packages from `requirements.txt`
2. Prepare the local dataset input if access is available
3. Run the main notebook or scripts in sequence
4. Generate the model outputs, fairness metrics, and thesis figures

Because the empirical design relies on a synthetic enriched fairness setting built on top of a local insurance dataset, full replication may require access to the underlying dataset or a locally prepared equivalent file.

## Scope and Limitations
This repository accompanies a thesis that uses an **illustrative synthetic enriched fairness setting**, not an observed portfolio with real protected-attribute data. Therefore:

- the metric magnitudes should be interpreted as illustrative
- the results are not direct evidence of actual market discrimination
- the repository supports the methodological and conceptual contribution of the thesis rather than a real-world causal claim about policyholder behavior

## Related Thesis Theme
The thesis argues that model-based fairness metrics are informative, but incomplete unless they are interpreted through broader customer-perceived fairness dimensions. The code in this repository supports the empirical side of that argument.

## Contact
For questions about the repository or the thesis, please contact the author through GitHub.
