# Task 2: EdTech Student Intervention Risk Prediction

## Base Public File
- `StudentPerformanceFactors.csv` (Kaggle Student Performance Factors dataset)

## Private Files
1. `task2_edtech_private_lms_train.csv`
2. `task2_edtech_private_lms_scoring.csv`

## Merge Instructions
1. Load `StudentPerformanceFactors.csv`.
2. Create merge key from original row order:
   - `base["student_row_id"] = base.index`
3. Merge base file with `task2_edtech_private_lms_train.csv` on `student_row_id` for training.
4. Merge base file with `task2_edtech_private_lms_scoring.csv` on `student_row_id` for final scoring.

## Objective
Predict `needs_intervention_30d`.

### Target Meaning
- `0`: learner is not likely to require intervention in the next 30 days.
- `1`: learner is likely to require intervention in the next 30 days.

## Rules
- Use only one final supervised learning algorithm.
- Do not use `student_row_id` as a model feature.
- Treat `support_ticket_text` as a text feature in some way.
- Do preprocessing, feature engineering, train-validation split, model training, evaluation, and final prediction.

## Required Output
1. Notebook or Python script.
2. Short explanation of preprocessing and algorithm choice.
3. Validation metrics.
4. `predictions.csv` with exactly these columns:
   - `student_row_id`
   - `needs_intervention_probability`
   - `needs_intervention_pred`
