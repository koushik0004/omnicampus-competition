TASK: Evaluate Native CatBoost Missing Value Handling

MODE: EXECUTION

IMPORTANT:

competition_workbench.ipynb is the single source of truth.

OBJECTIVE:

Determine whether CatBoost native missing value handling outperforms the current imputation strategy.

INPUT:

* competition_workbench.ipynb
* experiments.csv

REQUIREMENTS:

1. Start from current workbench.
2. Preserve all accepted features.
3. Preserve promoted CatBoost parameters.
4. Remove mean imputation from candidate pipeline.
5. Allow CatBoost to consume raw missing values directly.
6. Preserve folds and seed.
7. Compare candidate pipeline against current best pipeline.

IF IMPROVEMENT EXISTS:

* Update competition_workbench.ipynb
* Generate updated submission.csv
* Update experiments.csv

IF NO IMPROVEMENT:

* Leave notebook unchanged
* Leave submission unchanged
* Leave experiments.csv unchanged

OUTPUT:

* native_missing_value_report.md
* updated competition_workbench.ipynb (only if improved)

SUCCESS CRITERIA:

Native missing handling is promoted only when ROC-AUC improves.

STOP AFTER REPORT AND IMPLEMENTATION.
