# Native Missing Value Handling Report

- Timestamp: `2026-06-12T14:46:47+0530`
- Step: `22`
- Source of truth: `competition_workbench.ipynb`
- Objective: determine whether CatBoost native missing value handling outperforms the current mean-imputation strategy

## Baseline

- OOF ROC-AUC: `0.842536`
- Mean Fold ROC-AUC: `0.842171`
- Fold Scores: `0.833413, 0.870857, 0.864294, 0.793878, 0.848413`

## Native Missing Candidate

- Preprocessing change: removed mean imputation from the current accepted feature pipeline
- Categorical handling: preserved label encoding for `Player_Type`, `Position_Type`, and `Position`
- OOF ROC-AUC: `0.833903`
- Mean Fold ROC-AUC: `0.840484`
- Fold Scores: `0.821937, 0.869522, 0.862519, 0.797066, 0.851375`

## Decision

- Native CatBoost missing value handling did not improve OOF ROC-AUC.
- Improvement vs baseline OOF ROC-AUC: `-0.008633`
- The current mean-imputation CatBoost pipeline remains the selected pipeline.

## Action Taken

- Left `competition_workbench.ipynb` unchanged.
- Left `submission.csv` unchanged.
- Left `experiments.csv` unchanged.
