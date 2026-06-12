TASK: Evaluate SHAP-Based Feature Pruning

MODE: EXECUTION

IMPORTANT:

competition_workbench.ipynb is the single source of truth.

OBJECTIVE:

Determine whether removing low-importance SHAP features improves ROC-AUC.

INPUT:

* competition_workbench.ipynb
* experiments.csv

REQUIREMENTS:

1. Start from current workbench.
2. Train the current promoted CatBoost pipeline.
3. Compute SHAP feature importance.
4. Evaluate:

   * Remove bottom 10% features
   * Remove bottom 20% features
   * Remove bottom 30% features
5. Preserve folds and seed.
6. Compare each candidate against current best pipeline.
7. Select only the best-performing candidate.

IF IMPROVEMENT EXISTS:

* Update competition_workbench.ipynb
* Generate updated submission.csv
* Update experiments.csv

IF NO IMPROVEMENT:

* Leave notebook unchanged
* Leave submission unchanged
* Leave experiments.csv unchanged

OUTPUT:

* shap_feature_pruning_report.md
* updated competition_workbench.ipynb (only if improved)

SUCCESS CRITERIA:

SHAP-pruned feature set exists only if ROC-AUC improves.

STOP AFTER REPORT AND IMPLEMENTATION.
