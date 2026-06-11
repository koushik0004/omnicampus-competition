# Competition Notes

Competition: `NFL Draft Prediction`

Reference notebooks:
- `baseline.ipynb`
- `README.ipynb`

## Goal

Predict whether a player is drafted using the provided tabular features.

## Evaluation

- Metric: `AUC`
- Submission target: predicted probabilities for the test set

## Experiment Tracking Rules

- Do not modify the baseline pipeline when logging experiments.
- Record every experiment in `experiments.csv`.
- Use one unique `experiment_id` per run.
- Write timestamps in ISO 8601 format with timezone.
- Keep `feature_set`, `preprocessing`, and `model` descriptions specific enough to reproduce the run later.
- Put the exact leaderboard score in `public_score` after submission.
- Use `notes` for concise observations, tradeoffs, or failure cases.

## Suggested Workflow

1. Copy the template from `experiment-template.md`.
2. Fill in the new run details before or immediately after executing it.
3. Append the same information to `experiments.csv`.
4. Keep the notes file updated with useful competition-wide observations.
