# 📊 Exploratory Data Analysis (EDA)  
## Bivariate & Multivariate Analysis Notes

This repository contains concise and practical notes for performing **Bivariate** and **Multivariate Analysis** during Exploratory Data Analysis (EDA).

---

# 🔹 Bivariate Analysis (2 Variables)

### 🎯 Goal:
Understand the **relationship between two variables**

---

## ✅ 1. Numerical vs Numerical

### 📌 Plots to Use:
- Scatter Plot  
- Line Plot (for ordered/time data)  
- Correlation Heatmap  

### 📊 Insights:
- Linear / Non-linear relationships  
- Positive / Negative correlation  
- Outliers detection  

### 💻 Example:
```python
sns.scatterplot(x='Age', y='Fare', data=df)
