# Experiment Template

Use one record per experiment. Keep the baseline notebook unchanged and log only the delta.

## Experiment Metadata

- `experiment_id`:
- `timestamp`:
- `feature_set`:
- `preprocessing`:
- `model`:
- `cv_auc`:
- `public_score`:
- `notes`:

## Recommended Logging Format

- `experiment_id`: short stable label, e.g. `exp_001`
- `timestamp`: ISO 8601 timestamp with timezone
- `feature_set`: exact columns or engineered features used
- `preprocessing`: encoding, scaling, imputation, filtering, etc.
- `model`: model name and key hyperparameters
- `cv_auc`: cross-validation AUC
- `public_score`: leaderboard score from the submission
- `notes`: what changed, why it was tried, and any important observations

## Example

- `experiment_id`: `exp_001`
- `timestamp`: `2026-06-11T00:00:00+05:30`
- `feature_set`: `baseline features from baseline.ipynb`
- `preprocessing`: `label encoding for categorical columns`
- `model`: `RandomForestClassifier`
- `cv_auc`: `0.0000`
- `public_score`: `0.0000`
- `notes`: `baseline reference entry; replace values after running a real experiment`
