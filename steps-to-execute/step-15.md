TASK: Evaluate And Apply Position Percentile Features

MODE: EXECUTION

IMPORTANT:

competition_workbench.ipynb is the single source of truth.

OBJECTIVE:

Determine whether position-relative percentile features improve ROC-AUC.

INPUT:

* competition_workbench.ipynb
* experiments.csv

FEATURES:

* Sprint_40yd_Position_Percentile
* Vertical_Jump_Position_Percentile
* Broad_Jump_Position_Percentile
* Bench_Position_Percentile

REQUIREMENTS:

1. Start from current workbench.
2. Preserve accepted improvements.
3. Compute percentiles using training data only.
4. Apply same transformation to test data.
5. Compare against current best pipeline.

IF IMPROVEMENT EXISTS:

* Update competition_workbench.ipynb
* Generate submission.csv
* Update experiments.csv

IF NO IMPROVEMENT:

* No notebook changes
* No submission changes
* No experiment updates

OUTPUT:

* position_percentile_report.md
* updated competition_workbench.ipynb (only if improved)

STOP AFTER REPORT AND IMPLEMENTATION.
