# Stroke Prediction

# Overview
This project aims to predict whether an individual will develop stroke or not based on various health indicators. 
As we have to classify the individual in either category of stroke, its a classic logistic regression problem.


## Dataset Description
--------------------------

**Data Set Characteristics:**

    :Number of Instances: 4088

    :Number of Attributes: 4 numeric + 5 categorical  predictive attributes and the numerical target

    :Attribute Information:
     #   Column             Non-Null Count  Dtype  
        ---  ------             --------------  -----  
        0   gender             4088 non-null   object 
        1   age                4088 non-null   float64
        2   hypertension       4088 non-null   int64  
        3   heart_disease      4088 non-null   int64  
        4   ever_married       4088 non-null   object 
        5   work_type          4088 non-null   object 
        6   Residence_type     4088 non-null   object 
        7   avg_glucose_level  4088 non-null   float64
        8   bmi                3926 non-null   float64
        9   smoking_status     4088 non-null   object 

    :Missing Attribute Values: bmi : 126 entries

The target variable is the stroke possibility expressed in either 1 or 0.


### Approach
1. Exlore the dataset 
3. Data preprocessing 
4. Analyze correlations
5. Train and evaluate model 
6. Verify in test dataset


#### Explore the dataset 
    Few observation after analyzing the dataset
    - gender : majority of the samples are of female gender
    - One sample wheer gender = other
    - hypertension and heart_disease : Significant over representation of no hypertension and no heart disease 
    - work_type : significant majority of the work_type as private
    - ever_married : clear majority of the ever_married=true population
    - bmi, age, avg_glucose_level : have to club them in bins based on range and try as data is very sparse
        based on bins,
            - majority the samples are of age>30 and
            - bmi between 25-40 and
            - avg_glucose_level between 50-100
    - smoking_status : major cases fall in either never_smoked and unknown category

#### Data preprocessing 
    - Handling missing and duplicate values
        - bmi was missing from many samples, replaced the missing value with mean value the bmi. 
        - checked to see if any duplicate present accross all features together : didn't find any.
    - Encoding categorical features using one hot encoding
        -   The dataset has few categorical features 'gender','work_type','ever_married','Residence_type','smoking_status'. 
        -   The encoding creates several additional features with numerical values, this will be helpful of model training.   

#### Analyze correlations
#### Train and evaluate model 
#### Verify in test dataset




## Reference
- [Stroke Prediction by 123 of AI (Dec 2023)](https://kaggle.com/competitions/stroke-prediction-by-123-of-ai-dec-2023) by [Abbhinav Venkat](https://www.kaggle.com/abbhinavvenkat)