# Credit Risk Prediction Using Machine Learning

## Overview

This project presents an end-to-end Machine Learning framework for predicting loan default risk using historical borrower information. The objective is to assist financial institutions in identifying high-risk loan applicants before approving loans, thereby reducing financial losses and improving lending decisions.

The project includes data preprocessing, exploratory data analysis (EDA), feature engineering, hyperparameter optimization, threshold optimization, model comparison, and Explainable AI (SHAP).

---

## Features

- Exploratory Data Analysis (EDA)
- Duplicate and Missing Value Handling
- Outlier Detection and Capping using IQR
- Categorical Feature Encoding
- Feature Scaling using Min-Max Scaling
- Hyperparameter Optimization using Optuna
- Threshold Optimization
- ROC Curve and Precision-Recall Curve
- SHAP Explainability
- Feature Importance Analysis
- Comparison of Eight Machine Learning Models

---

## Dataset

**Dataset:** Credit Risk Dataset

The dataset contains borrower information including:

- Person Age
- Person Income
- Employment Length
- Home Ownership
- Loan Intent
- Loan Grade
- Loan Amount
- Loan Interest Rate
- Loan Percent Income
- Previous Default History
- Credit History Length

**Target Variable**

- `loan_status`
  - 0 → Non-Default
  - 1 → Default

---

## Project Workflow

```
Dataset
    │
    ▼
Exploratory Data Analysis
    │
    ▼
Data Cleaning
    │
    ▼
Missing Value Imputation
    │
    ▼
Outlier Detection & Capping
    │
    ▼
Categorical Encoding
    │
    ▼
Feature Scaling
    │
    ▼
Train-Test Split
    │
    ▼
Model Training
    │
    ▼
Hyperparameter Optimization
    │
    ▼
Threshold Optimization
    │
    ▼
Model Evaluation
    │
    ▼
SHAP Explainability
    │
    ▼
Model Comparison
```

---

## Data Preprocessing

The preprocessing pipeline includes:

- Duplicate record removal
- Median imputation for missing values
- Missing value indicators using SimpleImputer
- Outlier detection using IQR
- Outlier capping
- Binary encoding
- Ordinal encoding
- One-Hot encoding
- Min-Max feature scaling

---

## Machine Learning Models

Eight classification algorithms were implemented:

1. Logistic Regression
2. K-Nearest Neighbors (KNN)
3. Decision Tree
4. Random Forest
5. Voting Classifier
6. XGBoost
7. LightGBM
8. Balanced Random Forest

---

## Hyperparameter Optimization

Optuna was used to optimize model hyperparameters using 5-fold cross-validation.

Optimized parameters include:

- Learning Rate
- Tree Depth
- Number of Trees
- Number of Leaves
- Regularization
- Number of Neighbors
- Maximum Features
- Class Weights

---

## Threshold Optimization

Instead of using the default classification threshold of **0.50**, multiple probability thresholds were evaluated.

Metrics used:

- Precision
- Recall
- F1 Score

The threshold with the highest F1 Score was selected for each model.

---

## Model Evaluation Metrics

Models were evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC
- Precision-Recall AUC
- Confusion Matrix

---

## Explainable AI

Model predictions were interpreted using **SHAP (SHapley Additive Explanations)**.

Visualizations include:

- SHAP Beeswarm Plot
- SHAP Waterfall Plot
- SHAP Feature Importance Plot
- XGBoost Feature Importance
- LightGBM Feature Importance

---

## Best Performing Models

| Rank | Model |
|------|-------|
| 1 | XGBoost |
| 2 | LightGBM |
| 3 | Random Forest |
| 4 | Balanced Random Forest |
| 5 | Voting Classifier |
| 6 | KNN |
| 7 | Decision Tree |
| 8 | Logistic Regression |

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost
- LightGBM
- Optuna
- SHAP
- ydata-profiling
- Imbalanced-learn

---

## Project Structure

```
Credit-Risk-Prediction/
│
├── credit_risk_dataset.csv
├── Credit_Risk_Prediction.ipynb
├── README.md
├── Model_Comparison.csv
├── data_Report.html
│
├── Models/
│   ├── xgboost_credit_risk.pkl
│   ├── lightgbm.pkl
│   ├── random_forest.pkl
│   ├── balanced_random_forest.pkl
│   ├── decision_tree.pkl
│   ├── logistic_regression.pkl
│   ├── knn.pkl
│   └── voting_classifier.pkl
│
├── Figures/
│   ├── correlation_heatmap.png
│   ├── loan_grade.png
│   ├── loan_intent.png
│   ├── home_ownership.png
│   ├── roc_curve.png
│   ├── precision_recall_curve.png
│   ├── confusion_matrix.png
│   ├── shap_beeswarm.png
│   ├── shap_waterfall.png
│   ├── feature_importance.png
│   └── threshold_optimization.png
│
└── Project_Report.pdf
```

---

## Key Results

- End-to-end machine learning pipeline developed successfully.
- Eight classification models compared.
- Hyperparameter optimization improved predictive performance.
- Threshold optimization improved the balance between precision and recall.
- SHAP provided interpretable explanations for model predictions.
- XGBoost and LightGBM achieved the best overall performance.
- Ensemble learning methods consistently outperformed traditional machine learning algorithms.

---

## Future Improvements

- Deploy the model using Flask, FastAPI, or Streamlit.
- Integrate real-world banking datasets.
- Compare with CatBoost and TabNet.
- Build a web-based loan approval system.
- Incorporate credit bureau and transaction history data.

---

## References

1. Chen, T., & Guestrin, C. (2016). *XGBoost: A Scalable Tree Boosting System.*
2. Ke, G., et al. (2017). *LightGBM: A Highly Efficient Gradient Boosting Decision Tree.*
3. Lundberg, S. M., & Lee, S. I. (2017). *A Unified Approach to Interpreting Model Predictions.*
4. Pedregosa, F., et al. (2011). *Scikit-learn: Machine Learning in Python.*
5. Akiba, T., et al. (2019). *Optuna: A Next-generation Hyperparameter Optimization Framework.*

---

## Author

**Tejavath Venkatesh**

Department of Mathematics and Statistics  
Indian Institute of Technology Kanpur
