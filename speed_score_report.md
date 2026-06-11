# SPEED_SCORE Feature Evaluation Report

## Inputs Used

- `competition_workbench.ipynb`
- `experiments.csv`

## Step-by-Step Execution

1. Read `steps-to-execute/step-7.md` and used the current `competition_workbench.ipynb` as the starting pipeline.
2. Preserved all accepted improvements already present in the workbench:
   - `School_count`
   - missing-value indicator columns for the seven null-bearing numeric features
   - `BMI`
3. Added `SPEED_SCORE = (Weight * 200) / Sprint_40yd^4` on top of the current best pipeline.
4. Kept the same model and validation setup:
   - `RandomForestClassifier(n_estimators=100, max_depth=5, random_state=2025)`
   - `StratifiedKFold(n_splits=5, shuffle=True, random_state=42)`
5. Compared the current best pipeline against the SPEED_SCORE-enhanced pipeline under identical folds and seed.
6. Because ROC-AUC improved, updated `competition_workbench.ipynb`, regenerated `submission.csv`, and appended the accepted experiment to `experiments.csv`.

## Results

- Current best ROC-AUC before SPEED_SCORE: `0.817691`
- ROC-AUC with SPEED_SCORE: `0.827997`
- Delta: `+0.010306`
- Feature count after preprocessing: `23`

## Fold-Level AUC

- Current best pipeline: `0.786746`, `0.839832`, `0.836451`, `0.784481`, `0.840944`
- SPEED_SCORE pipeline: `0.806151`, `0.850614`, `0.860913`, `0.782171`, `0.840136`

## Recommendation

- `Keep`

SPEED_SCORE produced a clear ROC-AUC improvement under the same CV folds and seed, so it was promoted into `competition_workbench.ipynb`.
