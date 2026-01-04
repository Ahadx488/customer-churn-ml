# Customer Churn Analysis - EDA and Modeling

## Overview

This project focuses on Exploratory Data Analysis (EDA) and modeling to uncover insights from the data and build predictive models to understand Customer Churn.

Customer churn, also known as customer attrition, refers to the phenomenon where customers stop doing business with a company or service. It is a critical metric for businesses as it directly impacts revenue and profitability. 
High churn rates can indicate dissatisfaction with the product or service, poor customer experience.

Understanding the factors driving churn enables organizations to take proactive steps toward customer retention.

The goal of this project is to:

● Explore customer behavior through EDA

● Identify key churn-driving features

● Build and evaluate multiple classification models to predict churn

## Dataset

This project uses the Credit Card Customer Churn Prediction dataset from Kaggle: [Data Source](https://www.kaggle.com/datasets/rjmanoj/credit-card-customer-churn-prediction/data).

It contains the following features: 

 1. RowNumber
 2. CustomerId
 3. Surname
 4. CreditScore
 5. Geography
 6. Gender
 7. Age
 8. Tenure
 9. Balance
 10. NumOfProducts
 11. HasCrCard
 12. IsActiveMember
 13. EstimatedSalary
 14. Exited

🎯 Target Variable:

Exited → Indicates whether a customer has churned (1) or not (0)

## Requirements

The following libraries are required to run the notebook:

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- imbalanced-learn
- xgboost

## Key Features

1. Handling Imbalanced Data: The project implements techniques to help handle imbalanced data such as SMOTE, ensuring accurate predictions even when the dependent variable is underrepresented.
2. Exploratory Data Analysis (EDA): The project features a stage of Exploratory Data Analysis (EDA), where we examine the data closely to identify trends and understand the reasons behind customer churn.
3. Modeling & Classification: The project employs a variety of models, including Logistic Regression, Random Forest, K-Nearest Neighbors, Support Vector Machine, XGBoost, and Gradient Boosting, to predict customer churn, with techniques such as class weighting and SMOTE used to handle class imbalance.

## 📊 Model Performance Evaluation

Customer churn prediction is an imbalanced classification problem, therefore relying on accuracy alone is misleading.  
To properly evaluate model performance, multiple metrics were used:

- Accuracy  
- Recall  
- F1 Score  
- ROC–AUC  

Models were trained using class balancing techniques (SMOTE / class weights where applicable).

---

### Model Comparison Results

| Model                  | Accuracy | Recall | F1 Score | ROC AUC |
|------------------------|----------|--------|----------|---------|
| Gradient Boosting      | 0.817000   | 0.700342 | 0.598391   | 0.859767  |
| Random Forest          | 0.862000   | 0.414384 | 0.538976   | 0.852447  |
| XGBoost                | 0.833000   | 0.609589 | 0.586974   | 0.841784  |
| Support Vector Machine | 0.785667   | 0.662671 | 0.546224   | 0.822503  |
| K-Nearest Neighbors    | 0.752333   | 0.667808 | 0.512147   | 0.776639  |
| Logistic Regression    | 0.703667   | 0.683219 | 0.473029   | 0.764082  |

---

###Key Insights

- Gradient Boosting achieved the best overall performance with the highest F1 Score and ROC–AUC.
- XGBoost performed competitively and is a strong alternative.
- Random Forest showed high accuracy but low recall, making it less effective at detecting churned customers.
- Logistic Regression served as a baseline model and underperformed compared to ensemble methods.

---

### ✅ Final Conclusion

Gradient Boosting is the most suitable model for this dataset as it provides the best balance between precision and recall while handling class imbalance effectively.




