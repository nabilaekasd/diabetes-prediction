# Diabetes Prediction Using Gradient Boosting

This project aims to build a machine learning model to predict diabetes risk based on **demographic** and **clinical features**. It includes a comparison of model performance using only demographic features versus using all available features.

## Dataset

The dataset is a synthetic healthcare dataset consisting of **100,000 records** and includes the following features:

- `age`
- `gender`
- `hypertension`
- `heart_disease`
- `smoking_history`
- `bmi`
- `HbA1c_level`
- `blood_glucose_level`
- `diabetes` *(target variable)*

Link: [Kaggle - Diabetes Prediction Dataset](https://www.kaggle.com/datasets/iammustafatz/diabetes-prediction-dataset)

## Objectives

1. Evaluate the predictive performance of a Gradient Boosting classifier for diabetes prediction.
2. Compare model accuracy when using:
   - **Only demographic features**
   - **All features (demographic + clinical)**

## Project Pipeline

### 1. Exploratory Data Analysis (EDA)
- Dataset overview
- Outlier detection using IQR and boxplots
- Visualizing feature distributions (numeric & categorical)
- Correlation analysis between numerical features
- Target class distribution (checking for class imbalance)

### 2. Data Preprocessing
- Handling missing values (if any)
- Encoding categorical variables (One-Hot Encoding)
- Scaling numerical features (StandardScaler)
- Handling class imbalance using **SMOTE**

### 3. Modeling with Gradient Boosting
- **Model 1**: Trained on demographic features only  
  (`age`, `gender`, `hypertension`, `heart_disease`, `smoking_history`)
- **Model 2**: Trained on **all available features**

## Model Evaluation Results

| Model    | Features Used         | Accuracy | ROC AUC |
|----------|------------------------|----------|---------|
| Model 1  | Demographic only       | 0.661    | 0.800   |
| Model 2  | Demographic + Clinical | 0.956    | 0.974   |

---

## Conclusion

- Using only demographic features provides a baseline prediction capability.
- Including clinical features (BMI, HbA1c, blood glucose) significantly boosts model performance.
- Gradient Boosting proves to be a powerful algorithm for this classification task.

## Technologies Used

- Python 3.x
- pandas, numpy
- matplotlib, seaborn
- scikit-learn
- imbalanced-learn (for SMOTE)


## Presentations

https://drive.google.com/file/d/163d26HYGRBZpZXJMayUn4J_TJFpsFhfx/view?usp=drive_link
