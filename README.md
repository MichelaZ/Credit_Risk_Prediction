# Credit Risk Analysis
The purpose of this project is to determine the best supervised model to use to predict which loans are the highest risk.

## Results

| Test | Accuracy | High Risk Precision | Low Risk Precision | High Risk Recall | Low Risk Recall | High Risk F1 | Low Risk F1 |
|---|----|---|---|---|---|---|---|
| Naive Random Oversampling | 0.65 |  0.01 | 1.00 |  0.61 | 0.69 |  0.02 | 0.82 |
| SMOTE Oversampling | 0.65 | 0.01 | 1.00 | 0.61 | 0.69 | 0.02 | 0.82 |
| Cluster Centroid Undersampling | 0.51 |  0.01 | 1.00 | 0.59 | 0.43 | 0.01 | 0.60 |
| SMOTEEN | 0.63 | 0.01 | 1.00 | 0.72 | .53 | 0.02 | 0.69 |
| Balanced Random Forest Classifier | 0.79 | .04 | 1.00 | 0.67| .91 | 0.07 | 0.95 |
| Easy Ensemble Classifier| 0.92 | 0.07 | 1.00 | 0.90 | 0.94 | .14 | 0.97 |

- **Oversampling methods:** Naive Random Oversampling & SMOTE Oversampling didn’t do the worst, but I would not recommend them.
- **Undersampling & combination methods:** Cluster Centroid Undersampling & SMOTEEN preformed the worst probably due to dropped data. They had the worst accuracy, precision, and recall for high-risk loans.
- **Ensamble Learners:** Balanced Random Forest Classifier & Easy Ensemble Classifier preformed the best.

### Recommendations
I recommend the Easy ensemble model, because it had the highest accuracy, precision (high-risk) and recall(high-risk) scores. High risk score recall was the most important score in my evaluation of the model, because it is more important to determine which loans are might be high risk than which loans are actually high risk. This means that there will be people who are labeled high risk, but would most likely pay back the loan on time. Consider if this is a good trade off. 
