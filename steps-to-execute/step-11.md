TASK: Tune Top Models

MODE: EXECUTION

INPUT:
Top 2 models from model_comparison.md

TOOL:
Optuna

REQUIREMENTS:
Fixed feature set.
Fixed CV.

OUTPUT:
tuning_report.md

Include:
- best parameters
- score improvement
- overfitting observations

STOP AFTER REPORT.