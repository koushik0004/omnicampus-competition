# Native CatBoost Categorical Processing Report

- Timestamp: `2026-06-12T14:21:58+0530`
- Step: `19`
- Source of truth: `competition_workbench.ipynb`
- Objective: evaluate whether CatBoost native categorical handling improves ROC-AUC over the current label-encoded pipeline

## Categorical Columns

- `Player_Type`
- `Position_Type`
- `Position`

## Setup

- Kept all accepted features from the current workbench.
- Kept the promoted Optuna CatBoost parameters from step 17.
- Kept the same `StratifiedKFold(n_splits=5, shuffle=True, random_state=42)` split.
- Compared against the current label-encoded CatBoost pipeline.

## Baseline

- OOF ROC-AUC: `0.842536`
- Mean Fold ROC-AUC: `0.842171`

## Native CatBoost Candidate

- OOF ROC-AUC: `0.818606`
- Mean Fold ROC-AUC: `0.840232`
- Fold Scores: `0.824934, 0.867107, 0.868925, 0.784255, 0.855938`

## Decision

- Improvement vs current best pipeline: `-0.023931` OOF ROC-AUC
- Native categorical handling did not improve validation performance.
- The label-encoded CatBoost pipeline remains the selected pipeline.

## Action Taken

- Left `competition_workbench.ipynb` unchanged.
- Left `submission.csv` unchanged.
- Left `experiments.csv` unchanged.
