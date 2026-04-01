# 📊 Telecom Churn Analysis Dashboard

[![Live Demo](https://img.shields.io/badge/Power%20BI-Live%20Demo-yellow?logo=powerbi)](https://app.powerbi.com/view?r=eyJrIjoiNmI4YjI5NjItMGZhYS00Y2VmLTgxNzMtNmM4YWVmMTU1YWE2IiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9)

A Power BI dashboard for telecom customer churn analysis, integrated with a machine learning model for churn prediction. The dashboard provides both historical churn insights and forward-looking predictions to help stakeholders identify at-risk customers before they leave.

---

## 🖼️ Dashboard Preview

### Summary Page
![Churn Analysis Summary](./screenshots/summary.png)

### Prediction Page
![Churn Analysis Prediction](./screenshots/prediction.png)

---

## 📌 Project Overview

Customer churn is one of the most critical challenges in the telecom industry. This project combines exploratory data analysis with ML-powered prediction in a single Power BI report, giving business teams an end-to-end view of churn behavior.

**Key numbers from the dataset:**
- Total Customers: **6,418**
- New Joiners: **411**
- Total Churned: **1,732**
- Overall Churn Rate: **27.0%**
- Predicted Churners (ML Output): **381**

---

## 📂 Repository Structure
```
├── ChurnAnalysis.pbix          # Power BI report file
├── Predictions.csv             # ML model output (381 predicted churners)
├── data/
│   └── telecom_customers.csv   # Source dataset
├── ml_model/
│   └── churn_model.ipynb       # ML training notebook (if applicable)
├── screenshots/
│   ├── summary.png
│   └── prediction.png
└── README.md
```

---

## 📊 Dashboard Pages

### Page 1 — Churn Analysis Summary

Provides a high-level view of historical churn across demographic, account, geographic, and service dimensions.

| Section | Visuals |
|---|---|
| **KPI Cards** | Total Customers, New Joiners, Total Churn, Churn Rate |
| **Demographic** | Churn by Gender, Churn by Age Group |
| **Account Info** | Churn by Payment Method, Contract Type, Tenure Group |
| **Geographic** | Top 5 States by Churn Rate (Jammu & Kashmir at 57.2%) |
| **Services Used** | Churn by Internet Type, Churn by Service Subscriptions |
| **Churn Distribution** | Churn by Category (Competitor, Attitude, Dissatisfaction, Price) |

**Notable insights:**
- Month-to-month contract customers churn at **46.5%** vs 2.7% for two-year contracts
- Fiber Optic internet users have the highest churn rate at **41.1%**
- Customers who do NOT use Phone Service churn at **90.6%**
- Customers with >= 24 months tenure churn the most in absolute numbers (2.1K), but churn rate stabilizes around 27–28%

### Page 2 — Churn Prediction

Displays the ML model's predicted churner profiles and a customer-level risk table.

| Section | Details |
|---|---|
| **Predicted Churner Count** | 381 customers flagged as likely to churn |
| **Gender Split** | 249 Female, 132 Male |
| **Breakdown Charts** | By Age Group, Tenure, Marital Status, Payment Method, Contract |
| **State-wise Risk** | Jammu & Kashmir (57.2%) remains the highest-risk geography |
| **Customer Risk Table** | Customer ID, Monthly Charge, Total Revenue, Total Refunds, Referrals |

---

## 🤖 Machine Learning Model

The prediction output (`Predictions.csv`) contains **381 records** with 33 features including:

- Customer demographics: `Gender`, `Age`, `Married`, `State`
- Account attributes: `Contract`, `Payment_Method`, `Tenure_in_Months`
- Service flags: `Phone_Service`, `Internet_Type`, `Streaming_TV`, `Premium_Support`, etc.
- Financials: `Monthly_Charge`, `Total_Revenue`, `Total_Refunds`
- Target: `Customer_Status_Predicted` (1 = Predicted Churner)

The model was trained on historical customer data and its predictions are loaded directly into Power BI for the Prediction page visuals.

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| **Power BI Desktop** | Dashboard design and data visualization |
| **Python / Scikit-learn** | ML model training and prediction |
| **Pandas / NumPy** | Data preprocessing |
| **CSV** | Prediction output integration with Power BI |

---

## 🚀 How to Use

1. Clone the repository:
```bash
   git clone https://github.com/your-username/telecom-churn-analysis.git
```

2. Open `ChurnAnalysis.pbix` in Power BI Desktop.

3. If prompted, update the data source path to point to your local `data/` folder and `Predictions.csv`.

4. Refresh the data and explore both pages using the navigation buttons (Summary ↔ Churn Prediction).

---

## 📈 Key Business Takeaways

- Targeting **month-to-month contract** customers with retention offers could significantly reduce churn
- **Jammu & Kashmir** and **Assam** require region-specific retention strategies
- Customers leaving for **competitors** (761) represent the largest churn category — competitive pricing analysis is recommended
- Customers using **Unlimited Data** (80.1% churn) and lacking **Premium Support** (83.5% without it churn) are high-risk segments

---

## 👤 Author

**Hari**
Final Year B.Tech – Computer Science (AI), Parul University
Data Engineering Intern @ CloudServ Systems

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](https://linkedin.com/in/your-profile)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black)](https://github.com/your-username)
