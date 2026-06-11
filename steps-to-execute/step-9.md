TASK: Evaluate And Apply AGILITY_RATIO Feature

MODE: EXECUTION

IMPORTANT:

competition_workbench.ipynb is the single source of truth.

Never restart from baseline.ipynb.

OBJECTIVE:

Evaluate AGILITY_RATIO and apply it only if it improves ROC-AUC.

INPUT:

* competition_workbench.ipynb
* experiments.csv

FEATURE:
AGILITY_RATIO = Agility_3cone / Shuttle

REQUIREMENTS:

1. Start from current competition_workbench.ipynb.
2. Add AGILITY_RATIO.
3. Preserve accepted improvements.
4. Compare against current best pipeline.

IF IMPROVEMENT EXISTS:

* Update competition_workbench.ipynb
* Generate submission.csv
* Update experiments.csv

IF NO IMPROVEMENT:

* Leave notebook unchanged

OUTPUT:

* agility_ratio_report.md
* updated competition_workbench.ipynb (only if improved)

STOP AFTER REPORT AND IMPLEMENTATION.
