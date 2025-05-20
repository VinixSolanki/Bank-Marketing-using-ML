# 📊 Bank Marketing Campaign Analysis using Machine Learning

This project focuses on analyzing and predicting whether a client will subscribe to a term deposit using classification models based on the **Bank Marketing** dataset from the UCI Machine Learning Repository.

---

## 📁 Dataset Source

📌 **UCI Repository:** [Bank Marketing Dataset](https://archive.ics.uci.edu/dataset/222/bank+marketing)  
This dataset contains information on direct marketing campaigns (phone calls) of a Portuguese banking institution.

---

## 🎯 Objective

To build a machine learning model that can accurately predict if a client will subscribe to a term deposit (`y = yes` or `no`) using historical campaign and client-related data.

---

## 📌 Dataset Features

- **Categorical:** job, marital, education, default, housing, loan, contact, month, day_of_week, poutcome
- **Numerical:** age, duration, campaign, pdays, previous, emp.var.rate, cons.price.idx, cons.conf.idx, euribor3m, nr.employed
- **Target Variable:** `y` (yes or no – whether the client subscribed)

---

## 🔧 Steps Performed

### 1. 📥 Data Loading & Understanding
- Loaded the dataset and examined its shape, types, and unique values.

### 2. 🧹 Data Cleaning
- Checked for null values and inconsistencies.
- Handled unknowns and outliers.

### 3. 📊 Exploratory Data Analysis (EDA)
#### A. Univariate Analysis
- Plotted distribution of features like `age`, `balance`, `job`, `education`, `housing`, etc.

#### B. Bivariate Analysis
- **Numerical vs Target:** Observed the influence of `duration`, `balance`, and `pdays` on the target variable.
- **Categorical vs Target:** Used bar plots to check how different categories affect subscription rates.

### 4. 📈 Feature Engineering
- Age and balance were segmented into bins.
- Created a new `season` column from the `month`.
- One-hot encoding was applied to categorical variables.

### 5. ⚙️ Model Building
Used the following classification models:
- Logistic Regression
- Decision Tree
- Random Forest
- **XGBoost** (Best performer)

### 6. 🧪 Model Evaluation
Evaluated using:
- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC Score
- Cross-Validation

---

## 🏆 Best Model: XGBoost Classifier

| Metric        | Score |
|---------------|-------|
| Accuracy      | 0.93  |
| Precision     | 0.94  |
| Recall        | 0.93  |
| F1-Score      | 0.93  |
| ROC-AUC Score | 0.93  |

✅ Performed best in terms of all metrics.
✅ Handled class imbalance and overfitting well.

---

## 📌 Final Observations

- Clients with higher balances and older age tend to subscribe more.
- Longer call duration is strongly associated with higher subscription.
- Fewer campaign calls and recent past contacts improve conversion.
- XGBoost was the most reliable and high-performing model in this case.

---

## 💻 Tools & Libraries

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- XGBoost

---


