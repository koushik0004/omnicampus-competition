TASK: Evaluate And Apply Missing Indicators

OBJECTIVE:
Evaluate missing-value indicator features and permanently apply them to competition_workbench.ipynb if they improve ROC-AUC.

INPUT:
- competition_workbench.ipynb
- experiments.csv

REQUIREMENTS:
1. Use competition_workbench.ipynb as the starting point.
2. Add binary indicators for all columns with missing values.
3. Run identical CV folds and seed.
4. Compare against current best pipeline.
5. If ROC-AUC improves:
   - Update competition_workbench.ipynb
   - Generate submission.csv
   - Update experiments.csv
6. If ROC-AUC degrades:
   - Do not modify competition_workbench.ipynb

OUTPUT:
- missing_indicator_report.md
- updated competition_workbench.ipynb (only if improvement)

STOP AFTER REPORT AND IMPLEMENTATION.