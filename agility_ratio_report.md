# AGILITY_RATIO Evaluation Report

## Step Executed

Evaluated `AGILITY_RATIO = Agility_3cone / Shuttle` against the current best pipeline in `competition_workbench.ipynb` without changing any existing accepted improvements.

## Comparison Setup

- Source of truth: `competition_workbench.ipynb`
- Baseline pipeline: `School_count` + missing indicators + `BMI` + `SPEED_SCORE` + `EXPLOSIVENESS`
- Candidate pipeline: baseline pipeline + `AGILITY_RATIO`
- Model: `RandomForestClassifier(n_estimators=100, max_depth=5, random_state=2025)`
- CV: `StratifiedKFold(n_splits=5, shuffle=True, random_state=42)`

## Results

### Current best pipeline

- Feature count: `24`
- Fold AUCs: `0.802504`, `0.852958`, `0.860871`, `0.783617`, `0.841879`
- Mean CV ROC-AUC: `0.828366`

### Pipeline with AGILITY_RATIO

- Feature count: `25`
- Fold AUCs: `0.799324`, `0.848839`, `0.858768`, `0.781427`, `0.841440`
- Mean CV ROC-AUC: `0.825960`

### Delta

- `AGILITY_RATIO - current best = -0.002406`

## Decision

`AGILITY_RATIO` does not improve ROC-AUC.

Per `steps-to-execute/step-9.md`, the notebook was left unchanged and no new submission was generated.

## Files Changed

- Created `agility_ratio_report.md`

## Files Intentionally Unchanged

- `competition_workbench.ipynb`
- `experiments.csv`
- `submission.csv`
