# BMI Feature Evaluation Report

## Inputs Used

- `competition_workbench.ipynb`
- `experiments.csv`

## Step-by-Step Execution

1. Read `competition-goals-and-plan.md` to confirm the intent: keep experiments reproducible and only promote CV-backed improvements.
2. Read `steps-to-execute/step-6.md` and used the current `competition_workbench.ipynb` as the starting pipeline.
3. Preserved all accepted improvements already present in the workbench:
   - `School_count`
   - missing-value indicator columns for the seven null-bearing numeric features
4. Added `BMI = Weight / Height^2` on top of the current best pipeline.
5. Kept the same model and validation setup:
   - `RandomForestClassifier(n_estimators=100, max_depth=5, random_state=2025)`
   - `StratifiedKFold(n_splits=5, shuffle=True, random_state=42)`
6. Compared the current best pipeline against the BMI-enhanced pipeline under identical folds and seed.
7. Because ROC-AUC improved, updated `competition_workbench.ipynb`, regenerated `submission.csv`, and appended the accepted experiment to `experiments.csv`.

## Results

- Current best ROC-AUC before BMI: `0.817604`
- ROC-AUC with BMI: `0.817691`
- Delta: `+0.000087`
- Feature count after preprocessing: `22`

## Fold-Level AUC

- Current best pipeline: `0.788018`, `0.840031`, `0.839165`, `0.780074`, `0.840731`
- BMI pipeline: `0.786746`, `0.839832`, `0.836451`, `0.784481`, `0.840944`

## Recommendation

- `Keep`

BMI produced a small but positive ROC-AUC improvement under the same CV folds and seed, so it was promoted into `competition_workbench.ipynb`.
