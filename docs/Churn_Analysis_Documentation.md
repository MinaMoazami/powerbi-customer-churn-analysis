
# 📄 Customer Churn Analysis in Power BI

## 🧩 Project Overview
This Power BI case study explores customer churn behavior in a fictional telecom company named **Databel**. The goal is to identify churn rates, uncover patterns, and propose data-driven strategies to minimize customer loss. The project was completed through the DataCamp platform and combines analytical thinking with practical dashboard design.

---

## 📘 Introduction
Customer churn—the percentage of customers who stop using a company’s services during a given time period—is a critical metric for any subscription-based business. Understanding **who is leaving**, **why they’re leaving**, and **how to prevent it** is key to business sustainability and growth.

This project aims to simulate a real-world analysis by examining customer data from a telecom provider. Using Power BI and DAX, the analysis focuses on identifying churn trends across customer contracts, demographic groups, service types, and usage patterns.

---

## 🎯 Objectives
- Quantify the customer churn rate and analyze it by multiple variables.
- Understand key demographics and behavioral features associated with churn.
- Visualize churn patterns in geographic and demographic contexts.
- Build compelling dashboards to communicate insights to stakeholders.

---

## 🧰 Tools & Techniques
- **Power BI Desktop** for visualization and report generation.
- **DAX (Data Analysis Expressions)** for calculated columns and measures.
- **Power Query** for data transformation and modeling.

---

## 📊 Key Analytical Steps

### 1. Customer Metrics
- Calculated total number of customers using `COUNT(customer ID)`.
- Compared with `DISTINCTCOUNT(customer ID)` to validate uniqueness.

### 2. Churn Labeling & Rate Calculation
- Transformed the churn label to binary format (Yes → 1, No → 0).
- Created a column `Churned` and calculated:
  - Total churned customers.
  - Churn rate = churned customers / total customers.

### 3. Churn Reason Analysis
- Visualized churn reasons with bar charts.
- Investigated why customers left (contract type, plan, satisfaction, etc).

### 4. Demographic Insights
- Created a calculated column `Demographics` to group customers:
  - Senior (65+), Under30 (<30), and Other.
- Visualized churn by age brackets using line and stacked column charts.

### 5. Geographic Visualization
- Used map visualizations to show regions with the highest churn.

### 6. Contract Category Grouping
- Classified contract types into "Yearly" and "Monthly" using DAX `SWITCH()` function.
- Compared churn behavior across contract categories.

### 7. Plan Type Analysis
- Classified customers based on data consumption or unlimited plan status.
- Compared churn rates across plan usage levels.

---

## 📊 Dashboard Breakdown

### Dashboard 1: Churn by Contract
- Focus: Contract type, internet service, customer tenure.
- Filters: Monthly vs. Yearly plans.
- Highlights: Monthly contracts linked to higher churn.

### Dashboard 2: Demographics & Geography
- Focus: Age groups, regional churn distribution, plan types.
- Charts: Maps, bar charts, demographic filters.
- Highlights: Under-30 and senior segments showed distinct patterns.

---

## 📌 Results

The analysis revealed the following key insights:

- **Contract Type:** Monthly contracts have significantly higher churn compared to yearly contracts.
- **Age Groups:** Seniors (65+) and younger customers (<30) are more likely to churn than other demographics.
- **Geography:** Certain regions had disproportionately high churn, potentially due to service quality or pricing issues.
- **Data Consumption:** High usage doesn’t guarantee retention; customers with unlimited plans still churned if not satisfied.
- **Demographics:** Age, service plan, and location play important roles in predicting churn behavior.

These insights can guide targeted retention campaigns and product/service improvements to reduce churn.

---

## 🧠 Learnings and Takeaways
- DAX is a powerful tool for modeling KPIs like churn rate.
- Visual storytelling through dashboards helps communicate complex findings.
- Power BI's map and filtering features are highly effective for segmentation analysis.
- Customer demographics and behavior patterns are critical in retention strategies.

---

## 📂 Files Included
- `Dashboard1.pbix` and `Dashboard2.pbix`: Power BI reports.
- `dax_formulas_full.md`: DAX code used for calculations.
- `README.md`: Summary of the repository.
- Dashboard previews in `/images` folder.

---

## ✅ Final Notes
This project showcases how real-world business problems like customer churn can be analyzed effectively using Power BI and DAX. It serves as a template for tackling similar issues in other subscription-based services.

---

© 2025 Mina MoazamiGoudarzi. All rights reserved.
