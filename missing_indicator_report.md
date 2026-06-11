# Missing Indicator Evaluation Report

## Inputs Used

- `competition_workbench.ipynb`
- `experiments.csv`

## Step-by-Step Execution

1. Read `competition-goals-and-plan.md` to confirm the intent: keep experiments reproducible and promote only CV-backed improvements.
2. Read `steps-to-execute/step-5.md` and used the current `competition_workbench.ipynb` as the starting pipeline.
3. Evaluated the current best pipeline with `School_count` against the same pipeline plus binary missing-value indicators for:
   - `Age`
   - `Sprint_40yd`
   - `Vertical_Jump`
   - `Bench_Press_Reps`
   - `Broad_Jump`
   - `Agility_3cone`
   - `Shuttle`
4. Preserved the existing mean imputation, label encoding, `RandomForestClassifier`, and `StratifiedKFold(n_splits=5, shuffle=True, random_state=42)`.
5. Because ROC-AUC improved, updated `competition_workbench.ipynb`, regenerated `submission.csv`, and appended the experiment log.

## Results

- Baseline ROC-AUC: `0.815328`
- Missing-indicator ROC-AUC: `0.817604`
- Delta: `+0.002276`
- Feature count after preprocessing: `21`

## Recommendation

- `Keep`

The missing-value indicators improved ROC-AUC under the same CV folds and seed, so the change was promoted into `competition_workbench.ipynb`.
