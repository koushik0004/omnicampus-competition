# Position Percentile Features Evaluation

## Inputs Used

- `competition_workbench.ipynb`
- `experiments.csv`
- `steps-to-execute/step-15.md`

## Setup

- Baseline pipeline: current tuned CatBoost workbench from `EXP009`
- Validation: `StratifiedKFold(n_splits=5, shuffle=True, random_state=42)`
- Change tested: add position-relative percentile features for
  - `Sprint_40yd_Position_Percentile`
  - `Vertical_Jump_Position_Percentile`
  - `Broad_Jump_Position_Percentile`
  - `Bench_Position_Percentile`
- Leakage control: percentiles were fit from training data only and then applied to validation and test rows with the same fold-specific transform

## Results

- Baseline OOF ROC-AUC: `0.840338`
- Raw percentile variant OOF ROC-AUC: `0.827614`
- Sprint-inverted percentile variant OOF ROC-AUC: `0.828918`
- Best delta vs baseline: `-0.011420`

## Recommendation

**Reject**

The position percentile features did not improve the current best pipeline. `competition_workbench.ipynb`, `submission.csv`, and `experiments.csv` were left unchanged.
