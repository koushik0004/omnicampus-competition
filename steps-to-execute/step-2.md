TASK: Create Experiment Tracking Framework

MODE: EXECUTION

OBJECTIVE:
Create a reproducible experiment tracking system for all future competition work.

FILES TO REVIEW:
- baseline.ipynb
- README.ipynb

REQUIREMENTS:

Create:

1. experiments.csv

Columns:
- experiment_id
- timestamp
- feature_set
- preprocessing
- model
- cv_auc
- public_score
- notes

2. experiment-template.md

3. competition-notes.md

RULES:

- Do not train any new model.
- Do not modify baseline pipeline.
- Only create experiment management artifacts.

SUCCESS CRITERIA:

Future experiments can be recorded consistently.

STOP AFTER FILES ARE GENERATED.