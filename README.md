# 🚀 Neurofive Machine Learning Internship Portfolio

Welcome to my **Machine Learning Internship Portfolio**.

This repository contains my projects and assignments completed during the **Neurofive Machine Learning Internship**. Throughout the internship, I worked on data analysis, data preprocessing, visualization, regression, classification, model evaluation, hyperparameter tuning, machine learning pipelines, and ensemble learning.

The goal of this portfolio is to demonstrate my practical understanding of **Machine Learning concepts and their implementation using Python and real-world datasets**.

---

# 👨‍💻 About This Repository

During this internship, I developed practical Machine Learning skills by working through progressively challenging projects.

The projects cover:

* Exploratory Data Analysis
* Data Cleaning
* Data Preprocessing
* Feature Engineering
* Regression
* Classification
* Model Evaluation
* Hyperparameter Tuning
* Machine Learning Pipelines
* Ensemble Learning
* Random Forest
* XGBoost
* Feature Importance
* Model Interpretation

---

# 🛠️ Technologies Used

* Python
* Google Colab
* Jupyter Notebook
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* XGBoost
* Joblib

---

# 📂 Internship Projects

# 📅 Week 1 – Exploratory Data Analysis (EDA)

## 📌 Project Overview

This project focuses on **Exploratory Data Analysis (EDA)** using the Titanic dataset.

The objective was to understand the structure and quality of the dataset, identify missing values, analyze numerical and categorical features, detect duplicate records, visualize relationships between variables, and generate useful insights before building machine learning models.

## ✅ Tasks Completed

* Imported required Python libraries
* Loaded the Titanic dataset
* Displayed data using `head()`, `tail()`, and `sample()`
* Explored the dataset using `info()` and `describe()`
* Identified rows and columns
* Checked data types
* Identified missing values
* Detected duplicate records
* Classified numerical and categorical features
* Checked unique values
* Generated a correlation matrix
* Created data visualizations
* Documented observations and insights

## 📊 Dataset Summary

| Feature              | Value |
| -------------------- | ----: |
| Rows                 |   891 |
| Columns              |    10 |
| Missing Age Values   |   177 |
| Numerical Features   |     7 |
| Categorical Features |     3 |

## 📚 Learning Outcomes

* Exploratory Data Analysis
* Data Cleaning
* Missing Value Analysis
* Feature Identification
* Data Visualization
* Dataset Understanding

## 🔗 Google Colab

**EDA Notebook**

https://colab.research.google.com/drive/1sQ_Hta_KEx2aC2-Y1qba3h9551ePDPKv

---

# 📅 Week 2 – House Price Prediction using Linear Regression

## 📌 Project Overview

This project focuses on predicting house prices using **Linear Regression**.

The project introduced regression problems, feature selection, training/testing data splitting, model training, prediction, and evaluation using regression metrics.

## ✅ Tasks Completed

* Loaded the housing dataset
* Selected relevant numerical features
* Split data into training and testing sets
* Trained a Linear Regression model
* Generated house price predictions
* Evaluated the model using RMSE
* Evaluated the model using R² Score
* Compared actual and predicted prices
* Visualized prediction performance

## 📊 Evaluation Metrics

* Root Mean Squared Error (RMSE)
* R² Score

## 📚 Learning Outcomes

* Regression
* Feature Selection
* Train-Test Split
* Model Training
* Model Prediction
* Performance Evaluation
* Regression Analysis

## 🔗 Google Colab

**House Price Prediction**

https://colab.research.google.com/drive/1kxTRWZ5Y-C0Tc_bUV_oDWFK9NQvHeYv0

---

# 📅 Week 3 – Model Evaluation & Hyperparameter Tuning

## 📌 Project Overview

This project focused on evaluating a classification model beyond simple accuracy.

A **Decision Tree Classifier** was trained and evaluated using multiple classification metrics. Hyperparameter tuning was then performed using **GridSearchCV** to identify a better-performing model configuration.

## ✅ Tasks Completed

* Trained a baseline Decision Tree Classifier
* Evaluated Accuracy
* Calculated Precision
* Calculated Recall
* Calculated F1 Score
* Generated a Classification Report
* Displayed a Confusion Matrix
* Applied GridSearchCV
* Tuned multiple model hyperparameters
* Used cross-validation
* Compared baseline and optimized models

## 📊 Evaluation Metrics

* Accuracy
* Precision
* Recall
* F1 Score
* Confusion Matrix

## ⚙️ Hyperparameters Tuned

* `criterion`
* `max_depth`
* `min_samples_split`
* `min_samples_leaf`

## 📚 Learning Outcomes

* Classification
* Model Evaluation
* Classification Metrics
* Confusion Matrix
* Hyperparameter Optimization
* Cross Validation
* GridSearchCV
* Decision Tree Classification

---

# 📅 Week 4 – Task 1: Building a Proper ML Pipeline

## 📌 Project Overview

Production-ready machine learning code should not be a collection of disconnected preprocessing and model-training steps.

This project demonstrates how to build an end-to-end **Scikit-learn Pipeline** using the Titanic dataset.

The pipeline combines custom feature engineering, numerical and categorical preprocessing using `ColumnTransformer`, and model training into a single reusable estimator.

This approach helps prevent **data leakage**, improves reproducibility, and makes the machine learning workflow easier to maintain and deploy.

## 🎯 Task Objectives & Accomplishments

### Dataset Selection

Used the Titanic dataset containing:

* Numerical features
* Categorical features
* Missing values
* Discrete features

### Data Leakage Prevention

The dataset was split into training and testing sets before fitting preprocessing operations.

### Custom Feature Engineering

Created a custom Scikit-learn transformer using:

* `BaseEstimator`
* `TransformerMixin`

The transformer generated:

* `family_size`
* `is_alone`

### ColumnTransformer Implementation

#### Numerical Pipeline

```text
SimpleImputer(strategy="median")
        ↓
StandardScaler()
```

#### Categorical Pipeline

```text
SimpleImputer(strategy="most_frequent")
        ↓
OneHotEncoder(handle_unknown="ignore")
```

### Unified Pipeline

The complete workflow combines:

```text
Feature Engineering
        ↓
ColumnTransformer
        ↓
RandomForestClassifier
```

### Model Serialization

The complete pipeline was saved using **Joblib** so that it can be reused for future predictions.

## 📚 Learning Outcomes

* Scikit-learn Pipelines
* ColumnTransformer
* Feature Engineering
* Data Preprocessing
* Missing Value Handling
* One-Hot Encoding
* Feature Scaling
* Data Leakage Prevention
* Random Forest Classification
* Model Serialization
* Joblib

## 📁 Repository Files

```text
Week4_ML_Pipeline_Titanic.ipynb
titanic_ml_pipeline.joblib
```

---

# 📅 Week 4 – Task 2: Ensemble Learning – Random Forest vs XGBoost

## 📌 Project Overview

This project focuses on **Ensemble Learning**, where multiple machine learning models are combined to produce stronger and more reliable predictions.

The **Auto MPG dataset** is used to predict automobile fuel efficiency measured in miles per gallon (`mpg`).

Four regression models were compared:

1. Linear Regression
2. Decision Tree Regressor
3. Random Forest Regressor
4. XGBoost Regressor

The main objective was to understand how ensemble models perform compared with traditional single models.

---

## 🎯 Task Objectives & Accomplishments

* Loaded the Auto MPG dataset
* Explored dataset structure and statistics
* Checked missing values
* Cleaned the `horsepower` feature
* Removed unnecessary `car name` column
* Separated features and target
* Split data into training and testing sets
* Trained Linear Regression
* Trained Decision Tree Regressor
* Trained Random Forest Regressor
* Trained XGBoost Regressor
* Compared models using RMSE
* Compared models using R² Score
* Visualized model performance
* Generated Random Forest feature importance
* Generated XGBoost feature importance
* Compared important features from both ensemble models

---

## 🚗 Dataset

**Dataset:** Auto MPG

**Target Variable:**

```text
mpg
```

The dataset contains automobile characteristics such as:

* Cylinders
* Displacement
* Horsepower
* Weight
* Acceleration
* Model Year
* Origin

---

## 🤖 Models Used

| Model                   | Category       |
| ----------------------- | -------------- |
| Linear Regression       | Single Model   |
| Decision Tree Regressor | Single Model   |
| Random Forest Regressor | Ensemble Model |
| XGBoost Regressor       | Ensemble Model |

---

## 📊 Evaluation Metrics

### RMSE

**Root Mean Squared Error** measures the average magnitude of prediction errors.

A **lower RMSE** indicates better performance.

### R² Score

**R² Score** measures how much of the variation in the target variable is explained by the model.

A **higher R² Score** indicates better performance.

---

## 🌲 Random Forest

Random Forest is an ensemble learning algorithm that creates multiple decision trees independently.

The predictions from the individual trees are combined to produce the final prediction.

This approach helps reduce variance and generally produces a stable model.

---

## 🚀 XGBoost

XGBoost is a gradient boosting algorithm.

Unlike Random Forest, XGBoost builds decision trees sequentially. Each new tree attempts to correct errors made by the previous trees.

This allows XGBoost to progressively improve the prediction model.

---

## 🔍 Random Forest vs XGBoost

| Feature            | Random Forest   | XGBoost                 |
| ------------------ | --------------- | ----------------------- |
| Learning Method    | Bagging         | Boosting                |
| Tree Construction  | Independent     | Sequential              |
| Main Goal          | Reduce variance | Correct previous errors |
| Training           | Parallel trees  | Sequential improvement  |
| Feature Importance | Available       | Available               |
| Tuning Requirement | Moderate        | Usually higher          |

---

## 📈 Feature Importance

Feature importance was calculated for both Random Forest and XGBoost.

This helps identify which automobile characteristics have the greatest influence on MPG predictions.

The notebook contains separate visualizations for:

* Random Forest Feature Importance
* XGBoost Feature Importance

---

## 📊 Model Comparison

The models are evaluated using the actual test-set results generated by the notebook.

| Model             |                  RMSE |              R² Score |
| ----------------- | --------------------: | --------------------: |
| Linear Regression | Generated in Notebook | Generated in Notebook |
| Decision Tree     | Generated in Notebook | Generated in Notebook |
| Random Forest     | Generated in Notebook | Generated in Notebook |
| XGBoost           | Generated in Notebook | Generated in Notebook |

> The final values should be updated with the actual results generated after running the notebook.

---

## 📚 Learning Outcomes

* Ensemble Learning
* Random Forest Regression
* XGBoost Regression
* Decision Tree Regression
* Regression Model Comparison
* RMSE
* R² Score
* Feature Importance
* Model Interpretation
* Gradient Boosting
* Bagging
* Machine Learning Evaluation

---

## 📁 Week 4 Task 2 Repository Files

```text
W04_Ensemble_Learning_RandomForest_vs_XGBoost_AutoMPG.ipynb
auto-mpg.csv
```

## 🔗 GitHub

**Week 4 Task 2 – Ensemble Learning Notebook**

https://github.com/smartanilmali234-art/Anilmali/blob/main/W04_Ensemble_Learning_RandomForest_vs_XGBoost_AutoMPG.ipynb

---

# 📂 Complete Repository Structure

```text
Anilmali/
│
├── Week1_EDA.ipynb
│
├── Week2_HousePricePrediction.ipynb
│
├── Week3_ModelEvaluation.ipynb
│
├── Week4_ML_Pipeline_Titanic.ipynb
│
├── W04_Ensemble_Learning_RandomForest_vs_XGBoost_AutoMPG.ipynb
│
├── Titanic-Dataset.csv
│
├── auto-mpg.csv
│
├── titanic_ml_pipeline.joblib
│
├── requirements.txt
│
└── README.md
```

---

# 🎯 Skills Gained

## Data & Python

* Python Programming
* Pandas
* NumPy
* Data Cleaning
* Data Preprocessing

## Data Analysis

* Exploratory Data Analysis
* Missing Value Analysis
* Correlation Analysis
* Data Visualization
* Feature Identification

## Machine Learning

* Linear Regression
* Decision Tree Classification
* Decision Tree Regression
* Random Forest Classification
* Random Forest Regression
* XGBoost Regression
* Ensemble Learning

## Model Evaluation

* Accuracy
* Precision
* Recall
* F1 Score
* Confusion Matrix
* RMSE
* R² Score

## Advanced ML

* Feature Engineering
* Feature Scaling
* One-Hot Encoding
* ColumnTransformer
* Scikit-learn Pipelines
* Hyperparameter Tuning
* GridSearchCV
* Cross Validation
* Feature Importance
* Model Serialization

---

# 📈 Internship Progress

| Week          | Project                                  | Status      |
| ------------- | ---------------------------------------- | ----------- |
| Week 1        | Exploratory Data Analysis                | ✅ Completed |
| Week 2        | House Price Prediction                   | ✅ Completed |
| Week 3        | Model Evaluation & Hyperparameter Tuning | ✅ Completed |
| Week 4 Task 1 | Proper ML Pipeline                       | ✅ Completed |
| Week 4 Task 2 | Random Forest vs XGBoost                 | ✅ Completed |

---

# 🚀 Future Improvements

Future improvements to this portfolio may include:

* Logistic Regression
* Random Forest Classification
* XGBoost Classification
* Advanced Feature Engineering
* Cross Validation
* Hyperparameter Optimization
* Advanced Ensemble Methods
* Model Explainability
* Model Deployment using Streamlit
* REST API for ML Models
* End-to-End ML Applications
* Cloud Deployment

---

# 💡 Portfolio Goal

The goal of this internship portfolio is to demonstrate practical knowledge of **Machine Learning from data analysis to model development and evaluation**.

Through these projects, I am building experience in developing reproducible and practical machine learning solutions that can be applied to real-world problems.

---

# 👨‍💻 Author

**Anil Mali**

**Machine Learning Intern**

### GitHub

https://github.com/smartanilmali234-art/Anilmali

---

# ⭐ Acknowledgement

This repository contains my work completed as part of the **Neurofive Machine Learning Internship**.

I am continuously improving my Machine Learning skills through practical projects, experimentation, and real-world datasets.
 visiting my Machine Learning Internship Repository!
