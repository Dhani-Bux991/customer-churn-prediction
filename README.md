# Customer Churn Prediction 📉

Predicts which telecom customers are likely to leave, so a retention team can act early. The project covers exploratory analysis, a preprocessing pipeline, and a comparison of models and class-imbalance techniques.

## Problem
Losing customers costs telecom companies revenue. Only a minority of customers churn, so a model that simply predicts "no churn" looks accurate while missing the customers who matter. This project focuses on catching those customers.


## Approach
1. Cleaned the data and encoded categorical features
2. Built a preprocessing pipeline
3. Trained Logistic Regression and Decision Tree models
4. Tested SMOTE and class weighting to handle the class imbalance
5. Evaluated with precision, recall and F1-score on the churn class

## Results

| Approach | Accuracy | Precision | Recall | F1 |
|---|---|---|---|---|
| Baseline (imbalanced) | 0.804 | 0.655 | 0.553 | 0.600 |
| SMOTE | 0.759 | 0.540 | 0.634 | 0.583 |
| Class Weighting | 0.738 | 0.504 | 0.789 | 0.615 |

Precision, recall and F1 are for the churn class.

## Key Insights
- Class weighting caught 79% of churners, up from 55% for the baseline model.
- Accuracy fell because the model flags more customers as likely to leave. For churn, recall and F1 matter more than accuracy.
- The strongest predictors were tenure and fiber optic internet service, followed by total charges.
- Trade-off: precision dropped to 0.50, so about half of flagged customers will not actually leave.
