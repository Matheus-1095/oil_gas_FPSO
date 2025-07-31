# 🔍 Predictive Maintenance for FPSO Equipment – Shape Digital Data Science Test

This repository contains my solution to the technical challenge proposed for FPSO Oil&Gas solution. The objective was to analyze sensor data from an FPSO (Floating Production, Storage and Offloading) vessel and develop a predictive model to anticipate equipment failures.

---

## 🎯 Objective

To identify the most relevant features that anticipate equipment failures in FPSO operations, and build a robust machine learning model capable of predicting these failures **before they occur**, minimizing financial loss and operational risk.

---

## ⚙️ Tools and Libraries

- Python (Pandas, NumPy, Scikit-learn, DecisionTree, XGBoostm RandomForest, LogisticRegression)
- Matplotlib & Seaborn (Visualizations)
- SHAP (Model explainability)
- Imbalanced-learn (SMOTE for class balancing)

---

## 📊 Key Steps

### 1. Exploratory Data Analysis
- Normality and variance tests (Shapiro, Levene)
- Mann-Whitney U test to assess variable significance
- Spearman correlation to understand feature relationships

### 2. Feature Engineering
- Created `Vibration_RMS` and `Temp_Pressure` composite features
- Converted categorical presets into integer features

### 3. Feature Selection
- Used **Boruta** and **Feature Importance** to select the most predictive features
- Final features: `Vibration_RMS`, `Frequency`, `Temp_Pressure`

### 4. Modeling and Evaluation
- Tested four models: Decision Tree, Random Forest, XGBoost and Logistic Regression
- Applied **SMOTE** to address class imbalance
- Evaluated with cross-validation and test set metrics (Precision, Recall, F1, ROC AUC)

### 5. Explainability
- Used **SHAP values** to interpret the impact of each feature
- Identified that high vibration and high temp-pressure are strong predictors of failure

---

## ✅ Final Model: Logistic Regression

- **Recall**: 1.00 (no real failure goes undetected)
- **F1 Score**: 0.61
- **ROC AUC**: 0.97

Despite lower precision, the model's perfect recall ensures **zero false negatives**, which is critical in safety-sensitive contexts like Oil & Gas.

---

## 💰 Business Value

Predicting all failures in advance can prevent **millions of dollars in losses** per year due to unplanned downtime, repairs and environmental risks. A detailed business impact analysis is included in the notebook.

---

## 🙏 Acknowledgements

Thanks to the Shape Digital team for the opportunity to participate in this technical challenge. It was an enriching exercise that combined data science, domain understanding, and real-world impact.

---

## 📫 Contact

Feel free to connect or reach out:

**Matheus Guerreiro Bulhões**  
[LinkedIn](https://www.linkedin.com/in/matheusguerreirobulhoes/)  
matheus_uefacl@hotmail.com

