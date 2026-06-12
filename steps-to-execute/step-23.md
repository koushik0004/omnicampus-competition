TASK: Evaluate Weighted Probability Blending

MODE: EXECUTION

IMPORTANT:

competition_workbench.ipynb is the single source of truth.

OBJECTIVE:

Determine whether weighted blending improves ROC-AUC versus the current best single model.

INPUT:

* competition_workbench.ipynb
* experiments.csv

MODELS:

* Current promoted CatBoost
* Best RandomForest
* Best XGBoost

WEIGHTS TO TEST:

* 95 / 5
* 90 / 10
* 85 / 15
* 80 / 20
* 75 / 25
* 70 / 30

REQUIREMENTS:

1. Generate OOF predictions.
2. Evaluate every weight combination.
3. Preserve folds and seed.
4. Compare against current best pipeline.
5. Select only the highest-performing blend.

IF IMPROVEMENT EXISTS:

* Promote blend as default pipeline
* Update competition_workbench.ipynb
* Generate submission.csv
* Update experiments.csv

IF NO IMPROVEMENT:

* Leave notebook unchanged
* Leave submission unchanged
* Leave experiments.csv unchanged

OUTPUT:

* weighted_blend_report.md
* updated competition_workbench.ipynb (only if improved)

SUCCESS CRITERIA:

Blend is promoted only when ROC-AUC improves.

STOP AFTER REPORT AND IMPLEMENTATION.
