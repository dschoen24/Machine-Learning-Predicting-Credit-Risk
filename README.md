# Machine-Learning-Predicting-Credit-Risk

________________________________________________________________________________________________________________________________________________________

## Overview

Needed to build a machine learning model that attempts to predict whether a loan from Lending Club will become high risk or not.

_________________________________________________________________________________________________________________________________________________________

## Background

I used an entire year's worth of data (2019) to predict the credit risk of loans from the first quarter of the next year (2020).

________________________________________________________________________________________________________________________________________________________

## Preprocessing

I created a traning set from the 2019 loans data set using pd.get_dummies() to convert the categorical data to numeric columns.  I then created a testing set from the 2020 loans data set also converting the categorical data to numeric columns.  I then used code to fill in any missing categories in the testing set.

## Considering the Models

I compared this data by creating a Logistic Regression Model and a Random Forests Classifier Model.  

### Prediction:  

I feel that a Random Forest Classifier will perform better than a Logostic Regression Model based on the fact that a Random Forest Classifier can capture more complex feature patterns to provide the best accuracy while the Logistic Regression does not give us a discrete output but the probability associated with each output.

### Logistic Regression Model and Score (Unscaled Data)

![Logistic Regression Unscaled](https://user-images.githubusercontent.com/82673788/135774636-33a9aff9-52e5-4351-95e9-5f1f362c41b6.PNG)

### Random Forest Classifier and Score (Unscaled Data)

![Random Forest Classifier Unscaled](https://user-images.githubusercontent.com/82673788/135774990-a2939a31-8b7f-445c-b933-f481e2880ea0.PNG)

### Outcome

The Random Forest Classifier did out perform the Logistic Regression Model with a better accuracy rate.  This outcome was in line with my prediction

______________________________________________________________________________________________________________________________________________________

## Scaling the Data

The data in these models was never scaled so I used StandardScaler to scale the training and testing sets for both the Logistic Regression Models and the Random Forest Classifier Model.

### Scaling Prediction

Scaling the data will normalize all features so that each feature contributes approximately proportionately to the final distance.  Because our data will now be more evenly distributed, I predict that the Scaled data will perform better than our unscaled data.

### Logistic Regression Model and Score (Scaled Data)

![Logistic Regression Scaled](https://user-images.githubusercontent.com/82673788/135775270-edae4197-d33b-4e70-8cd6-43b48b4989ae.PNG)

### Random Forest Classifier and Score (Scaled Data)

![Random Forest Classifier Scaled](https://user-images.githubusercontent.com/82673788/135775277-6a665961-399c-4612-b575-debc35217e55.PNG)

_____________________________________________________________________________________________________________________________________________________________

## Comparison DataFrame

I created a DataFrame to hold all the scoring results from each of the models for easier comparison

![Data Frame of Results](https://user-images.githubusercontent.com/82673788/135775370-e1c64e58-92d4-4b89-88c7-2824e4570488.PNG)

## Conclusion:

It appears that overall the Random Forest Classifier gave us better accuracy over the Logistic Regression Model for both the Scaled and Unscaled data.  However, scaling the data did not improve the scoring and remained consistant expect for the Q1 2020 data in which the Logostic Regression Model was at 0.55 for unscaled and jumped to 0.75 for scaled.


