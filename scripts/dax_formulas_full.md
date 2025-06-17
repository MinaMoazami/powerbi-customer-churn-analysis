
# 📊 DAX Formulas for Customer Churn Analysis

This document summarizes all DAX formulas used in the Power BI project for analyzing customer churn data.

---

## 📌 1. Customer Counts

```DAX
Total Customers = COUNT('Databel-Data'[customer ID])
Unique Customers = DISTINCTCOUNT('Databel-Data'[customer ID])
```

---

## 📌 2. Churn Indicator and Churn Rate

### Churn Column (1 = Yes, 0 = No)
```DAX
Churned = IF('Databel-Data'[churn label] = "Yes", 1, 0)
```

### Number of Churned Customers
```DAX
Churned Customers = CALCULATE(COUNTROWS('Databel-Data'), 'Databel-Data'[Churned] = 1)
```

### Churn Rate
```DAX
Churn Rate = DIVIDE([Churned Customers], [Total Customers])
```

---

## 📌 3. Demographics Grouping

### Categorizing Age Groups
```DAX
Demographics = 
  IF('Databel-Data'[Age] >= 65, "Senior",
     IF('Databel-Data'[Age] < 30, "Under30", "Other"))
```

---

## 📌 4. Contract Type Classification

```DAX
Contract Category = 
  SWITCH('Databel-Data'[contracttype],
      "one Year", "Yearly",
      "two Year", "Yearly",
      "Month-to-Month", "Monthly",
      "other")
```

---

## 📌 5. Plan Type Analysis (e.g., Unlimited Plans)

You may use a calculated column or measure to classify users by plan type (example logic based on average monthly GB):

```DAX
Consumption Group = 
  SWITCH(TRUE(),
    'Databel-Data'[avg_monthly_gb_download] < 10, "Low Usage",
    'Databel-Data'[avg_monthly_gb_download] < 50, "Medium Usage",
    'Databel-Data'[avg_monthly_gb_download] >= 50, "High Usage",
    "Unknown")
```

---

## 📌 6. Geo Mapping

For visual maps, use the column with state or region info, ensure correct data category set to "State or Province".

---

## 📌 7. Additional Measures for Reporting

### Churn Rate by Plan Type
```DAX
Churn Rate (Unlimited Plan) = 
  CALCULATE([Churn Rate], 'Databel-Data'[plan_type] = "Unlimited")
```

### Churn Rate by Contract Category
```DAX
Churn Rate (Monthly Contracts) = 
  CALCULATE([Churn Rate], 'Databel-Data'[Contract Category] = "Monthly")
```

---

ℹ️ For more DAX logic, see the `.pbix` measures panel.
