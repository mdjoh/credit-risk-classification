# Classifying Customer Credit Risk

## Scope
Build a logistic regression model to classify customer credit risk.

## Model Evaluation Metric
Macro F1 score is the evaluation metric used because it provides the best overall reflection of model performance. The Macro F1 metric considers both precision and recall metrics and does not mask the poor performance of a prediction class that has low support.

## Steps Taken
- Baseline evaluation
- Feature engineering (age calculation, determine whether customer is in the typical working age range, categorical feature encoding, standard scaling)
- Feature selection (remove features with high cardinality, SelectKBest, recursive feature elimination)
- Hyperparameter tuning (grid and random search) of the number of features to select, regularization type, regularization strength, and optimization algorithm used
- Performance evaluation on test data

Cross-validation was applied in all steps to obtain the mean Macro F1 score

## Results
Below is a table of mean Macro F1 score results after applying the specified step. Each step includes the techniques indicated in previous steps.

| Step      | Mean Macro F1 Score|
| ----------- | ----------- |
| 1. Baseline      | 0.4972       |
| 2. Feature engineering   | 0.7047        |
| 3. Feature selection   | 0.7084        |
| 4. Hyperparameter tuning   | 0.7821        |
| 5. Test data   | 0.7992*        |

*The test data Macro F1 score is a single value and not a mean value obtained from cross-validation.

The Macro F1 score improved with each subsequent method. 
