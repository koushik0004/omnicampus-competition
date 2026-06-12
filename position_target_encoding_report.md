# Position Target Encoding Evaluation

## Inputs Used

- `competition_workbench.ipynb`
- `experiments.csv`
- `steps-to-execute/step-13.md`

## Setup

- Baseline pipeline: current `competition_workbench.ipynb` workbench
- Model: `CatBoostClassifier` with the frozen tuned parameters from `EXP009`
- Validation: `StratifiedKFold(n_splits=5, shuffle=True, random_state=42)`
- Change tested: strict out-of-fold `Position_Target_Encoded` added on top of the current accepted feature set
- Leakage control: inner OOF encoding for training rows, outer-fold training-only encoding for validation and test rows

## Results

- Baseline OOF ROC-AUC: `0.840338`
- Position target encoding OOF ROC-AUC: `0.838629`
- Delta: `-0.001709`

## Recommendation

**Reject**

`Position_Target_Encoded` did not improve the current best pipeline, so `competition_workbench.ipynb`, `submission.csv`, and `experiments.csv` were left unchanged.
