# Optuna 300 Trial Report

- Timestamp: `2026-06-12T13:37:03.263973+05:30`
- Step: `17`
- Source of truth: `competition_workbench.ipynb`
- Search budget: `300` Optuna trials
- Pruner: `MedianPruner(n_startup_trials=25, n_warmup_steps=1, interval_steps=1)`
- Search space: `depth, learning_rate, iterations, l2_leaf_reg, min_data_in_leaf, random_strength, bagging_temperature, border_count`

## Baseline

- Current best CatBoost OOF ROC-AUC: `0.841108`
- Current best CatBoost Mean Fold ROC-AUC: `0.842760`

## Best Trial

- OOF ROC-AUC: `0.842536`
- Mean Fold ROC-AUC: `0.842171`
- Fold Scores: `0.833413, 0.870857, 0.864294, 0.793878, 0.848413`
- Best Iterations By Fold: `152, 160, 102, 69, 127`
- Parameters: `{"allow_writing_files": false, "bagging_temperature": 4.401083568255273, "border_count": 207, "depth": 6, "eval_metric": "AUC", "iterations": 410, "l2_leaf_reg": 2.7208272685560084, "learning_rate": 0.04030377888196673, "loss_function": "Logloss", "min_data_in_leaf": 9, "random_seed": 2025, "random_strength": 1.014761081951387, "verbose": false}`

## Search Stats

- Completed trials: `74`
- Pruned trials: `226`

## Decision

- Improvement vs current best CatBoost: `0.001429`
- Promoted the 300-trial Optuna CatBoost configuration in `competition_workbench.ipynb`.
- Re-evaluated the full workbench; CatBoost remained the selected pipeline.
- Regenerated `submission.csv` with the promoted fold-averaged test predictions.
- Appended a new experiment row to `experiments.csv`.
