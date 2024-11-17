# Wind_Turbine_Energy_Prediction
![Logo_Green_Transparent](https://github.com/user-attachments/assets/f4fe13b8-1cd2-4450-b17c-d1ac93a5a25f)

## Table of Cotents
- [Project Overview](#project-overview)
- [Project Objectives](#project-objectives)
- [Data Cleaning](#data-cleaning)
- [Feature Engineering](#feature-engineering)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-EDA)
- [Mean Encoding](#mean-encoding)
- [Modellinf](#modelling)
- [Hyperparameter Tuning](#hyperparameter-tuning)
- [Inference Script Creation](#inference-script-creation)

###Project Overview 
Clean Energy Innovations Inc. is embarking on a mission to develop predictive models for renewable energy generation, specifically targeting sources like solar and wind to help overcome the challenges posed by the variable and unpredictable nature of renewable energy sources, ensuring a consistent and reliable energy supply.

###Project Objectives
The goal of the project is to develop precise machine learning models for predicting renewable energy generation. By achieving this primary objective, they intend to optimize the seamless integration of renewable energy sources like solar and wind into the existing energy grid. The improved prediction accuracy will naturally lead to enhanced grid stability, reduced fluctuation in energy supply, improved resource management for cost-effective energy production, and a lowered environmental footprint in energy generation.

###Data Cleaning
1.	Check for missing values
2.	Chane the timestamp to the correct datatypes
3.	Set the timestamp as index
4.	Check for duplicates

###Feature Engineering 
I went ahead to extract some features out of the existing dataset, features like quarter, month, weeks by number, hour. Also grouped the month into seasons like spring, summer, fall, and winter.

###Exploratory Data Analysis
Univariate Analysis:  There is large frequency of 0kw power generated in the turbine system, most especially across Fall and Winter season while spring has the least down time in terms of Zero power generation.
Multivariate Analysis: Exploring two or more features against each other

###Mean Encoding:
Encoded categorical variables (season & wind orientation) into numerical variables using mean encoding.

###Modelling
Split the dataset into train and test set, then trained the train dataset on the following machine learning algorithms
1.	Linear Regression
2.	Random Forest Regressor, 
3.	Gradient Boosting Regressor, and
4.	SVR

After training the test set with the algorithms above, we placed the tested the trained algorithm on the test set and evaluate the performance using the mean squared error, mean absolute error and picked the best performing models which are Random Forest Regressor and Gradient Boosting Regressor.

###Hyperparameter Tuning
Performed h Hyperparameter tuning on the best performing models using hyperopt and Bayesian optimization. Hyperparameter Tuning performed less, then we reverted to the original models.

###Inference Script Creation
We create a function that will automate all the processes in this project, and these functions could be running in a flask app or a docker container or whatever platform it could be deployed on.
