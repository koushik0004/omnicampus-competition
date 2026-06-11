TASK: Compare Candidate Models And Promote Winner

MODE: EXECUTION

IMPORTANT:

competition_workbench.ipynb is the single source of truth.

OBJECTIVE:

Identify the strongest model using the current best feature set and make it the new default model if it outperforms the current one.

INPUT:

* competition_workbench.ipynb
* experiments.csv

MODELS:

* RandomForest
* LightGBM
* CatBoost
* XGBoost

REQUIREMENTS:

1. Use existing accepted features.
2. Use identical folds and seed.
3. Compare models fairly.

IF A MODEL OUTPERFORMS CURRENT MODEL:

* Replace model in competition_workbench.ipynb
* Generate updated submission.csv
* Update experiments.csv

OUTPUT:

* model_comparison.md
* updated competition_workbench.ipynb

SUCCESS CRITERIA:
Workbench contains the best validated model.

STOP AFTER REPORT AND IMPLEMENTATION.
