# SHAP Feature Pruning Report

- Timestamp: `2026-06-12T14:32:05.666019+05:30`
- Step: `21`
- Source of truth: `competition_workbench.ipynb`
- Objective: determine whether removing low-importance SHAP features improves ROC-AUC

## Baseline

- OOF ROC-AUC: `0.842536`
- Mean Fold ROC-AUC: `0.842171`

## SHAP Importance Ranking

- `Broad_Jump_missing`: `0.007716`
- `Sprint_40yd_missing`: `0.008258`
- `Agility_3cone_missing`: `0.010196`
- `Vertical_Jump_missing`: `0.013216`
- `Shuttle_missing`: `0.014699`
- `Bench_Press_Reps_missing`: `0.026893`
- `Position_Type`: `0.055355`
- `Vertical_Jump`: `0.065096`
- `Broad_Jump`: `0.067946`
- `BMI`: `0.070535`
- `Year`: `0.089604`
- `EXPLOSIVENESS`: `0.089653`
- `Player_Type`: `0.094697`
- `Shuttle`: `0.095573`
- `Agility_3cone`: `0.097329`
- `Position`: `0.108860`
- `Height`: `0.126733`
- `School_count`: `0.150075`
- `Sprint_40yd`: `0.154893`
- `Bench_Press_Reps`: `0.162358`
- `Weight`: `0.194741`
- `Age`: `0.253375`
- `SPEED_SCORE`: `0.531159`
- `Age_missing`: `1.174356`

## Candidate Results

### Remove bottom 10%

- Features removed: `2`
- Removed features: `Broad_Jump_missing`, `Sprint_40yd_missing`
- Feature count: `22`
- OOF ROC-AUC: `0.812811`
- Mean Fold ROC-AUC: `0.841329`

### Remove bottom 20%

- Features removed: `5`
- Removed features: `Broad_Jump_missing`, `Sprint_40yd_missing`, `Agility_3cone_missing`, `Vertical_Jump_missing`, `Shuttle_missing`
- Feature count: `19`
- OOF ROC-AUC: `0.817723`
- Mean Fold ROC-AUC: `0.841868`

### Remove bottom 30%

- Features removed: `7`
- Removed features: `Broad_Jump_missing`, `Sprint_40yd_missing`, `Agility_3cone_missing`, `Vertical_Jump_missing`, `Shuttle_missing`, `Bench_Press_Reps_missing`, `Position_Type`
- Feature count: `17`
- OOF ROC-AUC: `0.838599`
- Mean Fold ROC-AUC: `0.841583`

## Best Candidate

- Best reduced set: remove bottom `30%` SHAP features.
- OOF ROC-AUC: `0.838599`
- Mean Fold ROC-AUC: `0.841583`
- Improvement vs baseline OOF ROC-AUC: `-0.003937`

## Decision

- No SHAP-pruned feature set improved the current best pipeline on OOF ROC-AUC.
- The current workbench remains the selected pipeline.
- Left `competition_workbench.ipynb`, `submission.csv`, and `experiments.csv` unchanged.
