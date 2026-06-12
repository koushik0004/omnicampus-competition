# School Target Encoding Evaluation

## Inputs Used

- `competition_workbench.ipynb`
- `experiments.csv`
- `steps-to-execute/step-14.md`

## Setup

- Baseline pipeline: current `competition_workbench.ipynb` workbench
- Model: `CatBoostClassifier` with the frozen tuned parameters from `EXP009`
- Validation: `StratifiedKFold(n_splits=5, shuffle=True, random_state=42)`
- Change tested: strict out-of-fold `School_Target_Encoded` added on top of the current accepted feature set
- Leakage control: inner OOF encoding for training rows, outer-fold training-only encoding for validation and test rows

## Results

- Baseline OOF ROC-AUC: `0.840338`
- School target encoding OOF ROC-AUC: `0.835964`
- Delta: `-0.004374`

## Recommendation

**Reject**

`School_Target_Encoded` did not improve the current best pipeline, so `competition_workbench.ipynb`, `submission.csv`, and `experiments.csv` were left unchanged.
