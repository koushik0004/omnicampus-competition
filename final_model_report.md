# Final Model Report

- Timestamp: `2026-06-12T09:56:34+0530`
- Notebook: `competition_workbench.ipynb`
- Final selected pipeline: `Tuned CatBoost`
- Source experiment: `EXP009`
- Competition step finalized: `13`

## Selected Model

- Model family: `CatBoostClassifier`
- Validation status: `Best validated pipeline retained after ensemble check`
- OOF ROC-AUC: `0.840338`
- Recorded public score: `0.84745`
- Feature set: `Workbench + School Count Encoding + Missing Indicators + BMI + SPEED_SCORE + EXPLOSIVENESS`
- Preprocessing: `Mean Imputation + Label Encoding + School Count Encoding + Missing Indicators + BMI + SPEED_SCORE + EXPLOSIVENESS`

## Frozen Parameters

- `iterations=400`
- `learning_rate=0.03654113675342291`
- `depth=4`
- `l2_leaf_reg=5.946538137175175`
- `min_data_in_leaf=11`
- `random_strength=1.0175536836933734`
- `bagging_temperature=2.0747131960172585`
- `border_count=137`
- Fixed training args: `loss_function=Logloss`, `eval_metric=AUC`, `random_seed=2025`, `verbose=False`, `allow_writing_files=False`

## Final Decision

- Step 12 clean rerun confirmed `Tuned CatBoost` remained stronger than both validated ensemble methods.
- `Mean Average` OOF ROC-AUC: `0.836973`
- `Rank Average` OOF ROC-AUC: `0.835746`
- Delta vs tuned CatBoost: `-0.003365`
- Final predictions were generated from the retained tuned CatBoost default pipeline.

## Final Artifact

- Final upload file: `final_submission.csv`
- Submission schema: `Id,Drafted`
