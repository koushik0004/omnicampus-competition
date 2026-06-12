TASK: Deep Tune Current CatBoost Using Optuna 100 Trials

MODE: EXECUTION

IMPORTANT:

competition_workbench.ipynb is the single source of truth.

Never restart from baseline.ipynb.

OBJECTIVE:

Determine whether a larger Optuna search improves ROC-AUC over the current promoted CatBoost configuration.

INPUT:

* competition_workbench.ipynb
* experiments.csv

TOOL:

* Optuna

REQUIREMENTS:

1. Start from current competition_workbench.ipynb.
2. Preserve all accepted features.
3. Preserve preprocessing.
4. Preserve CV folds and seed.
5. Run 100 Optuna trials.
6. Search:

   * depth
   * learning_rate
   * iterations
   * l2_leaf_reg
   * min_data_in_leaf
   * random_strength
   * bagging_temperature
   * border_count
7. Compare against current best pipeline.

IF IMPROVEMENT EXISTS:

* Update competition_workbench.ipynb
* Generate updated submission.csv
* Update experiments.csv

IF NO IMPROVEMENT:

* Leave competition_workbench.ipynb unchanged
* Leave submission.csv unchanged
* Leave experiments.csv unchanged

OUTPUT:

* optuna_100_report.md
* updated competition_workbench.ipynb (only if improved)

STOP AFTER REPORT AND IMPLEMENTATION.
