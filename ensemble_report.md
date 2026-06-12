# Ensemble Report

- Timestamp: `2026-06-12T13:42:18.573714+05:30`
- Feature set: `Workbench + School Count Encoding + Missing Indicators + BMI + SPEED_SCORE + EXPLOSIVENESS`
- Preprocessing: `Mean Imputation + Label Encoding + School Count Encoding + Missing Indicators + BMI + SPEED_SCORE + EXPLOSIVENESS`
- Step: `12`
- Methods: `Mean Average, Rank Average`
- Top validated models: `RandomForest, Tuned CatBoost`

## Validated Models

### RandomForest

- OOF ROC-AUC: `0.826997`
- Mean Fold ROC-AUC: `0.828366`
- Fold Scores: `0.802504, 0.852958, 0.860871, 0.783617, 0.841879`

### Tuned CatBoost

- OOF ROC-AUC: `0.842536`
- Mean Fold ROC-AUC: `0.842171`
- Fold Scores: `0.833413, 0.870857, 0.864294, 0.793878, 0.848413`

## Ensemble Results

### Mean Average

- OOF ROC-AUC: `0.838485`

### Rank Average

- OOF ROC-AUC: `0.837222`

## Decision

- Best single model: `Tuned CatBoost` at `0.842536` OOF ROC-AUC.
- Best ensemble: `Mean Average` at `0.838485` OOF ROC-AUC.
- Delta vs best single model: `-0.004051`.
- No ensemble improved on tuned CatBoost validation performance.
- Retained tuned CatBoost as the default pipeline in `competition_workbench.ipynb`.
- Left `experiments.csv` unchanged.
