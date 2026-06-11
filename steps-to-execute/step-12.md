TASK: Evaluate And Promote Ensemble

MODE: EXECUTION

IMPORTANT:

competition_workbench.ipynb is the single source of truth.

OBJECTIVE:

Determine whether an ensemble outperforms the best individual model.

INPUT:

* competition_workbench.ipynb
* experiments.csv

METHODS:

* Mean Average
* Rank Average

REQUIREMENTS:

1. Use top validated models only.
2. Generate OOF predictions.
3. Compare ensemble against best single model.

IF ENSEMBLE IMPROVES ROC-AUC:

* Make ensemble the default pipeline
* Update competition_workbench.ipynb
* Generate submission.csv
* Update experiments.csv

IF NOT:

* Keep current best model

OUTPUT:

* ensemble_report.md
* updated competition_workbench.ipynb

STOP AFTER REPORT AND IMPLEMENTATION.
