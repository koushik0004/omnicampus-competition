# Tuning Report

- Timestamp: `2026-06-12T09:21:37.605625+05:30`
- Feature set: `Workbench + School Count Encoding + Missing Indicators + BMI + SPEED_SCORE + EXPLOSIVENESS`
- Preprocessing: `Mean Imputation + Label Encoding + School Count Encoding + Missing Indicators + BMI + SPEED_SCORE + EXPLOSIVENESS`
- Step: `11`
- Tuner: `Optuna`
- Trials: `30`

## Baseline CatBoost

- OOF ROC-AUC: `0.831762`
- Mean Fold ROC-AUC: `0.844619`
- Fold Scores: `0.824312, 0.873372, 0.866695, 0.805527, 0.853189`
- Best Iterations By Fold: `167, 301, 87, 490, 31`
- Parameters: `{'loss_function': 'Logloss', 'eval_metric': 'AUC', 'iterations': 1000, 'learning_rate': 0.03, 'depth': 6, 'l2_leaf_reg': 3.0, 'random_seed': 2025, 'verbose': False, 'allow_writing_files': False}`

## Best Optuna Trial

- Objective ROC-AUC: `0.840338`
- Parameters: `{'iterations': 400, 'learning_rate': 0.03654113675342291, 'depth': 4, 'l2_leaf_reg': 5.946538137175175, 'min_data_in_leaf': 11, 'random_strength': 1.0175536836933734, 'bagging_temperature': 2.0747131960172585, 'border_count': 137}`

## Re-evaluated Tuned CatBoost

- OOF ROC-AUC: `0.840338`
- Mean Fold ROC-AUC: `0.842664`
- Fold Scores: `0.818305, 0.865544, 0.874380, 0.801573, 0.853515`
- Best Iterations By Fold: `157, 247, 204, 293, 137`
- Delta vs baseline: `0.008575`

## Decision

- Promoted tuned CatBoost parameters in `competition_workbench.ipynb`.
- Selected model for submission: `Tuned CatBoost`
- Regenerated `submission.csv` with tuned fold-averaged predictions.
- Appended a new experiment row to `experiments.csv`.
