TASK: Evaluate School Count Encoding

MODE: EXECUTION

OBJECTIVE:
Determine whether School count encoding improves ROC-AUC.

BASELINE:
Current best pipeline.

CHANGE ALLOWED:
School count encoding only.

PROHIBITED:
- New features
- New models
- Hyperparameter tuning

OUTPUT:
school_encoding_report.md

Report:
- Baseline AUC
- New AUC
- Delta
- Keep/Reject recommendation

STOP AFTER REPORT.