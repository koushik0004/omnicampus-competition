TASK: Evaluate And Apply SPEED_SCORE Feature

MODE: EXECUTION

IMPORTANT:

competition_workbench.ipynb is the single source of truth.

Never restart from baseline.ipynb.

OBJECTIVE:

Evaluate SPEED_SCORE and apply it only if it improves the current best pipeline.

INPUT:

* competition_workbench.ipynb
* experiments.csv

FEATURE:
SPEED_SCORE = (Weight * 200) / Sprint_40yd^4

REQUIREMENTS:

1. Start from current competition_workbench.ipynb.
2. Add SPEED_SCORE.
3. Preserve all previously accepted improvements.
4. Use identical CV folds and seed.
5. Compare against current best pipeline.

IF IMPROVEMENT EXISTS:

* Update competition_workbench.ipynb
* Generate updated submission.csv
* Update experiments.csv

IF NO IMPROVEMENT:

* Leave notebook unchanged

OUTPUT:

* speed_score_report.md
* updated competition_workbench.ipynb (only if improved)

STOP AFTER REPORT AND IMPLEMENTATION.
