# Capstone Project - Stroke Prediction using Machine Learning

<img align="left" height="200" src="images/stroke-img.jpg"/>

According to the World Stroke Organization (WSO), stroke is the second-leading cause of death in the world and the third-leading cause of death and disability combined. 
Stroke can be prevented with appropriate public policy action to address risk factors and increased public awareness.

The aim of this project is to develop and evaluate a suitable machine learning model to predict the risk of stroke. The project utilizes different features to identify everyone's risk of stroke. And to provide early preventive measures and/or treatments to the possible high risk groups.

<br>

## Role and Objective
As the author of the dataset did not indicated the source of the data, I would assume the dataset belongs to Hospital X, and I am working as an Data Analyst in Hospital X.

My task is to develop an suitable machine learning model to predict whom are the patients potential at risk of developing stroke based on hospital's patient information records.
This is to allow the hospital to identify these group of potential high risk patients (existing/new), to provide preventive measures or treatments as early as possible to reduce the incidence rate/complications of the disease.

Reduction of incidence / complications of the disease would lessen the hospital's manpower and resources required to treat these patients, eg. shorter hospital stay, and lesser manpower required.

Patient's level of satisfactory could also be increased as the patient sees that the hospital showing genuine concerns regarding their health status, and would choose the hospital as most preferred to go to for any medical services required.


## Dataset
[Dataset Source](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset "Kaggle Home")

##### Attribute Information
There are total 5110 records records in the dataset.<br>
There are 10 feature columns and 1 target column in the dataset.

|Attribute|Description|
|:--:|:--|
|gender|"Male", "Female" or "Other"|
|age|age of the patient|
|hypertension|0 if the patient doesn't have hypertension, 1 if the patient has hypertension|
|heart_disease|0 if the patient doesn't have any heart diseases, 1 if the patient has a heart disease|
|ever_married|"No" or "Yes"|
|work_type|"children", "Govt_jov", "Never_worked", "Private" or "Self-employed"|
|Residence_type|"Rural" or "Urban"|
|avg_glucose_level|average glucose level in blood|
|bmi|body mass index|
|smoking_status|"formerly smoked", "never smoked", "smokes" or "Unknown"* |
|stroke|1 if the patient had a stroke or 0 if not|

*Note: "Unknown" in smoking_status means that the information is unavailable for this patient
<br clear="left"/>

##### Sample of the dataset
<figure>
    <img src="images/dataset-head1.jpg"/>
</figure>
<br clear="left"/>

##### Distribution of the dataset attributes

<img src="images/dataset-img0a.jpg"/>
<img src="images/dataset-img0b.jpg"/>
<br clear="left"/>

## Data Processing
* Populate null values in BMI attribute with the average value of the column.
* Perform one-hot encoding on categorical data.
* Check for duplicate records.
* Check for outliers in the dataset and justify whether to remove or not to remove.

## ML Models Used
- Logistic Regression
- XGBoost

## Steps
* Splitting dataset into training & test sets. 
* Train the above models using the training dataset.
* Compare & evaluate results on the different ML models, 
    - No minority oversampling done on the training and test dataset.
    - Minority oversampling on the training dataset but not on the test dataset.
    - Minority oversampling done on both the training and test dataset.
    - Minority oversampling done on both the training and test dataset, and with outliers removed.

## Test Results
[Test Results](FinalResults.pdf)

<img src="images/TestResult1.jpg"/>
<img src="images/TestResult2.jpg"/>
<img src="images/TestResult3.jpg"/>
