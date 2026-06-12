TASK: Evaluate CatBoost Stability Across Alternative Random Seeds

MODE: EXECUTION

IMPORTANT:

competition_workbench.ipynb is the single source of truth.

OBJECTIVE:

Determine whether the promoted CatBoost configuration is robust or overfit to the current seed.

INPUT:

* competition_workbench.ipynb
* experiments.csv

REQUIREMENTS:

1. Preserve current pipeline.
2. Evaluate seeds:

   * 2025
   * 42
   * 777
   * 999
   * 1234
3. Preserve folds.
4. Compare mean OOF ROC-AUC.
5. Promote only if a new seed consistently improves validation.

IF IMPROVEMENT EXISTS:

* Update competition_workbench.ipynb
* Generate submission.csv
* Update experiments.csv

IF NO IMPROVEMENT:

* Leave all artifacts unchanged

OUTPUT:

* seed_stability_report.md
* updated competition_workbench.ipynb (only if improved)

STOP AFTER REPORT AND IMPLEMENTATION.
