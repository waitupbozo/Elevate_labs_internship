
# 🧠 Titanic Dataset Preprocessing

This project demonstrates an end-to-end data preprocessing pipeline applied to the **Titanic Dataset**. It focuses on preparing raw data for machine learning by handling missing values, encoding categorical variables, normalizing data, and dealing with outliers. These steps are essential before feeding the data into ML models.

---

## 🛠️ Tools and Libraries Used

| Tool/Library         | Description |
|----------------------|-------------|
| `pandas`             | For data manipulation and analysis. |
| `missingno`          | To visualize missing data. |
| `sklearn.impute.SimpleImputer` | To impute missing values. |
| `sklearn.preprocessing.LabelEncoder` | To encode categorical variables. |
| `sklearn.preprocessing.StandardScaler` | To standardize numerical features. |
| `matplotlib.pyplot`  | For plotting data visualizations. |
| `seaborn`            | For enhanced data visualization (especially boxplots). |

---

## 🧾 Steps Followed

### 1. **Importing Libraries and Dataset**
We loaded the Titanic dataset using `pandas.read_csv()` and imported necessary libraries for preprocessing and visualization.

### 2. **Initial Exploration**
- Displayed the first few rows using `df.head()`.
- Used `df.describe()` and `df.info()` to understand the structure and data types.
- Identified missing data using `df.isnull().sum()` and visualized it with `missingno.matrix()`.

### 3. **Handling Missing Values**
- Numerical columns like `Age` were imputed using **mean** strategy (`SimpleImputer`).
- Categorical variables like `Embarked` were encoded using `LabelEncoder`.
- The `Cabin` column's missing values were replaced with the string "UNKNOWN".

### 4. **Standardization of Numerical Features**
- Applied `StandardScaler` to normalize features such as `Age` and `Fare`.

### 5. **Outlier Detection and Removal**
- Used **boxplots** to visualize outliers.
- Defined a function using **IQR** method to remove outliers from each numerical column.
- Re-visualized the boxplots after cleaning the data.

---

## 🎤 Interview Questions & Answers

### 1. **What are the different types of missing data?**
- **MCAR (Missing Completely at Random):** Missingness has no relation to any variable.
- **MAR (Missing at Random):** Missingness is related to other observed data.
- **MNAR (Missing Not at Random):** Missingness is related to the unobserved data itself.

### 2. **How do you handle categorical variables?**
- **Label Encoding:** Assigns a unique number to each category (used here for 'Embarked').
- **One-Hot Encoding:** Converts each category into a new binary column.

### 3. **What is the difference between normalization and standardization?**
- **Normalization:** Scales values to a range (typically 0–1).
- **Standardization:** Scales values based on z-score (mean = 0, std = 1). We used this via `StandardScaler`.

### 4. **How do you detect outliers?**
- Using **boxplots** and **IQR method**:
  
  Outlier<Q1−1.5×IQRor>Q3+1.5×IQR
  

### 5. **Why is preprocessing important in ML?**
- It ensures **data quality**, removes **bias**, and improves **model performance**.
- It makes models more **generalizable** and prevents misleading patterns.

### 6. **What is one-hot encoding vs label encoding?**
- **One-Hot Encoding:** Converts each category into a new column with 0s and 1s.
- **Label Encoding:** Assigns an integer to each category.
- Use **one-hot** for **non-ordinal** data, **label** for **ordinal** or tree-based models.

### 7. **How do you handle data imbalance?**
- **Oversampling (SMOTE)** or **undersampling**.
- **Class weighting** or **ensemble methods** like **Balanced Random Forest**.
- **Synthetic data generation**.

### 8. **Can preprocessing affect model accuracy?**
Absolutely. Poor preprocessing can lead to:
- **Overfitting/underfitting**
- **Data leakage**
- **Reduced accuracy**
Proper preprocessing boosts model **robustness and performance**.



