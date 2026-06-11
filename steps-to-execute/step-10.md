TASK: Compare Candidate Models

MODE: EXECUTION

MODELS:
- Random Forest
- LightGBM
- CatBoost

INPUT:
Best feature set so far.

REQUIREMENTS:
Same folds.
Same seed.

OUTPUT:
model_comparison.md

Rank by:
- ROC-AUC
- Stability
- Training Time

Select Top 2.

STOP AFTER REPORT.