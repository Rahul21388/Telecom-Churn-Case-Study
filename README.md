# Telecom Churn Prediction Case Study

## 📌 Problem Statement

In the telecom industry, customers can choose from multiple service providers and switch between them, leading to an average annual churn rate of 15-25%. Given that acquiring a new customer costs 5-10 times more than retaining an existing one, customer retention is a top priority.

For telecom companies, identifying high-risk customers and understanding churn indicators is essential for reducing customer loss and improving profitability.

## 🔍 Business Objective

- Predict which customers are likely to churn in the future.
- Identify key factors influencing customer churn.
- Help telecom companies implement targeted retention strategies.

This project is focused on the **Indian and Southeast Asian markets**, where the prepaid model dominates.

## 📖 Understanding Churn

There are different ways to define churn:

1. **Revenue-Based Churn:** Customers who have not generated any revenue over a specific period.
2. **Usage-Based Churn:** Customers who have not used any telecom services (calls, SMS, mobile internet) over a given time.

For this project, **we define churn using the usage-based definition**, considering customers who have neither made calls nor used mobile data in a specific period.

### 📊 High-Value Customers

- In the Indian and Southeast Asian markets, **80% of revenue comes from the top 20% of customers**.
- The focus of this study is on **high-value customers**, defined as those who have recharged above the 70th percentile in the first two months.

## 🗂️ Dataset Overview

The dataset contains **customer-level information for four consecutive months** (June–September), encoded as 6, 7, 8, and 9.

| Phase  | Time Period | Description |
|--------|------------|-------------|
| Good Phase | June & July | Customers use services normally |
| Action Phase | August | Customers start showing signs of churn |
| Churn Phase | September | Customers who have stopped using services |

### **Data Dictionary**
The dataset contains multiple attributes related to customer activity, including:

- Call usage (incoming & outgoing)
- Mobile data usage (2G/3G)
- Recharge patterns
- Customer demographics

## Dataset Download
Due to GitHub's file size limit, the dataset can be downloaded from:
📥 [Download Dataset](https://drive.google.com/file/d/1SWnADIda31mVFevFcfkGtcgBHTKKI94J/view?usp=sharing)

📌 **Data Dictionary**: [Download Here](https://view.officeapps.live.com/op/view.aspx?src=https%3A%2F%2Fcdn.upgrad.com%2FUpGrad%2Ftemp%2Fa625d1ee-b8d7-4edb-bdde-b1d82beaf5b4%2FData%2BDictionary-%2BTelecom%2BChurn%2BCase%2BStudy.xlsx&wdOrigin=BROWSELINK)

## 🛠️ Data Preparation Steps

1. **Feature Engineering:**  
   - Create new features that could indicate customer churn based on domain knowledge.
  
2. **Filter High-Value Customers:**  
   - Identify customers who have recharged above the **70th percentile** in the good phase.

3. **Tag Churners:**  
   - Customers who have not made any calls or used mobile data in the churn phase are labeled as **churners (1), else 0**.

4. **Remove Churn Phase Attributes:**  
   - Drop features related to the churn phase to ensure unbiased predictions.

## 🚀 Model Development

The project involves building **predictive models** to identify customers likely to churn.

### **Modeling Approach**
- **Step 1:** Preprocess data (handle missing values, format conversions, etc.)
- **Step 2:** Perform exploratory data analysis (EDA) to gain insights
- **Step 3:** Engineer new features from raw data
- **Step 4:** Reduce dimensionality using **Principal Component Analysis (PCA)**
- **Step 5:** Train multiple machine learning models:
  - **Logistic Regression**
  - **Decision Trees / Random Forest**
  - **Gradient Boosting Models (XGBoost, LightGBM)**
- **Step 6:** Handle class imbalance (as churn is typically low at 5-10%)
- **Step 7:** Evaluate models using appropriate metrics (precision, recall, F1-score)

### **Key Evaluation Metrics**
- **Recall (Sensitivity):** More important than accuracy as predicting churners correctly is the priority.
- **Precision-Recall Curve:** Helps to select the best threshold for churn classification.
- **Feature Importance Analysis:** Helps telecom companies understand churn indicators.

## 📌 Key Insights & Business Recommendations

- Identify **early warning signs of churn** (e.g., decreasing recharges, lower call duration, reduced data usage).
- Implement **personalized retention strategies** (e.g., offering discounts, better data plans).
- Improve **customer experience** based on identified churn triggers.

## 🏁 Conclusion

By leveraging machine learning, this project aims to **predict churn effectively and reduce revenue loss** by proactively retaining high-value customers.

---

## 🔗 Repository Structure
