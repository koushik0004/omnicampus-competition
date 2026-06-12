# EXPLOSIVENESS Feature Report

## Inputs

- Source notebook: `competition_workbench.ipynb`
- Experiment log: `experiments.csv`
- Baseline for this step: `EXP006`

## Feature Definition

`EXPLOSIVENESS` was implemented using the repo tutorial definition:

`0.5 * (zscore(Vertical_Jump) + zscore(Broad_Jump))`

The z-score statistics were computed from the training set and then applied to both train and test.

## Validation Setup

- Model: `RandomForestClassifier(n_estimators=100, max_depth=5, random_state=2025)`
- Cross-validation: `StratifiedKFold(n_splits=5, shuffle=True, random_state=42)`
- Decision rule: keep the feature only if mean ROC-AUC improves over the current best pipeline

## Results

- Current best before `EXPLOSIVENESS`: `0.827997`
- With `EXPLOSIVENESS`: `0.828366`
- Delta: `+0.000369`
- Feature count after acceptance: `24`

### Fold AUCs

- Before: `0.806151`, `0.850614`, `0.860913`, `0.782171`, `0.840136`
- After: `0.802504`, `0.852958`, `0.860871`, `0.783617`, `0.841879`

## Decision

Keep `EXPLOSIVENESS`.

The gain is small, but it is positive under the unchanged folds, seed, and model configuration required by the instructions.
