
# 🚢 Exploratory Data Analysis: Titanic Dataset

## 📌 1. Introduction

This report presents an exploratory data analysis of the Titanic dataset. The goal is to understand the underlying patterns, relationships, and potential factors that influenced passenger survival. We use various data visualization and statistical techniques to uncover insights and answer key questions.

---

## 🗂️ 2. Data Loading and Initial Exploration

**Tools Used:**

- **Pandas**: For data manipulation and analysis.
- **Matplotlib & Seaborn**: For creating visualizations.
- **Missingno**: For visualizing missing data patterns.

**Steps:**

1. Import libraries: `pandas`, `matplotlib`, `seaborn`, `missingno`, `scipy.stats`
2. Load dataset with `pd.read_csv()`
3. Visualize missing values using `msno.matrix()`

**Insights:**

- Dataset includes demographics, travel details, and survival status.
- Missing values in 'Age', 'Cabin', and 'Embarked' columns.

---

## 🧹 3. Data Cleaning and Preprocessing

**Steps:**

1. Handle missing values:
    - Impute 'Age' with mean
    - Fill 'Cabin' with 'UNKNOWN' or else drop the column
    - Fill 'Embarked' with mode
2. Use `describe()` and `value_counts()` for stats

**Insights:**

- Average age ≈ 30.
- Majority were in Pclass 3.
- More males than females.
- Most passengers embarked from Southampton(S).

---

## 📊 4. Univariate and Bivariate Analysis

**Steps:**

1. Plot histograms and boxplots for numerical features
2. Correlation matrix with `df.corr()` + heatmap
3. Use `sns.pairplot()` to explore feature relationships

**Insights:**

- Age and Fare appear to have some correlation with survival.
- There might be a relationship between Pclass and survival.

---

## 📈 5. Statistical Testing

**Tools:**

- `scipy.stats`: Chi-square and t-tests

**Tests:**
- **Chi-Square Test:** p-values less than 0.05 suggest a significant relationship with survival.
    - Sex: **p < 0.05** (significant)
    - Pclass: **p < 0.05** (significant)
    - Embarked: **p < 0.05** (significant)

- **T-Test:** p-values less than 0.05 suggest a significant difference in means between survivors and non-survivors.
    - Age, Pclass: **p < 0.05**

---

## ✅ 6. Conclusion

- **Sex**: Females had higher survival rates
- **Pclass**: Higher classes = better survival
- **Age**: Younger = more likely to survive
- **Embarked**: Embarkation port influences survival
- **Fare**: Higher fare = better odds

These findings can guide predictive modeling and deepen understanding of the Titanic tragedy.

---
