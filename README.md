# Interpretable_ML_Assignment2
Developing interpretable models to predict which customers are at risk of churning.

## 📌 Project Overview  
This project focuses on **interpretable machine learning** techniques to analyze **customer churn** in the telecommunications industry. Customer churn refers to when customers stop using a company’s services and move to competitors. For telecom providers, reducing churn is a **critical business priority**, as retaining existing customers is often more cost-effective than acquiring new ones.  

The goal of this assignment was two-fold:  

1. **Understand the factors driving churn**  
   - Identify which customer characteristics (e.g., tenure, contract type, payment methods, value-added services) are associated with higher or lower churn risk.  
   - Ensure results are **interpretable** so that business stakeholders can translate them into actionable retention strategies.  

2. **Build and compare interpretable predictive models**  
   - **Linear Regression** (churn as a continuous 0/1 variable): establish a simple baseline, though not ideal for binary outcomes.  
   - **Logistic Regression** (churn as binary): directly model churn probability and interpret coefficients in terms of odds ratios.  
   - **Generalized Additive Models (GAM):** capture non-linear effects of features like tenure and monthly charges, providing richer insights into churn patterns.  

By evaluating assumptions, interpreting coefficients and smooth terms, and comparing performance across models, we aimed to recommend the most **effective yet interpretable model** for the telecom company to address churn.  

This makes the project not just about prediction accuracy, but also about **business interpretability and actionable insights**—helping decision-makers design data-driven retention campaigns.  

## 🗂 Repository Structure
```
Interpretable_ML_Assignment2/
│── Interpretable_ML_Assignment2.ipynb   # Main Colab notebook with code, results, and discussion
│── dataset                              # dataset
│── README.md                            # Project documentation
```

## 📑 Tasks Completed
1. **Exploratory Data Analysis (EDA)**  
   - Data cleaning, feature engineering, and visualization.  
   - Checked assumptions for Linear, Logistic, and GAM models (linearity, residuals, multicollinearity, etc.).  

2. **Linear Regression**  
   - Treated churn as continuous (0 = stay, 1 = churn).  
   - Interpreted coefficients and assessed performance.  
   - Limitations: assumption violations and poor handling of binary outcomes.  

3. **Logistic Regression**  
   - Modeled churn as a binary outcome.  
   - Interpreted coefficients as log-odds and odds ratios.  
   - Achieved strong accuracy and ROC-AUC but struggled with recall.  

4. **Generalized Additive Model (GAM)**  
   - Captured non-linear effects of variables like tenure, monthly charges, and total charges.  
   - Provided smooth effect plots for interpretability.  
   - Delivered the best balance of accuracy, F1 score, and interpretability.  

5. **Model Comparison & Recommendation**  
   - Compared performance across Linear, Logistic, and GAM.  
   - GAM recommended as the **primary model** for deployment, with Logistic Regression as a reliable benchmark.  

## 📊 Key Results
- **Linear Regression:** Accuracy ~79%, F1 ~0.53–0.58, ROC-AUC ~0.84.  
- **Logistic Regression:** Accuracy ~80%, F1 ~0.56–0.59, ROC-AUC ~0.84.  
- **GAM:** Accuracy ~79–82%, F1 ~0.60, ROC-AUC ~0.85, better recall for churners.  


## 💡 Recommendation
For the telecom company, the **Generalized Additive Model (GAM)** should serve as the **primary model** since it balances predictive performance with interpretability, especially capturing non-linear effects. **Logistic regression** should be maintained as a **benchmark model**, while **linear regression** is not recommended for business use beyond baseline exploration.  

Together, GAM and Logistic Regression provide actionable insights that can guide **customer retention strategies** while remaining interpretable to non-technical stakeholders.  

## ▶️ Running the Notebook
The project was developed and tested in **Google Colab**.  
You can open the notebook directly in Colab using this badge:  

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mobasserulHaque/Interpretable_ML_Assignment2/blob/main/Interpretable_ML_Assignment2.ipynb)  

## 📂 Dataset
- **Telco Customer Churn Dataset** from Kaggle: [Link](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)  
- Contains customer demographics, account information, and usage features.  

