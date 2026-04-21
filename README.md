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




## ✅ 2. Categorical vs Numerical

📌 **Use:**
- Bar Plot
- Box Plot
- Violin Plot

📊 **Insights:**
- Compare averages across categories
- Understand spread and skewness

💻 **Example:**
```python
sns.barplot(x='Pclass', y='Age', data=df)
sns.boxplot(x='Pclass', y='Age', data=df)
```

---

## ✅ 3. Categorical vs Categorical

📌 **Use:**
- Countplot
- Stacked Bar Chart
- Crosstab

📊 **Insights:**
- Frequency comparison
- Relationship between categories

💻 **Example:**
```python
sns.countplot(x='Pclass', hue='Survived', data=df)
pd.crosstab(df['Pclass'], df['Survived'])
```

---

## 🔹 Multivariate Analysis (3+ Variables)

### 🎯 Goal
Understand complex relationships among multiple variables. Multivariate analysis helps reveal deeper patterns and interactions between several variables.

---

### ✅ Common Techniques

#### ✔️ 1. Pairplot
Visualizes pairwise relationships across multiple variables

```python
sns.pairplot(df, hue='Survived')
```

#### ✔️ 2. Correlation Heatmap
Shows correlation between numerical variables

```python
sns.heatmap(df.corr(), annot=True)
```

#### ✔️ 3. GroupBy Analysis
Aggregates data for better insights

```python
df.groupby('Pclass')['Survived'].mean()
```

#### ✔️ 4. Multivariate Scatter Plot
Adds a third variable using hue/size

```python
sns.scatterplot(x='Age', y='Fare', hue='Survived', data=df)
```

#### ✔️ 5. FacetGrid
Creates multiple plots for subsets

```python
sns.FacetGrid(df, col='Pclass').map(sns.scatterplot, 'Age', 'Fare')
```

---

## 🧠 Quick Cheat Sheet

| Variable Types | Best Plots |
|---|---|
| Numerical vs Numerical | Scatter, Line, Heatmap |
| Categorical vs Numerical | Bar, Box, Violin |
| Categorical vs Categorical | Countplot, Crosstab |
| Multivariate | Pairplot, Heatmap, GroupBy |

---

## ⚠️ Key Insights

- 📌 Use **scatter plots** for numerical relationships
- 📌 Use **bar/box plots** for category comparisons
- 📌 Use **countplots** for categorical frequency
- 📌 Use **heatmaps** to understand correlations
- 📌 Use **pairplots** for overall dataset understanding
