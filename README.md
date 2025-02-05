# Diabetes-Prediction-EDA-and-ML

![image](https://github.com/user-attachments/assets/404824a1-89a8-4609-ace5-aec236e039fb)


Stark Health Clinic aims to develop a robust diabetes prediction model to accurately identify individuals at risk of developing diabetes allowing for timely and targeted preventive measures.

## Project Description:
Stark Health Clinic is a private owned hospital located in Lagos, Nigeria. It was founded in 1972 by an astute medical professional. The hospital provides a wide range of medical services, including but not limited to general medicine, surgery, pediatrics, obstetrics and gynecology. The Hospital is known for its state-of-the-art facilities, modern equipment, and highly skilled medical professionals. It was then observed that an increasing number of patients presented themselves with complains including chest pains, blood pressure related issues, cholesterol level declines and stroke in some cases, hence an inquiry into the possibility of patients being at risk of a heart disease.

This project focuses on exploring and analyzing a diabetes dataset, using exploratory data analysis (EDA) and machine learning techniques to predict the likelihood of diabetes in individuals. The primary goal is to uncover key patterns and relationships within the data that can assist in identifying at-risk patients. Through Exploratory Data Analysis, I gained insights into factors such as age, blood sugar level, hypertension, and other clinical attributes. I then applied machine learning algorithms, to predict the probability of a patient having a diabetes, aiming to improve early detection and inform better clinical decision-making.

## Dataset Description
Source: Collected data from approximately 100,000 medical patients evaluated for diabetes.

Target Variable: Binary outcome indicating diabetes presence (1) or absence (0).

Independent Variables: information believed to have an influence on the outcome to predict. Eg Age, Hypertension, Blood glucose level etc

This Diabetes Dataset contains information about 100,000 medical patients evaluated for the presence of diabetes. Each record provides details on different patient characteristics that may influence the likelihood of a diabetes diagnosis. The dataset includes the following attributes:

## FEATURE NAME & DECRIPTION OF THE DATASET
gender - Gender of the individual (e.g., 'Male', 'Female').

age - Age of the individual in years.

hypertension - Whether the individual has hypertension (0 = No, 1 = Yes).

heart_disease - Whether the individual has heart disease (0 = No, 1 = Yes).

smoking_history - Smoking history of the individual (e.g., 'never', 'former', 'current').

bmi - Body Mass Index (BMI) of the individual.

HbA1c_level - Hemoglobin A1c level, indicating average blood sugar levels over the past 3 months.

blood_glucose_level - Current blood glucose level of the individual.

diabetes - Target variable indicating whether the individual has diabetes (0 = No, 1 = Yes).

## Data Preparation (EDA)
Loading the Data
Data Cleaning
Handling Missing Data
Model Building and Predictions
Summarizing and Visualization
Model Evaluation Summary

Data Cleaning and Transformation: I checked for missing values and data inconsistencies in the dataset, standardizing data to maintain model integrity. Some outliers were noted especially in the continuous variables. Most of the continuous variables (HbA1c Level, Blood Glucose Level, BMI, age) are slightly right-skewed, while majority of the categorical variables (Gender, Hypertension, Heart Disease, and Diabetes) are highly imbalanced, meaning one category dominates. This does not indicate skewness but rather class imbalance.
And in addressing the data imbalance certain weights were assigned to balance the data for optimal result.

I also explored the correlation between diabetes and other features

![image](https://github.com/user-attachments/assets/1889e613-11b1-4a01-86d1-af5f473ae4eb)


Key Positive Correlations: Diabetes is positively correlated with

HbA1c_level (0.41): indicating that higher average blood sugar levels are associated with a higher likelihood of diabetes.
Blood_glucose_level (0.42): Suggesting that increased blood glucose levels are a strong indicator of diabetes.
Age (0.26): Suggests that older individuals are slightly more likely to have diabetes.
Moderate Correlations

Bmi and age (0.34): Older individuals tend to have slightly higher BMI.
Bmi and smoking_history (0.21): Suggests a slight relationship between BMI and smoking history.
Age and smoking_history (0.3): suggests that Older individuals are more likely to have a smoking history.
Weak Correlations Heart_disease has a weak correlation with all other variables, such as blood glucose level (0.071), indicating a slight relationship. Hypertension and blood sugar level (0.085) show a minor association.

Gender shows negligible correlation with most features, indicating no strong association between gender and other factors in this dataset.



Model Building: The data was split into training and testing sets, with 80% of the data used for training the model and 20% for testing. This provided an unbiased evaluation of the model’s performance. I reviewed logistic regression and further examined other machine algorithms to determine the model with optimal effectiveness in other to reduce issues arising from false predictions as human lives are involved and the project essence is to achieve early detection and avoid needless deaths.

Model Evaluation: The Random Forest Classifier has better performance of 98% accross all metrics with False prediction of patients with and without diabetes as 411 and 422 respectively. Based on the displayed results, here’s an evaluation of the model’s performance:

Precision: This measures how many of the predicted positive cases were actually positive. Both classes (0 and 1) have a precision of 0.98, meaning that 98% of the positive predictions were correct.

Recall: This measures how many of the actual positive cases were correctly identified. The recall for both classes is 0.98, indicating that the model is effectively capturing almost all true positive cases.

F1-Score: is the harmonic mean of precision and recall. The F1-score is 0.98 for both classes, confirming a strong balance between precision and recall.

Accuracy: The overall model accuracy is 98%, showing that the model correctly classifies most of the test instances.


2. Confusion Matrix Analysis:
The confusion matrix shows:

True Positives (TP): 17017 instances were correctly predicted as not having Diabetes.
True Negatives (TN): 17216 instances were correctly predicted as having Diabetes.
False Positives (FP): 422 instances were incorrectly predicted as not having diabetes.
False Negatives (FN): 411 instances were incorrectly predicted as having diabetes.
This indicates a fair performance, with all predictions being nearly correct.

![image](https://github.com/user-attachments/assets/8f89ff25-dfbe-4a66-9e76-4d1046df190f)


## Conclusion
The evaluation of the models demonstrates that the model is highly accurate (98%), with very few false positives and false negatives. The confusion matrix further confirms the robustness of the models, strong precision and recall, meaning it correctly identifies and captures relevant instances with minimal errors. The model took 43 seconds to train, indicating reasonable training efficiency.

This Random Forest model is well-optimized for the classification task, providing high reliability in predicting outcomes. However, if further improvements are needed, fine-tuning hyperparameters might be explored.

