# Model Comparison

- Timestamp: `2026-06-12T06:05:00+05:30`
- Feature set: `Workbench + School Count Encoding + Missing Indicators + BMI + SPEED_SCORE + EXPLOSIVENESS`
- Preprocessing: `Mean Imputation + Label Encoding + School Count Encoding + Missing Indicators + BMI + SPEED_SCORE + EXPLOSIVENESS`
- Fold strategy: `StratifiedKFold(n_splits=5, shuffle=True, random_state=42)`
- Model seed: `2025`

## Results

| Model | OOF ROC-AUC | Mean Fold ROC-AUC | Fold Scores |
| --- | ---: | ---: | --- |
| CatBoost | 0.831850 | 0.833920 | 0.814970, 0.865417, 0.841523, 0.804195, 0.843495 |
| RandomForest | 0.826997 | 0.828366 | 0.802504, 0.852958, 0.860871, 0.783617, 0.841879 |
| XGBoost | 0.822401 | 0.822954 | 0.806504, 0.850018, 0.829235, 0.800312, 0.828699 |
| LightGBM | 0.809142 | 0.809378 | 0.795452, 0.833639, 0.806293, 0.784510, 0.826998 |

## Decision

- Current default: `RandomForest` at `0.826997` OOF ROC-AUC.
- Best candidate: `CatBoost` at `0.831850` OOF ROC-AUC.
- Action: promoted `CatBoost` in `competition_workbench.ipynb` and regenerated `submission.csv`.
