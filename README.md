# 📊 Loan Applications Data Analysis Dashboard

## Project Overview

This project demonstrates an end-to-end data analytics workflow using **SQL** and **Tableau** to analyze loan application data and uncover insights related to credit risk, loan approvals, borrower demographics, and lending trends.

The goal of this project is to showcase how data can be transformed into actionable business intelligence for financial institutions, lending organizations, and decision-makers.

---

## 🚀 Business Problem

Financial institutions process thousands of loan applications and must balance growth opportunities with credit risk.

This dashboard helps answer key business questions:

* What factors influence loan approvals?
* Which borrower segments have the highest approval rates?
* How does credit risk impact lending decisions?
* What relationship exists between income and loan amount?
* How do approval patterns vary across demographics and time?

---

## 📈 Dashboard Preview

![Loan Applications Dashboard](https://github.com/Dipenpatel303/Loan-Application-Data-Analysis/blob/main/Loan%20Application%20Approval%20Dashboard.png)

---

## 🛠️ Tools & Technologies

### SQL

* Data Extraction
* Data Cleaning
* Data Transformation
* Aggregations
* KPI Calculations
* Risk Categorization
* Business Logic Development

### Tableau

* Interactive Dashboard Design
* KPI Scorecards
* Heat Maps
* Stacked Bar Charts
* Donut Charts
* Scatter Plots
* Trend Analysis

---

## 📂 Dataset Information

The dataset contains loan application records with variables including:

* Applicant Age
* Annual Income
* Credit Score
* Marital Status
* Education Level
* Loan Purpose
* Loan Amount
* Approval Status
* Application Year

Total Records Analyzed:

**20,000 Loan Applications**

---

## 📊 Key Performance Indicators (KPIs)

| Metric                | Value      |
| --------------------- | ---------- |
| Total Applications    | 20,000     |
| Average Loan Amount   | $24,882.87 |
| Approval Rate         | 23.9%      |
| Approved Applications | 4,780      |
| Average Credit Score  | 572        |

---

## 🔍 Dashboard Components

### 1. Loan Approval by Risk Category

A heatmap showing approval patterns across:

* High Risk
* Medium Risk
* Low Risk

This analysis helps identify which credit score ranges contribute most to approved loans.

---

### 2. Loan Approval by Marital Status

Analyzes approved and rejected applications across:

* Married
* Single
* Divorced
* Widowed

Key Insight:
Married applicants represent the highest volume of approved loans.

---

### 3. Loan Approval Trends Over Time

A time-series visualization used to identify:

* Lending trends
* Approval fluctuations
* Performance monitoring opportunities

---

### 4. Age Group Distribution

Approval patterns segmented by age groups:

* 18–24
* 25–34
* 35–44
* 45–54
* 55+

Key Insight:
Applicants aged 35–44 account for the highest number of approvals.

---

### 5. Loan Approval by Education Type

Donut chart displaying approvals among:

* High School
* Associate
* Bachelor
* Master
* Doctorate

This provides insights into educational demographics of approved borrowers.

---

### 6. Income vs Loan Amount Analysis

Scatter plot comparing:

* Annual Income
* Loan Amount
* Approval Status

Key Insight:
Higher income generally supports larger loan approvals, though additional factors such as credit score and risk profile remain important.

---

## 🧮 SQL Analysis Performed

### KPI Calculation

```sql
SELECT
COUNT(*) AS Total_Applications,
AVG(Loan_Amount) AS Avg_Loan_Amount,
SUM(CASE WHEN Loan_Status='Approved' THEN 1 ELSE 0 END) AS Approved_Applications
FROM Loan_Data;
```

### Risk Categorization

```sql
CASE
    WHEN Credit_Score < 500 THEN 'High Risk'
    WHEN Credit_Score BETWEEN 500 AND 649 THEN 'Medium Risk'
    ELSE 'Low Risk'
END AS Risk_Category
```

### Approval Rate Calculation

```sql
SELECT
ROUND(
100.0 * SUM(CASE WHEN Loan_Status='Approved' THEN 1 ELSE 0 END)
/ COUNT(*),2
) AS Approval_Rate
FROM Loan_Data;
```

---

## 💡 Key Insights

* Approval rates increase among medium and low-risk applicants.
* Income and credit score strongly influence approval outcomes.
* Married applicants receive the highest number of approvals.
* The 35–44 age group represents the largest approved borrower segment.
* Education level provides additional context for borrower demographics.
* Data visualization enables rapid identification of lending patterns and risk exposure.

---

## 🎯 Business Value

This dashboard can support:

* Credit Risk Assessment
* Lending Strategy Optimization
* Portfolio Monitoring
* Customer Segmentation
* Executive Reporting
* Data-Driven Decision Making

---

## 📚 Skills Demonstrated

### Data Analytics

* Exploratory Data Analysis (EDA)
* KPI Development
* Statistical Interpretation
* Trend Analysis

### SQL

* Joins
* Aggregations
* CASE Statements
* Window Functions
* Data Transformation

### Tableau

* Dashboard Development
* Interactive Reporting
* Data Storytelling
* Advanced Visualizations

### Business Intelligence

* Financial Analytics
* Credit Risk Analysis
* Performance Measurement
* Executive Dashboarding

---

## 👨‍💻 Author

**Dipen Patel, MBBS, MPH, MPM**

Data Analyst | Public Health Professional | SQL Developer | Tableau Developer

Experienced in transforming complex datasets into actionable insights through analytics, visualization, and data-driven decision-making.

---

⭐ If you found this project helpful, please consider giving the repository a star.
