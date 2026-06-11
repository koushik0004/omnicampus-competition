# School Count Encoding Evaluation

## Setup

- Baseline pipeline: current notebook pipeline from `baseline.ipynb`
- Model: `RandomForestClassifier(n_estimators=100, max_depth=5, random_state=2025)`
- Validation: `StratifiedKFold(n_splits=5, shuffle=True, random_state=42)`
- Only change tested: replace dropping `School` with a single `School_count` feature derived from training-set frequency counts

## Results

- Baseline AUC: `0.811480`
- New AUC: `0.815328`
- Delta: `+0.003848`

## Recommendation

**Keep**

`School` count encoding improved mean ROC-AUC by about `0.0038` with no model, feature-set, or hyperparameter changes outside the allowed scope.
