# 📊 Customer Churn Prediction using Machine Learning

---

## 🚀 Project Overview

Customer churn prediction is one of the most important business problems in industries like telecom, banking, and subscription-based services.

In this project, we build a **Machine Learning classification model** that predicts whether a customer is likely to **churn (leave the service)** based on their account information, service usage, and billing details.

By identifying potential churners in advance, businesses can take proactive actions such as offering discounts, improving service, or personalized engagement strategies.

---

## 🎯 Objective

The primary objective of this project is:

* To predict whether a customer will churn (**Yes / No**)
* To analyze customer behavior patterns
* To build a model that helps reduce customer attrition

---

## 🧠 Machine Learning Type

* **Supervised Learning**
* **Classification Problem**

---

## 📁 Dataset Description

The dataset contains customer information such as:

* Demographics (gender, senior citizen, dependents)
* Account details (tenure, contract type)
* Services used (internet, streaming, security)
* Billing information (monthly charges, total charges)
* Target variable (**Churn**)

---

## 🔧 Data Preprocessing & Cleaning

The following steps were performed to prepare the data:

* Removed unnecessary columns (`customerID`)
* Converted `TotalCharges` to numeric (handled invalid values)
* Handled missing values using row removal
* Encoded categorical variables using **One-Hot Encoding**
* Converted target variable (`Churn`) into binary (0/1)

---

## ⚙️ Feature Engineering

* Dropped redundant columns (`customerID`)
* Applied **One-Hot Encoding** using `pd.get_dummies()`
* Ensured dataset is fully numeric and ML-ready

---

## 📊 Model Building

We trained and evaluated multiple models:

### 🔹 Logistic Regression

* Simple and interpretable model
* Good baseline performance

### 🔹 Decision Tree Classifier

* Captures non-linear relationships
* Tends to overfit without tuning

### 🔹 Random Forest Classifier (Tuned) ✅

* Ensemble method combining multiple decision trees
* Handles complex patterns effectively
* Reduced overfitting using hyperparameter tuning

---

## 🔥 Final Model — Tuned Random Forest

### Parameters Used:

* `n_estimators = 200`
* `max_depth = 10`
* `class_weight = 'balanced'`
* `random_state = 42`

---

## 📈 Model Evaluation

### Metrics Used:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix

---

### 📊 Final Performance

| Metric            | Value |
| ----------------- | ----- |
| Accuracy          | ~76%  |
| Precision (Churn) | ~53%  |
| Recall (Churn)    | ~70%  |
| F1 Score          | ~60%  |

---

## 🧠 Key Insights

* Dataset is **imbalanced**, with more non-churn customers
* Accuracy alone is misleading in classification problems
* **Recall is the most important metric** for churn prediction
* Tuned Random Forest provides the best balance between precision and recall

---

## 🏆 Business Impact

This model can help companies:

* Identify customers likely to churn
* Take preventive actions (offers, engagement)
* Improve customer retention
* Reduce revenue loss

---

## 💾 Model Saving

The trained model and feature columns were saved using `pickle`:

* `churn_model.pickle`
* `churn_columns.pickle`

---

## 🔮 Prediction Function

A custom prediction function was created to:

* Accept user input
* Convert it into model-compatible format
* Predict churn outcome

---

## 🛠️ Technologies Used

* Python 🐍
* Pandas
* NumPy
* Scikit-learn
* Jupyter Notebook

---

## 📂 Project Structure

```
customer-churn-prediction/
│
├── data/
│   └── churn.csv
│
├── notebooks/
│   └── churn_prediction.ipynb
│
├── models/
│   ├── churn_model.pickle
│   └── churn_columns.pickle
│
├── README.md
├── .gitignore
```

---

## 📌 Future Improvements

* Hyperparameter tuning using GridSearchCV
* Try advanced models (XGBoost, LightGBM)
* Deploy model using Streamlit or Flask
* Improve recall using SMOTE (oversampling)

---

## 👨‍💻 Author

**Ujjawal Shrivastava**
Aspiring Data Scientist | Machine Learning Enthusiast

---

## ⭐ If you found this project useful, don't forget to give it a star!
