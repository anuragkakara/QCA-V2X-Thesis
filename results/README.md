# Results

This folder contains the empirical data generated during the experimental evaluation of the QCA framework.

## Contents

### `empirical_results.json`

A comprehensive JSON file containing all measured values from the experiments described in Chapter 5 of the thesis. This file serves as the **single source of truth** for all numerical values reported throughout the thesis.

The file is structured into the following sections:

| Section | Maps To Thesis Section |
|---|---|
| `dataset` | Section 4.4 (VeReMi distribution) |
| `baseline_ai_nids_only` | Section 5.2 / 5.3.1 (Random Forest performance) |
| `qca_extended_pipeline` | Section 5.3.2 (QCA-integrated metrics) |
| `ml_dsa_65_standalone` | Section 4.5 (PQC implementation) |
| `urllc_compliance` | Section 5.3.3 (Framework verdict) |
| `noise_resilience` | Appendix B.2 (Noise reliability) |
| `scalability_test` | Appendix B.1 (Scalability) |
| `rf_vs_xgboost_comparison` | Section 5.2 (Algorithm selection) |

## Dataset Source

All experiments use the publicly available **VeReMi dataset** (van der Heijden et al., 2018) with the 70/30 stratified train/test split methodology described in Chapter 4 of the thesis.

## Relationship To Figures And Notebooks

The figure generation notebooks in the `notebooks/` folder load values **directly from this JSON file** to render the thesis figures. This ensures perfect consistency between:

- ✅ The numerical values reported in thesis prose
- ✅ The values shown in thesis tables
- ✅ The values plotted in thesis figures
- ✅ The data preserved in this empirical results file

## Date Of Experiments

Experiments conducted: **2026-05-03**

## Format

JSON format (UTF-8) for machine readability and easy parsing in Python, R, or any modern data analysis tool. The file can be loaded with:

```python
