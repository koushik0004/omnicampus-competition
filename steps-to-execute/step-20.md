TASK: Evaluate Recursive Feature Elimination

MODE: EXECUTION

IMPORTANT:

competition_workbench.ipynb is the single source of truth.

OBJECTIVE:

Determine whether removing weak features improves ROC-AUC.

INPUT:

* competition_workbench.ipynb
* experiments.csv

REQUIREMENTS:

1. Start from current workbench.
2. Preserve model and preprocessing.
3. Perform recursive feature elimination using the promoted CatBoost model.
4. Evaluate multiple reduced feature sets.
5. Use identical folds and seed.
6. Compare the best reduced feature set against the current best pipeline.

IF IMPROVEMENT EXISTS:

* Update competition_workbench.ipynb
* Generate updated submission.csv
* Update experiments.csv

IF NO IMPROVEMENT:

* Leave notebook unchanged
* Leave submission unchanged
* Leave experiments.csv unchanged

OUTPUT:

* rfe_feature_selection_report.md
* updated competition_workbench.ipynb (only if improved)

SUCCESS CRITERIA:

Reduced feature set is promoted only when validation improves.

STOP AFTER REPORT AND IMPLEMENTATION.
