# HR Employee Attrition Prediction

## About
This project predicts if an employee will leave the company or stay
It uses the IBM HR Analytics Attrition dataset
The dataset has 1470 employees and 35 columns
The target column is Attrition

## Dataset
File name is WA_Fn-UseC_-HR-Employee-Attrition.csv
Source is Kaggle
The data is made up by IBM so it is not real employee data
Only about 16 percent of employees left so the data is imbalanced

## Steps
1 Load the data with pandas
2 Drop columns that never change or are just IDs
   EmployeeCount Over18 StandardHours EmployeeNumber
3 Encode the text columns
   BusinessTravel is ordinal so it gets an ordered map
   Attrition Gender and OverTime are binary so they get a 0 and 1 map
   Department EducationField JobRole and MaritalStatus get one hot encoding
4 Scale the number columns with StandardScaler
5 Split the data into train and test sets
6 Train three models
   Logistic Regression
   Decision Tree
   Random Forest
7 Compare the models using confusion matrix and F1 score
8 Plot feature importance for each model

## Libraries
pandas
matplotlib
scikit-learn

## How to run
Open the notebook in Google Colab
Upload the csv file using the Files panel
Run every cell once from top to bottom
Do not run the encoding cells twice or Attrition will turn into NaN

## Notes
Accuracy can fool you here because the data is imbalanced
So F1 score and the confusion matrix are used to judge the models
