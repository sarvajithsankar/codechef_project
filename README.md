# 📊 Customer Churn Prediction: Strategic Analysis

[![Open In Colab](https://colab.research.google.com/drive/1t0vcIMEtz0nGx2mLMBRYfMlItxSJh0JH?usp=sharing)
![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Library](https://img.shields.io/badge/Library-Scikit--Learn-orange)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 📌 Executive Summary
In the telecom industry, acquiring a new customer is 5-25x more expensive than retaining an existing one. This project utilizes **Machine Learning (Gradient Boosting)** to predict which customers are at risk of leaving ("Churning").

By analyzing the behavior of **7,000+ customers**, we developed a predictive model that identifies at-risk users with **77% sensitivity (Recall)**, enabling the support team to intervene proactively before a customer leaves.

## 🔍 Key Insights & Discovery
During the Exploratory Data Analysis (EDA), we uncovered several critical patterns:
* **The "Month-to-Month" Trap:** Customers on monthly contracts are significantly more likely to churn compared to those on 1-year or 2-year plans.
* **The "12-Month Cliff":** Churn risk is highest in the first year. If a customer stays past 12 months, their loyalty increases drastically.
* **Price Sensitivity:** Higher monthly charges correlate with churn, but primarily for customers without tech support or backup services.

## 🛠️ Tech Stack
* **Language:** Python 🐍
* **Data Manipulation:** Pandas, NumPy
* **Visualization:** Seaborn, Matplotlib
* **Machine Learning:** Scikit-Learn (Gradient Boosting Classifier, Random Forest)
* **Interactive Simulation:** Ipywidgets

## 🧠 Model Performance
We moved beyond standard Accuracy metrics to focus on **Recall**, as missing a churning customer is costly.

| Metric | Score | Interpretation |
| :--- | :--- | :--- |
| **Accuracy** | **~75%** | Correctly predicts the outcome 3 out of 4 times. |
| **Recall (Churn)** | **~77%** | Captures 77% of all customers who are about to leave. |
| **Precision** | **~52%** | When we flag a customer, there is a >50% chance they are truly at risk. |

> **Technique Used:** We utilized **Threshold Moving** (lowering the decision boundary to 0.3) to prioritize catching churners over raw accuracy.

## 🚀 How to Run
1.  Click the **"Open in Colab"** badge at the top of this README.
2.  Run the notebook cells sequentially.
3.  Scroll to the bottom to try the **Interactive Churn Simulator**, where you can adjust customer details and see real-time risk predictions.

## 🔮 Future Scope
* **Deployment:** Build a web application using **Streamlit** for the customer success team.
* **Explainability:** Implement **SHAP (SHapley Additive exPlanations)** values to give individual reasons for why a specific customer was flagged.
* **Deep Learning:** Experiment with a Neural Network (MLP) using PyTorch for potentially higher accuracy.

---
**Author:** Sarvajith Sankar

*Built for the CodeChef VIT Recruitment Task*
