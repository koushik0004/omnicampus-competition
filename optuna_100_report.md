# Optuna 100 Trial Report

- Timestamp: `2026-06-12T13:23:12.453726+05:30`
- Step: `16`
- Source of truth: `competition_workbench.ipynb`
- Search budget: `100` Optuna trials
- Search space: `depth, learning_rate, iterations, l2_leaf_reg, min_data_in_leaf, random_strength, bagging_temperature, border_count`

## Baseline

- OOF ROC-AUC: `0.840338`
- Mean Fold ROC-AUC: `0.842664`

## Best Trial

- OOF ROC-AUC: `0.841108`
- Mean Fold ROC-AUC: `0.842760`
- Fold Scores: `0.821089, 0.872619, 0.864010, 0.801502, 0.854578`
- Best Iterations By Fold: `91, 140, 57, 120, 127`
- Parameters: `{'loss_function': 'Logloss', 'eval_metric': 'AUC', 'iterations': 319, 'learning_rate': 0.05636222508350733, 'depth': 6, 'l2_leaf_reg': 4.829465028684626, 'min_data_in_leaf': 11, 'random_strength': 1.0968021783282067, 'bagging_temperature': 1.4893907310245134, 'border_count': 197, 'random_seed': 2025, 'verbose': False, 'allow_writing_files': False}`

## Decision

- Improvement vs current best: `0.000770`
- Promoted the 100-trial Optuna CatBoost configuration in `competition_workbench.ipynb`.
- Regenerated `submission.csv` with the promoted fold-averaged test predictions.
- Appended a new experiment row to `experiments.csv`.
