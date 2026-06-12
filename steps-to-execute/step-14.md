TASK: Evaluate And Apply School Target Encoding

MODE: EXECUTION

IMPORTANT:

competition_workbench.ipynb is the single source of truth.

OBJECTIVE:

Determine whether School target encoding outperforms the current School count encoding setup.

INPUT:

* competition_workbench.ipynb
* experiments.csv

FEATURE:

School_Target_Encoded

REQUIREMENTS:

1. Start from current workbench.
2. Preserve all accepted improvements.
3. Implement strict OOF target encoding.
4. Compare against current best pipeline.
5. Use identical folds and seed.

IF IMPROVEMENT EXISTS:

* Update competition_workbench.ipynb
* Generate submission.csv
* Update experiments.csv

IF NO IMPROVEMENT:

* Leave notebook unchanged
* Leave submission unchanged
* Leave experiment log unchanged

OUTPUT:

* school_target_encoding_report.md
* updated competition_workbench.ipynb (only if improved)

STOP AFTER REPORT AND IMPLEMENTATION.
