# 🏦 Bank Customer Churn Prediction

### **Identifying At-Risk Customers with Machine Learning**

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)](https://streamlit.io/)
[![Live App](https://img.shields.io/badge/Live-App-success?style=for-the-badge&logo=streamlit)](https://customerbankchurn.streamlit.app/)

---

## 📖 Overview

**Customer retention is cheaper than acquisition.**

This project utilizes a **Machine Learning** approach to predict whether a bank customer is likely to churn (leave the bank) based on their profile and activity. By analyzing factors such as credit score, geography, and balance, the model identifies "at-risk" customers, enabling proactive retention strategies.

The solution is deployed as an interactive **Streamlit Web Application**, providing real-time risk assessments and probability scores.

> *"Turning data into retention strategies."*

---

## 📱 Web App Features

Experience the predictive model in action:

👉 **[Launch the Live App](https://customerbankchurn.streamlit.app/)**

* **⚡ Real-Time Prediction:** Instant churn probability calculation based on user inputs.
* **👥 Preset Profiles:** Quickly test the model with "Safe" vs. "Risky" customer scenarios.
* **📊 Risk Assessment:** Visual probability indicators with a professional dark-themed UI.
* **❓ Feature Insights:** Expandable help sections explaining the impact of each variable.

---

## 📊 Model Performance

The **Random Forest Classifier** was selected for its robustness and ability to handle complex data structures. Performance metrics on the test set:

* **✅ Accuracy:** `85.50%`
* **🎯 Precision:** `0.6324`
* **🔎 Recall:** `0.6260`
* **⚖️ F1-Score:** `0.6292`

*Note: The model utilizes `class_weight='balanced'` to effectively handle the imbalance between churned and retained customers.*

---

## 🛠️ Tools & Technologies Used

* **🐍 Python:** Core programming language.
* **🐼 Pandas & NumPy:** For data manipulation and analysis.
* **🌲 Scikit-Learn:** Used for model training (Random Forest), evaluation, and preprocessing.
* **⚙️ Joblib:** Used for serializing the model and scaler for deployment.
* **🌐 Streamlit:** The framework used to build the interactive web dashboard.

---

## ⚙️ The Workflow (Pipeline)

The project follows a rigorous ML pipeline from raw data to deployment.

```mermaid
graph TD;
    A["📂 Bank Customer Data
          (CSV)"] -->|Cleaning & Encoding| B{"⚙️ Preprocessing
           (One-Hot & Scaling)"};
    B -->|Handling Imbalance| C["🌲 Random Forest Model
         (Class Weight: Balanced)"];
    C -->|Evaluation| D["📊 Model Metrics
          (Acc: 85.5%)"];
    D -->|Deployment| E["📱 Streamlit Web App
         (Real-time Risk Scoring)"];

    style A fill:#f9f,stroke:#333,stroke-width:2px
    style C fill:#bbf,stroke:#333,stroke-width:2px
    style E fill:#bfb,stroke:#333,stroke-width:2px
