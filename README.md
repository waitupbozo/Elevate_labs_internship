
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





