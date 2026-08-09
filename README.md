# 🚀 Neurofive Machine Learning Internship Portfolio

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green)
![NumPy](https://img.shields.io/badge/NumPy-Numerical%20Computing-blue)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-orange)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-red)
![Google%20Colab](https://img.shields.io/badge/Google-Colab-yellow?logo=googlecolab)

---

# 👨‍💻 About This Repository

This repository contains my work completed during the **Neurofive Machine Learning Internship**. Throughout the internship, I worked on data preprocessing, visualization, machine learning model development, evaluation, and hyperparameter tuning using real-world datasets.

---

# 🛠️ Technologies Used

- Python
- Google Colab
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Scikit-learn

---

# 📂 Internship Projects

## 📅 Week 1 – Exploratory Data Analysis (EDA)

### 📌 Project Overview

This project focuses on Exploratory Data Analysis (EDA) using the Titanic dataset. The objective was to understand the dataset, inspect data quality, identify missing values, classify features, and generate useful insights before building machine learning models.

### ✅ Tasks Completed

- Imported required libraries
- Loaded Titanic dataset
- Displayed dataset using head(), tail(), sample()
- Explored dataset using info() and describe()
- Identified rows and columns
- Checked data types
- Found missing values
- Detected duplicate records
- Classified numerical and categorical features
- Checked unique values
- Generated correlation matrix
- Created data visualizations
- Documented observations

### 📊 Dataset Summary

| Feature | Value |
|----------|------:|
| Rows | 891 |
| Columns | 10 |
| Missing Age Values | 177 |
| Numerical Features | 7 |
| Categorical Features | 3 |

### 📚 Learning Outcomes

- Exploratory Data Analysis
- Data Cleaning
- Missing Value Analysis
- Feature Identification
- Data Visualization

### 🔗 Google Colab

**EDA Notebook**

https://colab.research.google.com/drive/1sQ_Hta_KEx2aC2-Y1qba3h9551ePDPKv

---

# 📅 Week 2 – House Price Prediction using Linear Regression

### 📌 Project Overview

Built a Linear Regression model to predict house prices using selected numerical features. The project introduced regression problems, feature selection, model training, prediction, and evaluation.

### ✅ Tasks Completed

- Loaded housing dataset
- Selected relevant features
- Split data into training and testing sets
- Trained Linear Regression model
- Predicted house prices
- Evaluated model using RMSE and R² Score
- Compared actual vs predicted values
- Visualized prediction performance

### 📊 Evaluation Metrics

- Root Mean Squared Error (RMSE)
- R² Score

### 📚 Learning Outcomes

- Regression
- Feature Selection
- Model Training
- Performance Evaluation
- Prediction Analysis

### 🔗 Google Colab

**House Price Prediction**

https://colab.research.google.com/drive/1kxTRWZ5Y-C0Tc_bUV_oDWFK9NQvHeYv0

---

# 📅 Week 3 – Model Evaluation & Hyperparameter Tuning

### 📌 Project Overview

This project focused on evaluating a classification model beyond accuracy using Precision, Recall, and F1-Score. Hyperparameter tuning was performed using GridSearchCV to improve model performance.

### ✅ Tasks Completed

- Trained baseline Decision Tree Classifier
- Evaluated Accuracy
- Calculated Precision
- Calculated Recall
- Calculated F1 Score
- Generated Classification Report
- Displayed Confusion Matrix
- Tuned model using GridSearchCV
- Optimized multiple hyperparameters
- Compared baseline and optimized models

### 📊 Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

### ⚙️ Hyperparameters Tuned

- criterion
- max_depth
- min_samples_split
- min_samples_leaf

### 📚 Learning Outcomes

- Model Evaluation
- Classification Metrics
- Confusion Matrix Interpretation
- Hyperparameter Optimization
- Cross Validation
- GridSearchCV

---

# 📁 Repository Structure

```
Anilmali/

│── Week1_EDA.ipynb

│── Week2_HousePricePrediction.ipynb

│── Week3_ModelEvaluation.ipynb

│── Titanic-Dataset.csv

│── README.md
```

---

# 🎯 Skills Gained

- Data Cleaning
- Exploratory Data Analysis
- Data Visualization
- Machine Learning
- Linear Regression
- Decision Tree Classification
- Model Evaluation
- Hyperparameter Tuning
- Feature Engineering
- Python Programming
- Scikit-learn

---

# 🚀 Future Improvements

- Random Forest Classifier
- Logistic Regression
- XGBoost
- Feature Scaling
- Pipeline Implementation
- Cross Validation Techniques
- Model Deployment using Streamlit

---

# Week 4: Machine Learning Fundamentals – Building Proper ML Pipelines

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![scikit-learn](https://img.shields.io/badge/scikit--learn-v1.0%2B-orange)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 📌 Project Overview

Production-ready machine learning code isn't a collection of ad-hoc Jupyter notebook cells — it requires clean, modular, and leak-free architecture. This project demonstrates how to build an end-to-end **Scikit-Learn Pipeline** on the Titanic survivorship dataset.

By wrapping custom feature engineering, multi-type preprocessing (`ColumnTransformer`), and model training into a unified pipeline object, this project enforces strict training/testing boundaries to prevent **data leakage** and ensure seamless reproducibility in production environments.

---

## 🎯 Task Objectives & Accomplishments

- [x] **Dataset Selection:** Utilized the Titanic dataset containing a mix of continuous, discrete, missing, and categorical features.
- [x] **Data Leakage Prevention:** Applied train-test splitting prior to any imputation, encoding, or scaling.
- [x] **Custom Feature Engineering:** Built a Scikit-Learn compatible transformer using `BaseEstimator` and `TransformerMixin` to generate domain-specific features:
  - `family_size`: Combining `SibSp` + `Parch` + 1.
  - `is_alone`: Binary indicator flag for solo travelers.
- [x] **ColumnTransformer Implementation:**
  - **Numerical Sub-Pipeline:** `SimpleImputer(strategy='median')` ➔ `StandardScaler()`
  - **Categorical Sub-Pipeline:** `SimpleImputer(strategy='most_frequent')` ➔ `OneHotEncoder(handle_unknown='ignore')`
- [x] **Unified Pipeline Assembly:** Chained feature engineering, `ColumnTransformer`, and `RandomForestClassifier` into a single estimator object.
- [x] **Baseline Comparison:** Confirmed pipeline accuracy and F1-score match or exceed manual preprocessing approaches while writing significantly cleaner code.
- [x] **Model Serialization:** Serialized the complete pipeline using `joblib` for direct raw-data inference.

---

## 🛠️ Repository Structure

```text
├── Week4_ML_Pipeline_Titanic.ipynb   # 32-cell complete Jupyter Notebook
├── titanic_ml_pipeline.joblib         # Serialized end-to-end model pipeline
├── README.md                          # Project documentation
└── requirements.txt                   # Dependency requirements
# 👨‍💻 Author

**Anil Mali**

Machine Learning Intern

GitHub:
https://github.com/smartanilmali234-art/Anilmali

---

⭐ Thank you for visiting my Machine Learning Internship Repository!
