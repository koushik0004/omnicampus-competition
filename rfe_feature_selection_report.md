# Recursive Feature Elimination Report

- Timestamp: `2026-06-12T14:27:28+0530`
- Step: `20`
- Source of truth: `competition_workbench.ipynb`
- Objective: determine whether removing weak features improves ROC-AUC

## Baseline

- OOF ROC-AUC: `0.842536`
- Mean Fold ROC-AUC: `0.842171`

## RFE Path

Recursive elimination was run from the current promoted CatBoost pipeline using the same folds and seed. At each step, the weakest feature from the current subset was removed and the reduced set was re-evaluated.

| Step | Removed Feature | Feature Count | OOF ROC-AUC | Mean Fold ROC-AUC |
| --- | --- | ---: | ---: | ---: |
| 1 | `Broad_Jump_missing` | 23 | 0.834765 | 0.839566 |
| 2 | `Sprint_40yd_missing` | 22 | 0.812811 | 0.841329 |
| 3 | `Vertical_Jump_missing` | 21 | 0.840589 | 0.843452 |
| 4 | `Agility_3cone_missing` | 20 | 0.837575 | 0.843111 |
| 5 | `Shuttle_missing` | 19 | 0.817723 | 0.841868 |
| 6 | `Bench_Press_Reps_missing` | 18 | 0.838818 | 0.841191 |
| 7 | `Player_Type` | 17 | 0.834095 | 0.840493 |
| 8 | `Position_Type` | 16 | 0.827983 | 0.839447 |
| 9 | `Vertical_Jump` | 15 | 0.817847 | 0.837773 |
| 10 | `Broad_Jump` | 14 | 0.820887 | 0.837922 |

## Best Reduced Set

- Feature count: `21`
- Removed feature: `Vertical_Jump_missing`
- OOF ROC-AUC: `0.840589`
- Mean Fold ROC-AUC: `0.843452`
- Improvement vs baseline OOF ROC-AUC: `-0.001947`

Selected features:

- `Year`
- `Age`
- `Height`
- `Weight`
- `Sprint_40yd`
- `Vertical_Jump`
- `Bench_Press_Reps`
- `Broad_Jump`
- `Agility_3cone`
- `Shuttle`
- `Player_Type`
- `Position_Type`
- `Position`
- `School_count`
- `Age_missing`
- `Bench_Press_Reps_missing`
- `Agility_3cone_missing`
- `Shuttle_missing`
- `BMI`
- `SPEED_SCORE`
- `EXPLOSIVENESS`

## Decision

- No reduced feature set improved the current best pipeline on OOF ROC-AUC.
- The best reduced set improved mean fold ROC-AUC slightly, but not the validation metric used for promotion.
- The current workbench remains the selected pipeline.

## Action Taken

- Left `competition_workbench.ipynb` unchanged.
- Left `submission.csv` unchanged.
- Left `experiments.csv` unchanged.
