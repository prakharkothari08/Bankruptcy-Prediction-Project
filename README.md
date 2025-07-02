
# Bankruptcy Prediction using Machine Learning

This project explores various machine learning models to predict corporate bankruptcy using financial indicators. It follows a complete machine learning workflow—covering data preprocessing, feature scaling, dimensionality reduction, and classification.

## 📊 Project Overview

The primary goal of this project is to predict bankruptcy status of companies using financial ratios and performance metrics. The focus was on comparing model performance with and without Principal Component Analysis (PCA) for dimensionality reduction.

## ⚙️ Workflow

1. **Data Preprocessing**
   - Removed rows with missing values
   - Dropped constant (non-informative) columns
   - Standardized numerical features

2. **Modeling (without PCA)**
   - Logistic Regression
   - Random Forest
   - Support Vector Machine (SVM)
   - K-Nearest Neighbors (KNN)

3. **Modeling (with PCA)**
   - PCA applied to reduce dimensionality
   - Re-trained all models on PCA-transformed data

4. **Evaluation Metrics**
   - Accuracy
   - Precision
   - Recall
   - F1-score

## 🧠 Results Summary

### Without PCA:
- **Logistic Regression** and **Random Forest** showed high accuracy but low recall for bankruptcy cases.
- **SVM** had perfect precision but extremely low recall.
- **KNN** performed similarly to Logistic Regression.

### With PCA:
- Models generally showed reduced recall.
- PCA simplified data but sometimes at the cost of minority class detection (bankrupt companies).

## 🔍 Key Features Influencing Bankruptcy

Top predictors identified from feature importances and coefficients:

- Net Income to Stockholder's Equity
- Persistent EPS in Last 4 Seasons
- Net Profit before Tax / Paid-in Capital
- Equity to Liability
- Net Income to Total Assets
- Interest Expense Ratio
- Degree of Financial Leverage (DFL)

These features highlight the importance of profitability, leverage, and cash flow management in predicting bankruptcy.

## ✅ Conclusion

The models achieved high overall accuracy but struggled with identifying the minority class. PCA helped with dimensionality reduction but often led to loss of critical recall performance. Future improvements could include:

- Handling class imbalance with oversampling or SMOTE
- Ensemble methods or boosting
- Cost-sensitive learning approaches

