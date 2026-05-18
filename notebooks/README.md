# Notebooks

This folder contains the Google Colab notebooks used to generate the figures and empirical results reported in the thesis. Each notebook is self-contained and can be executed in Google Colab using locked empirical values from `results/empirical_results.json`.

## Contents

| Notebook | Generates | Thesis Reference |
|---|---|---|
| `figure_09_rf_vs_xgboost_generation.ipynb` | Figure 9 | Section 5.2 (RF vs XGBoost comparison) |
| `figure_10_confusion_matrix_generation.ipynb` | Figure 10 | Section 5.2 (Random Forest confusion matrix) |
| `figure_11_baseline.ipynb` | Figure 11 | Section 5.3.1 (Baseline AI-NIDS performance) |
| `figure_12_qca_generation.ipynb` | Figure 12 | Section 5.3.2 (QCA-integrated pipeline) |
| `figure_13_comparison_generation.ipynb` | Figure 13 | Section 5.3.3 (Baseline vs QCA comparison) |
| `figure_B1_scalability_generation.ipynb` | Figure B.1 | Appendix B.1 (Scalability stress test) |
| `figure_B2_noise_generation.ipynb` | Figure B.2 | Appendix B.2 (Noise resilience evaluation) |

## How To Run

Each notebook is independent and can be executed in any order:

1. Open the notebook in Google Colab
2. Mount Google Drive when prompted
3. Run all cells (Runtime → Run all, or Ctrl+F9)
4. The generated PNG figure saves to your Google Drive

## Empirical Data Source

All notebooks use **locked empirical values** corresponding to the experimental data reported in Chapter 5 of the thesis. The complete dataset of measurements is stored in `results/empirical_results.json`, which serves as the single source of truth for all numerical values.

This approach ensures:
- ✅ Perfect reproducibility across execution environments
- ✅ Identical figures regardless of Colab session
- ✅ Direct mapping between figure values and thesis prose

## Technical Stack

- **Python 3** (Google Colab default runtime)
- **matplotlib** — figure generation
- **numpy** — numerical operations
- **GridSpec** (matplotlib.gridspec) — multi-panel layouts with broken y-axis

## Original Experimental Pipeline

The notebooks in this folder generate **figures only** using locked values. The full experimental pipeline (VeReMi dataset preprocessing, Random Forest training, ML-DSA-65 cryptographic verification, scalability and noise testing) was conducted separately. The empirical outputs from those experiments are recorded in `results/empirical_results.json`.

## Dataset Acknowledgement

This work uses the publicly available **VeReMi dataset** (van der Heijden et al., 2018) and **VeReMi Extension** (Kamel et al., 2020), with a stratified 70/30 train/test split methodology described in Chapter 4 of the thesis.
