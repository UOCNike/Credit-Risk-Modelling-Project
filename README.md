# Credit-Risk-Modelling-Project
End-to-end Credit Risk Modeling project using Machine Learning. Includes data cleaning, EDA, feature engineering, model comparison, and deployment of a Streamlit web app to predict credit risk (Good/Bad) using the German Credit dataset.


# Credit Risk Modeling Using Machine Learning

## Project Overview
This project is an end-to-end **Credit Risk Modeling** application built using **Machine Learning** techniques to predict whether a credit applicant represents a **Good** or **Bad** credit risk. The solution covers the complete data science workflow — from data preprocessing and exploratory data analysis (EDA) to model training, evaluation, and deployment using a **Streamlit web application**.

The project is based on the **German Credit Risk Dataset**, which contains demographic and financial attributes of loan applicants.

---

## Dataset Description
- **Dataset:** German Credit Risk Dataset  
- **Records:** 1,000 rows  
- **Features:** 11 columns   
- **Target Variable:** `risk`
  - `good` → Low credit risk  
  - `bad` → High credit risk  

---

## Data Preparation & Cleaning
- Loaded and explored data using **Pandas** in Jupyter Notebook
- Dropped irrelevant or non-informative columns
- Handled missing values by removing records with missing **saving** or **checking account** information, as these fields are critical for risk assessment
- Defined the target variable (`risk`) for supervised classification

---

## Exploratory Data Analysis (EDA)
Performed detailed EDA using **Matplotlib** and **Seaborn**, including:

### Univariate Analysis
- Histograms for numerical features (age, credit amount, duration)
- Box plots to detect outliers

### Categorical Analysis
- Count plots for gender, housing type, and credit purpose
- Identified dominant categories (e.g., car loans as the most common purpose)

### Bivariate & Multivariate Analysis
- Correlation heatmaps
- Scatter plots (e.g., credit amount vs age)
- Pivot tables for deeper feature interactions

### Risk-Based Insights
- Compared feature distributions between **good** and **bad** risk applicants
- Observed higher credit amounts and longer durations associated with higher risk

---

## Feature Engineering & Preprocessing
- Encoded categorical variables and target labels using **LabelEncoder**
- Saved fitted encoders as reusable `.pkl` files using **joblib**
- Split data into **training (80%)** and **testing (20%)** sets
- Applied **stratified sampling** to preserve class balance

---

## Machine Learning Models
Tree-based classification models were selected due to their robustness and ability to handle non-scaled data.

### Models Implemented:
- Decision Tree Classifier
- Random Forest Classifier
- Extra Trees Classifier
- XGBoost Classifier

### Model Selection:
- Used **GridSearchCV** for hyperparameter tuning
- Evaluated models based on accuracy and generalization
- **Extra Trees Classifier** achieved the best performance (~66% accuracy) and was selected as the final model

---

## Model Deployment (Streamlit App)
A web-based application was developed using **Streamlit** to allow real-time credit risk prediction.

### Application Features:
- User-friendly input fields for applicant details
- Loads trained ML model and encoders
- Predicts credit risk as **Good** or **Bad**
- Demonstrates how changes in inputs affect risk predictions

---

## Tools & Technologies
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- XGBoost
- Joblib
- Jupyter Notebook
- Streamlit

