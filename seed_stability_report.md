# Seed Stability Report

- Timestamp: `2026-06-12T13:49:22+05:30`
- Step: `18`
- Source of truth: `competition_workbench.ipynb`
- Goal: check whether the promoted CatBoost configuration is stable across alternative random seeds

## Setup

- Fixed folds: `StratifiedKFold(n_splits=5, shuffle=True, random_state=42)`
- Fixed feature pipeline: current workbench preprocessing
- Model under test: tuned CatBoost from step 17
- Tested seeds: `2025, 42, 777, 999, 1234`

## Results

| Seed | OOF ROC-AUC | Mean Fold ROC-AUC |
| --- | ---: | ---: |
| 2025 | 0.842536 | 0.842171 |
| 42 | 0.810399 | 0.838112 |
| 777 | 0.825884 | 0.839931 |
| 999 | 0.836691 | 0.839519 |
| 1234 | 0.837852 | 0.841793 |

## Decision

- Best seed by OOF ROC-AUC: `2025`
- Best seed by mean fold ROC-AUC: `2025`
- No alternative seed improved validation over the current promoted seed.
- The tuned CatBoost configuration is not showing seed sensitivity that justifies promotion to a different seed.

## Action Taken

- Left `competition_workbench.ipynb` unchanged.
- Left `submission.csv` unchanged.
- Left `experiments.csv` unchanged.

