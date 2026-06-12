# Weighted Blend Report

- Timestamp: `2026-06-12T14:57:52.298716+05:30`
- Feature set: `Workbench + School Count Encoding + Missing Indicators + BMI + SPEED_SCORE + EXPLOSIVENESS`
- Preprocessing: `Mean Imputation + Label Encoding + School Count Encoding + Missing Indicators + BMI + SPEED_SCORE + EXPLOSIVENESS`
- Step: `23`
- Methods: `Weighted probability blend`
- Top validated models: `Tuned CatBoost, RandomForest, XGBoost`

## Validated Models

### Tuned CatBoost

- OOF ROC-AUC: `0.842536`
- Mean Fold ROC-AUC: `0.842171`
- Fold Scores: `0.833413, 0.870857, 0.864294, 0.793878, 0.848413`

### RandomForest

- OOF ROC-AUC: `0.826997`
- Mean Fold ROC-AUC: `0.828366`
- Fold Scores: `0.802504, 0.852958, 0.860871, 0.783617, 0.841879`

### XGBoost

- OOF ROC-AUC: `0.822401`
- Mean Fold ROC-AUC: `0.822954`
- Fold Scores: `0.806504, 0.850018, 0.829235, 0.800312, 0.828699`

## Weighted Blend Results

### Weighted Blend: Tuned CatBoost=95%, XGBoost=5%

- Weights: `Tuned CatBoost=95%, XGBoost=5%`
- OOF ROC-AUC: `0.842704`

### Weighted Blend: Tuned CatBoost=90%, XGBoost=10%

- Weights: `Tuned CatBoost=90%, XGBoost=10%`
- OOF ROC-AUC: `0.842594`

### Weighted Blend: Tuned CatBoost=100%

- Weights: `Tuned CatBoost=100%`
- OOF ROC-AUC: `0.842536`

### Weighted Blend: Tuned CatBoost=90%, RandomForest=5%, XGBoost=5%

- Weights: `Tuned CatBoost=90%, RandomForest=5%, XGBoost=5%`
- OOF ROC-AUC: `0.842493`

### Weighted Blend: Tuned CatBoost=85%, RandomForest=5%, XGBoost=10%

- Weights: `Tuned CatBoost=85%, RandomForest=5%, XGBoost=10%`
- OOF ROC-AUC: `0.842405`

### Weighted Blend: Tuned CatBoost=95%, RandomForest=5%

- Weights: `Tuned CatBoost=95%, RandomForest=5%`
- OOF ROC-AUC: `0.842308`

### Weighted Blend: Tuned CatBoost=85%, RandomForest=10%, XGBoost=5%

- Weights: `Tuned CatBoost=85%, RandomForest=10%, XGBoost=5%`
- OOF ROC-AUC: `0.842278`

### Weighted Blend: Tuned CatBoost=85%, XGBoost=15%

- Weights: `Tuned CatBoost=85%, XGBoost=15%`
- OOF ROC-AUC: `0.842231`

### Weighted Blend: Tuned CatBoost=80%, RandomForest=10%, XGBoost=10%

- Weights: `Tuned CatBoost=80%, RandomForest=10%, XGBoost=10%`
- OOF ROC-AUC: `0.842152`

### Weighted Blend: Tuned CatBoost=80%, RandomForest=15%, XGBoost=5%

- Weights: `Tuned CatBoost=80%, RandomForest=15%, XGBoost=5%`
- OOF ROC-AUC: `0.842055`

## Decision

- Best single model: `Tuned CatBoost` at `0.842536` OOF ROC-AUC.
- Best weighted blend: `Weighted Blend: CatBoost 95% + XGBoost 5%` at `0.842704` OOF ROC-AUC.
- Improvement vs best single model: `0.000167`.
- Promoted `Weighted Blend: CatBoost 95% + XGBoost 5%` as the default pipeline in `competition_workbench.ipynb`.
- Regenerated `submission.csv` with blended predictions.
- Appended a new experiment row to `experiments.csv`.
