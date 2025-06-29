# summer-analytics-age-prediction
# NHANES Age Group Prediction – Summer Analytics 2025, IIT Guwahati

This project was developed as part of the **Summer Analytics 2025 Hackathon** conducted by **IIT Guwahati**. The task is to build a machine learning model that classifies survey respondents as either *Adult* (age < 65) or *Senior* (age ≥ 65) using health and nutrition data from the **NHANES** dataset.

## 📝 Problem Statement

Given respondent data such as BMI, glucose levels, insulin levels, and physical activity, the task is to classify individuals into:
- **Adult (0)**: Age < 65
- **Senior (1)**: Age ≥ 65

## 📁 Dataset Description

- `train.csv`: 2,016 rows with features and `age_group` label (target)
- `test.csv`: 312 rows with only features
- `sample_submission.csv`: Format for your final predictions

### 📌 Features

| Feature | Description |
|--------|-------------|
| SEQN | Unique respondent ID |
| RIAGENDR | Gender (1 = Male, 2 = Female) |
| PAQ605 | Weekly physical activity (moderate/vigorous) |
| BMXBMI | Body Mass Index |
| LBXGLU | Glucose level |
| DIQ010 | Diabetes (Yes/No) |
| LBXGLT | Glucose Tolerance |
| LBXIN | Insulin level |

### ❗ Notes
- The target variable `age_group` must be encoded:  
  `Adult` → `0`, `Senior` → `1`
- The dataset contains missing values that must be handled appropriately.

## 🛠️ Methodology

### ✅ Preprocessing
- Handled missing values using appropriate imputation (e.g., median/mode)
- Standardized continuous features using `StandardScaler`

### ✅ Feature Engineering
- Created derived features and handled categorical encoding
- Visualized feature distributions to improve understanding

### ✅ Models Used
- Logistic Regression
- Random Forest Classifier
- Support Vector Machine (SVM)
- XGBoost Classifier
- Voting Classifier (Ensemble)

### ✅ Class Imbalance Handling
- Applied **SMOTE** to balance class distribution in training data

### ✅ Hyperparameter Tuning
- GridSearchCV for model optimization

### ✅ Evaluation Metrics
- Accuracy
- Precision, Recall, F1-score
- Confusion Matrix

## 📈 Final Results

| Model | Accuracy | Notes |
|-------|----------|-------|
| Voting Classifier | 92.3% | Best performing on validation |
| XGBoost | 91.7% | Strong individual performance |
| Random Forest | 90.4% | Good generalization |

## 📂 Project Structure

