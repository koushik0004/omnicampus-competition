TASK: Evaluate And Apply BMI Feature

MODE: EXECUTION

IMPORTANT:

competition_workbench.ipynb is the single source of truth.

Never restart from baseline.ipynb.

All experiments must begin from the current state of competition_workbench.ipynb.

Accepted improvements must be merged into competition_workbench.ipynb.

OBJECTIVE:

Evaluate whether BMI improves ROC-AUC and permanently apply it only if it improves the current best pipeline.

INPUT:

* competition_workbench.ipynb
* experiments.csv

FEATURE:
BMI = Weight / Height^2

REQUIREMENTS:

1. Start from current competition_workbench.ipynb.
2. Add BMI feature.
3. Keep all existing accepted improvements.
4. Use identical CV folds and seed.
5. Compare against current best pipeline.

IF IMPROVEMENT EXISTS:

* Update competition_workbench.ipynb
* Generate updated submission.csv
* Append experiment result to experiments.csv

IF NO IMPROVEMENT:

* Leave competition_workbench.ipynb unchanged

OUTPUT:

* bmi_feature_report.md
* updated competition_workbench.ipynb (only if improved)

SUCCESS CRITERIA:
Workbench contains BMI only when ROC-AUC improves.

STOP AFTER REPORT AND IMPLEMENTATION.
