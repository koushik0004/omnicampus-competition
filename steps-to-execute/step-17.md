TASK: Deep Tune Current CatBoost Using Optuna 300 Trials

MODE: EXECUTION

IMPORTANT:

Run only after Step 16 completes.

competition_workbench.ipynb is the single source of truth.

OBJECTIVE:

Determine whether an extended hyperparameter search improves ROC-AUC.

INPUT:

* competition_workbench.ipynb
* experiments.csv

TOOL:

* Optuna

REQUIREMENTS:

1. Start from current workbench.
2. Use the currently promoted CatBoost.
3. Preserve feature engineering.
4. Preserve CV folds.
5. Run 300 Optuna trials.
6. Use pruning.
7. Compare against current best pipeline.

IF IMPROVEMENT EXISTS:

* Update competition_workbench.ipynb
* Generate submission.csv
* Update experiments.csv

IF NO IMPROVEMENT:

* Leave notebook unchanged
* Leave submission unchanged
* Leave experiments unchanged

OUTPUT:

* optuna_300_report.md
* updated competition_workbench.ipynb (only if improved)

STOP AFTER REPORT AND IMPLEMENTATION.
