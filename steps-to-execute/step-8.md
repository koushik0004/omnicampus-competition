TASK: Evaluate And Apply EXPLOSIVENESS Feature

MODE: EXECUTION

IMPORTANT:

competition_workbench.ipynb is the single source of truth.

Never restart from baseline.ipynb.

OBJECTIVE:

Evaluate EXPLOSIVENESS and apply it only if it improves ROC-AUC.

INPUT:

* competition_workbench.ipynb
* experiments.csv

FEATURE:

EXPLOSIVENESS = standardized combination of:

* Vertical_Jump
* Broad_Jump

REQUIREMENTS:

1. Start from current competition_workbench.ipynb.
2. Add EXPLOSIVENESS.
3. Preserve all accepted improvements.
4. Use identical folds and seed.
5. Compare against current best pipeline.

IF IMPROVEMENT EXISTS:

* Update competition_workbench.ipynb
* Generate submission.csv
* Update experiments.csv

IF NO IMPROVEMENT:

* Keep notebook unchanged

OUTPUT:

* explosiveness_report.md
* updated competition_workbench.ipynb (only if improved)

STOP AFTER REPORT AND IMPLEMENTATION.
