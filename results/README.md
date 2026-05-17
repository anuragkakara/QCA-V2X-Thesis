# Results

This folder contains the empirical data generated during the experimental evaluation of the QCA framework.

## Contents

### `empirical_results.json`

A comprehensive JSON file containing all measured values from the experiments described in Chapter 5 of the thesis. The file is structured into the following sections:

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

All experiments use the publicly available VeReMi dataset (van der Heijden et al., 2018) with the 70/30 stratified train/test split methodology described in Chapter 4.

## Reproducibility

These results were generated using the notebooks in the `notebooks/` folder. To reproduce, run the corresponding notebook in Google Colab with the VeReMi dataset.

## Date Of Experiments

Experiments conducted: 2026-05-03

## Format

JSON format (UTF-8) for machine readability and easy parsing in Python, R, or any modern data analysis tool.
