# 🏠 Housing Price Prediction - Exploratory Data Analysis and Modeling

## Overview
Task3.ipynb includes exploratory data analysis and predictive modeling on a housing dataset.  
The goal is to predict housing prices based on various features.  
The notebook follows a structured workflow from data loading to model evaluation.

---

## Key Steps Performed

### 1. Data Loading and Initial Exploration
- **Libraries Imported**: pandas, numpy, matplotlib, seaborn, scikit-learn (train_test_split, LinearRegression, metrics, LabelEncoder)
- **Dataset**: `Housing.csv` containing 545 entries with 13 features, including price, area, bedrooms, bathrooms, and various categorical features about house amenities.

### 2. Data Preprocessing
- **Categorical Encoding**: Used `LabelEncoder` to convert categorical columns (mainroad, guestroom, basement, etc.) into numeric values.
- **Logarithmic Transformation**: Applied log transform to handle skewness and reduce outlier influence, particularly for the target variable `price`.

### 3. Model Building and Evaluation
- **Train-Test Split**: Divided data into training and testing sets.
- **Linear Regression**: Built an initial baseline model.
- **Regularization Techniques**: Applied Lasso and Ridge regression with hyperparameter tuning.
- **Cross-Validation**: Used cross-validation to assess model performance more reliably.
- **Performance Metrics**: Evaluated using Mean Absolute Error (MAE), Mean Squared Error (MSE), and R-squared (R²) score.

---

## Challenges and Solutions

- **Categorical Data Handling**:
  - **Problem**: Original categorical features couldn't be used directly in regression.
  - **Solution**: Applied LabelEncoder to convert them to numeric values.

- **Model Performance Issues**:
  - **Problem**: Initial models (including regularized versions) showed poor performance (low R-squared).
  - **Solution**: Attempted hyperparameter tuning and cross-validation but saw minimal improvement.

- **Data Transformation**:
  - Implemented logarithmic transformation of features and the target variable, improving R-squared to 0.66, though still not ideal.

---

## Key Observations
- The logarithmic transformation provided the most significant improvement in model performance.
- The final R-squared of **0.66** indicates the model exhibits moderate performance.
