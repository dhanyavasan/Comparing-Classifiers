# Term Deposit Campaign Analysis & Model Comparison

## Overview
This project analyzes a marketing campaign dataset by exploring features, applying feature engineering, and building baseline and advanced classification models. It involves fine-tuning, evaluating key metrics, and ultimately comparing classifiers to identify the most suitable model for the business objective.

Link to Jupyter Notebook: 

## Insights from Data Exploration & Visualizations
1. The campaign primarily targeted customers working as administrators, blue-collar workers, and technicians, while students, self-employed individuals, and the unemployed formed the least represented segments.
2. The outcome of the previous campaign strongly impacts customer decisions—those with a successful prior outcome are significantly more likely to accept the term deposit, whereas a failed previous campaign greatly reduces the chances of acceptance.
3. Campaign activity follows a clear seasonal pattern, peaking between May and August, while remaining minimal from September to April. The near absence of activity in January and February suggests a likely pause in campaign efforts during those months.

## Observations on Data Imbalance 
The dataset is significantly imbalanced, with approximately 4,500 positive instances out of 41,188 records, indicating a strong skew toward customers who did not subscribe to the term deposit.

## Model Performance Comparison
Multiple classification algorithms like **Logistic Regression, KNN, Decision Tree, SVM** were applied and evaluated based on training/test accuracy and training time. After performing hyperparameter tuning, the best-performing configurations for each model were selected. The final models were then assessed using key evaluation metrics, as summarized in the table below.

### Metrics of Base Models:
<img width="408" alt="Screenshot 2025-04-12 at 1 08 57 PM" src="https://github.com/user-attachments/assets/5de1c4a3-0462-484c-ab4c-1de47e7f3827" />



### Metrics of Hyperparameter Tuned Models:
<img width="406" alt="Screenshot 2025-04-12 at 1 09 32 PM" src="https://github.com/user-attachments/assets/ff8ad75c-39ba-43e3-8e95-55990982f4ea" />


Among the evaluated classifiers (Logistic Regression, KNN, Decision Tree, SVM), all models improved after hyperparameter tuning.

## Evaluation Metric Selection & Justification
Due to the high class imbalance, the Accuracy metric is not a reliable indicator of model performance. In this campaign context, where both false positives and false negatives carry business costs, it's essential to balance Precision and Recall. The **F1 Score** is the most suitable metric, as it **effectively captures this trade-off in imbalanced classification tasks**.

## Model Selection & Conclusion
After comparing the F1 Scores across all classification models, the **Decision Tree Classifier** demonstrated the highest performance, achieving an **F1 Score of 0.9139**. Based on this result and the business objective, it is concluded that the **Decision Tree is the most suitable model for this campaign scenario**.

## Next Steps and Recommendations
- Deploy the Decision Tree model for campaign targeting.
- Explore additional features to improve performance.
- Monitor and retrain the model as new data becomes available.





    
