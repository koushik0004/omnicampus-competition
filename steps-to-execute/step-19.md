TASK: Evaluate Native CatBoost Categorical Processing

MODE: EXECUTION

IMPORTANT:

competition_workbench.ipynb is the single source of truth.

Never restart from baseline.ipynb.

OBJECTIVE:

Determine whether CatBoost native categorical handling improves ROC-AUC versus the current Label Encoding approach.

INPUT:

* competition_workbench.ipynb
* experiments.csv

REQUIREMENTS:

1. Start from current competition_workbench.ipynb.
2. Preserve all accepted features.
3. Preserve current Optuna-promoted CatBoost parameters.
4. Identify all categorical columns currently label encoded.
5. Create a candidate pipeline using CatBoost native categorical support.
6. Preserve identical folds and random seed.
7. Compare candidate pipeline against current best pipeline.

IF IMPROVEMENT EXISTS:

* Update competition_workbench.ipynb
* Generate updated submission.csv
* Update experiments.csv

IF NO IMPROVEMENT:

* Leave competition_workbench.ipynb unchanged
* Leave submission.csv unchanged
* Leave experiments.csv unchanged

OUTPUT:

* native_catboost_categorical_report.md
* updated competition_workbench.ipynb (only if improved)

SUCCESS CRITERIA:

Workbench contains CatBoost native categorical handling only if ROC-AUC improves.

STOP AFTER REPORT AND IMPLEMENTATION.
