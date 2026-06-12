# Reproducibility Report

- Timestamp: `2026-06-12T09:56:34+0530`
- Notebook executed: `competition_workbench.ipynb`
- Execution mode: `Fresh kernel, start-to-finish`
- Step finalized: `13`

## Execution Verification

- Clean execution command completed successfully: `jupyter nbconvert --to notebook --execute competition_workbench.ipynb --inplace`
- Notebook execution reproduced the recorded step 12 outputs.
- Selected pipeline after rerun: `Tuned CatBoost`
- `experiments.csv` remained unchanged during the finalization pass.

## Metric Verification

- Recorded best experiment in `experiments.csv`: `EXP009`
- Recorded EXP009 CV ROC-AUC: `0.840338`
- Clean rerun tuned CatBoost OOF ROC-AUC: `0.840338`
- Match status: `Exact match`
- Ensemble rerun results: `Mean Average=0.836973`, `Rank Average=0.835746`
- Ensemble decision reproduced: `No ensemble improved on tuned CatBoost`

## Submission Verification

- Generated `final_submission.csv` from the validated notebook predictions.
- Submission columns: `Id`, `Drafted`
- Submission row count: `696`
- Probability range: `0.0101589753703815` to `0.9668958614511608`
- `submission.csv` and `final_submission.csv` SHA-256: `ca57476d5ebd3df0867585d35eb35e286bc35844cf95baf1f0007c7b4c63f0e0`

## Conclusion

- The final submission is reproducible from the current notebook state.
- The generated artifacts are ready for leaderboard upload.
