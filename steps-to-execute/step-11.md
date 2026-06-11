TASK: Tune Current Best Model And Promote Improvements

MODE: EXECUTION

IMPORTANT:

competition_workbench.ipynb is the single source of truth.

OBJECTIVE:

Optimize the currently selected model and apply tuned parameters only if validation improves.

INPUT:

* competition_workbench.ipynb
* experiments.csv

TOOL:
Optuna

REQUIREMENTS:

1. Tune only the current best model.
2. Keep feature set unchanged.
3. Keep preprocessing unchanged.
4. Keep CV split unchanged.

IF TUNED MODEL IMPROVES ROC-AUC:

* Update competition_workbench.ipynb
* Generate updated submission.csv
* Update experiments.csv

IF NO IMPROVEMENT:

* Retain current configuration

OUTPUT:

* tuning_report.md
* updated competition_workbench.ipynb

STOP AFTER REPORT AND IMPLEMENTATION.
