# QCA-V2X-Thesis

**Quantum Cryptography Authentication (QCA) Framework for V2X Networks**

This repository contains the code, empirical data, and figures supporting a Master's by Research thesis on V2X network security:

> *"Advancing Intrusion Detection in AI-based Vehicle-to-Everything (V2X) Networks: An Approach Involving Quantum Cryptography Authentication (QCA)"*

## Overview

The QCA framework proposes a layered "AI-first, Quantum-second" defence architecture for V2X (Vehicle-to-Everything) networks, addressing the latency paradox that arises when post-quantum cryptography is naively applied to safety-critical vehicular environments.

### Key Components

1. **AI-NIDS Behavioural Pre-Filter** — Random Forest classifier trained on the VeReMi dataset
2. **Post-Quantum Cryptographic Verification** — ML-DSA-65 signatures (NIST FIPS 204 standard)
3. **Layered Defence Pipeline** — End-to-end latency analysis against URLLC 10 ms safety threshold

## Key Empirical Findings

| Metric | Value |
|---|---|
| Random Forest Accuracy | 99.6277% |
| Random Forest Recall | 99.9626% |
| RF Inference Latency | 0.0091 ms |
| ML-DSA-65 Verification Latency | 1.6903 ms |
| QCA Pipeline Total Latency | 0.4348 ms |
| URLLC Budget Utilisation | 4.35% |
| Scalability Improvement (batch 100→10,000) | 18.6× |

## Repository Structure
Each subfolder contains its own README with detailed contents and usage instructions.

## Quick Start

To regenerate any figure from the thesis:

1. Open the corresponding notebook from the `notebooks/` folder in Google Colab
2. Mount Google Drive when prompted
3. Run all cells (Runtime → Run all)
4. The figure saves automatically to your Google Drive

All notebooks use locked empirical values from `results/empirical_results.json`, ensuring perfect reproducibility.

## Technical Stack

- **Language:** Python 3 (Google Colab default runtime)
- **ML Library:** scikit-learn (Random Forest, XGBoost) — used in the original experimental pipeline
- **Cryptography:** pqcrypto (ML-DSA-65 / CRYSTALS-Dilithium, NIST FIPS 204)
- **Visualisation:** matplotlib
- **Environment:** Google Colab
- **Dataset:** VeReMi (Vehicular Reference Misbehavior dataset)

## Dataset Acknowledgement

This work uses the **VeReMi dataset** (van der Heijden et al., 2018) and the **VeReMi Extension** (Kamel et al., 2020), which are publicly available benchmarks for V2X misbehaviour detection research.

## Reproducibility

The figure generation notebooks in this repository load values directly from `results/empirical_results.json`. This separation between empirical data and visualisation logic ensures:

-  Figures can be regenerated without re-running the full experimental pipeline
-  All values shown in figures exactly match the thesis prose and tables
-  Examiners can verify the relationship between data and visualisation independently

The original experimental pipeline (VeReMi preprocessing, model training, ML-DSA-65 verification, scalability and noise testing) is documented in detail in Chapter 4 of the thesis, with all measurements recorded in `results/empirical_results.json`.

## Licence

This work is released under the MIT Licence. See the [LICENSE](LICENSE) file for details.
