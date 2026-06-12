TASK: Evaluate And Apply Position Target Encoding

MODE: EXECUTION

IMPORTANT:

competition_workbench.ipynb is the single source of truth.

Never restart from baseline.ipynb.

OBJECTIVE:

Evaluate whether out-of-fold target encoding of Position improves ROC-AUC.

INPUT:

* competition_workbench.ipynb
* experiments.csv

FEATURE:

Position_Target_Encoded

REQUIREMENTS:

1. Start from current competition_workbench.ipynb.
2. Preserve every accepted feature and model currently present.
3. Implement STRICT out-of-fold target encoding.
4. Prevent target leakage.
5. Use identical CV folds and seed.
6. Compare against the current best pipeline.

IF IMPROVEMENT EXISTS:

* Update competition_workbench.ipynb
* Generate updated submission.csv
* Update experiments.csv

IF NO IMPROVEMENT:

* Leave competition_workbench.ipynb unchanged
* Leave submission.csv unchanged
* Leave experiments.csv unchanged

OUTPUT:

* position_target_encoding_report.md
* updated competition_workbench.ipynb (only if improved)

SUCCESS CRITERIA:

Position target encoding exists only if ROC-AUC improves.

STOP AFTER REPORT AND IMPLEMENTATION.
