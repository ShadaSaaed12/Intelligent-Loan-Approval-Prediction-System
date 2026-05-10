# Intelligent Loan Approval Prediction System

## Overview
This project aims to predict loan approval decisions using Machine Learning techniques based on applicants’ financial, personal, and credit-related information.

The project workflow includes:
- Data Cleaning
- Exploratory Data Analysis (EDA)
- Data Preprocessing
- Dimensionality Reduction
- Model Training
- Hyperparameter Tuning
- Model Evaluation

The final optimized Support Vector Machine (SVM) model achieved:

- ✅ Accuracy: **91.67%**
- ✅ ROC-AUC Score: **0.9679**

---

# Dataset Information

| Feature | Details |
|---|---|
| Dataset Size | 20,000 Records |
| Total Features | 35 Features |
| Target Variable | `LoanApproved` |

## Target Labels

| Label | Meaning |
|---|---|
| 1 | Approved |
| 0 | Rejected |

---

# Main Features

Some of the important features used in the project:

- Age
- AnnualIncome
- CreditScore
- EmploymentStatus
- EducationLevel
- LoanAmount
- DebtToIncomeRatio
- PaymentHistory
- BankruptcyHistory
- MonthlyIncome
- SavingsAccountBalance

---

# Data Cleaning

To prevent **Data Leakage**, the following columns were removed:

- `RiskScore`
- `InterestRate`
- `BaseInterestRate`
- `MonthlyLoanPayment`

## Additional Preprocessing Steps

- Missing Value Checking
- Outlier Detection using IQR
- Outlier Handling using Capping

---

# Exploratory Data Analysis (EDA)

EDA was performed to analyze:

- Loan approval distribution
- Credit score behavior
- Income distribution
- Employment status impact
- Bankruptcy history effect

## Key Insights

- Higher credit scores increased loan approval probability.
- Higher annual income was associated with approved loans.
- Bankruptcy history negatively affected loan approval decisions.

---

# Preprocessing

## Encoding

Categorical variables were encoded using:

- `OrdinalEncoder`

## Feature Scaling

Numerical features were standardized using:

- `StandardScaler`

## Pipeline Components

- `ColumnTransformer`
- `Pipeline`

---

# Dimensionality Reduction

Two feature selection techniques were compared:

| Technique | Accuracy |
|---|---|
| PCA | 90.45% |
| SelectKBest | 91.39% |

## Best Technique

✅ `SelectKBest`

---

# Machine Learning Model

## Model Used

- Support Vector Machine (SVM)

## Hyperparameter Tuning

Performed using:

- `GridSearchCV`
- `StratifiedKFold`

## Best Parameters

```python
{
    'svm__C': 1,
    'svm__gamma': 'scale',
    'svm__kernel': 'linear'
}

---

## Technologies Used

- Python  

- Pandas  

- NumPy  

- Matplotlib  

- Seaborn  

- Scikit-learn  

---

## Final Results

| Metric   | Score   |

|----------|---------|

| Accuracy | 91.67%  |

| ROC-AUC  | 0.9679  |

---

## Conclusion

The project successfully demonstrated the effectiveness of Machine Learning techniques in predicting loan approval decisions.

Feature selection using SelectKBest improved model performance, while the optimized SVM model achieved strong accuracy and an excellent ROC-AUC score.

---

## Future Improvements

- Apply ensemble models such as Random Forest and XGBoost  

- Handle class imbalance using SMOTE  

- Deploy the model using Flask or Streamlit  

- Add advanced feature engineering techniques to further improve model performance
