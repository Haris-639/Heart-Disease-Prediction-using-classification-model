# Heart Disease Prediction

## Task Objective

The objective of this project is to predict whether a patient has heart disease based on various medical attributes such as age, cholesterol, chest pain type, blood pressure, etc.

Using machine learning classification models, we aim to:
- Build a predictive model for heart disease
- Identify which features are most influential
- Evaluate model performance using accuracy, confusion matrix, and ROC-AUC

## Dataset Used
**Dataset**= "https://www.kaggle.com/datasets/ketangangal/heart-disease-dataset-uci"

The dataset includes patient medical records with the following features:

| Feature                        | Description                                               |
|--------------------------------|-----------------------------------------------------------|
| age                            | Age of the patient                                        |
| sex                            | Biological sex                                            |
| chest_pain_type                | Type of chest pain                                        |
| resting_blood_pressure         | Resting blood pressure (in mm Hg)                         |
| cholestoral                    | Serum cholesterol (in mg/dl)                              |
| fasting_blood_sugar            | Whether fasting blood sugar > 120 mg/dl                   |
| rest_ecg                       | Resting electrocardiographic results                      |
| Max_heart_rate                 | Maximum heart rate achieved                               |
| exercise_induced_angina       | Exercise-induced chest pain                                |
| oldpeak                        | ST depression induced by exercise                         |
| slope                          | Slope of the peak exercise ST segment                     |
| vessels_colored_by_flourosopy | Number of major vessels colored by fluoroscopy             |
| thalassemia                    | Thalassemia defect type                                   |
| target                         | Binary Target— 1: Heart Disease, 0: No Disease            |


## Models Applied

- **Logistic Regression** using `sklearn.linear_model.LogisticRegression`

### Preprocessing Steps:

- Handled missing values (none present)
- Encoded categorical variables using Label Encoding
- Outliers identified in numerical features using the IQR method
- Split dataset into training and test sets (80/20 split)


## Key Results and Findings

| Metric                    | Value         |
|---------------------------|---------------|
| Accuracy (Test Set)       | ~ 0.7902439024390244  |
| ROC AUC Score             | ~ 0.8654102417666095 |

- Confusion matrix was plotted to visualize true vs predicted classes.
- ROC Curve demonstrated how well the model distinguishes between positive and negative cases.
- Feature importance was extracted using model coefficients.

### Insights:

- Logistic Regression performed reasonably well in classifying heart disease presence.
- Although Decision tree was giving better accuracy but didn't used it as data may be overfitting
- Features such as chest pain type, thalassemia, and oldpeak were among the most important contributors based on model coefficients.
- The model can be improved by trying more advanced classifiers and tuning hyperparameters.
