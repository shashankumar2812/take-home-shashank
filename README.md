This file gives an overview of the assignment solution. I have included detailed notes in the respective sections of the notebooks for reference specifically around the choices and the assumptions I made. The

- README.md contains summary of the work
- 01_exploratory_data_analysis.ipynb contains details of data exploration
- 02_model_development.ipynb contaains details of model development steps

## Problem

Use the publicly available IMDB Datasets to build a model that predicts a movie’s average rating.

## Data 

The data for the solution can be found on following links:

- IMDb Dataset Details [Data Description](https://www.imdb.com/interfaces/)
- IMDb Dataset [Dataset](https://datasets.imdbws.com/)

Note: I have used only 2 out of 5 tsv files to develop the solution in interest of time. More details will follow in the notebooks.


## Approach

I am solving this assignment as a standard regression problem for predicting movie ratings. My attempt while solving this assignment is to show the breadth of my knowledge and not necessarily build the best model. The current state of model development process is highly empirical and generally model development process takes multiple iterations to arrive at a solution. The general workflow in the notebook is as follows: 

1. Exploratory Data Analysis 

2. Data Preprocessing/Feature Engineering/Data Cleaning
    * Processed/Filtered invalid/null values
    * Removed special characters 

* Feature Engineering
    
* Model Selection
    * Linear Regression
    * Decision Tree
    * Random Forest
    * XGBoost
    
* Model Evaluation 
    * MSE
    * RMSE
    * MAE
    
* Hyperparameter Tuning

To choose the best solution, I will follow following strategy:

- I will iterate multiple times through EDA, Data Preprocessing, Feature Engineering and Data Cleaning (in general it takes approx 70-80% of the time) to find optimal steps. 
- Assuming no other business metric dictates, I will evaluate multiple models on metrics like RMSE and MAE.
- Time to run the algorithm and other production related constraints also play important role in choosing the best model.


## Assumptions

- The problem is a standard regression problem and the problem statement is restricted to only movie rating prediction (and not series, short movies and other content type).
- Model evaluation will be based on RMSE and the assumption is all the movies are equally important. 
-  All movies having <10 votes are filtered out with an assumption that they are outliers (somewhat arbitrary cutoff).


## If I had more time in hand

Given more time, I will consider following:

- I will speak with Business stakeholders to better understand the problem and if required, customize the solution to suit their needs. Understanding the underlying meaning of data is also important.
- I will explore other csv files and develop more features to include in the model. I will __fix data quality issues__, if they exist. In my experience, this always results in the highest improvement in model performance.
- I will iterate through exploratory data analysis, data preprocessing and data cleaning  process empirically.
- If business dictates, I will design a production solution to get the benefits of the model on regular basis (I can think of a solution to build a Production Pipeline using Airflow, AWS SageMaker, Papermill, S3 and Snowflake).
- I will consider more Machine Learning/Deep Learning models if the simpler models used in this Notebook do not suffice the primary business objective.
- I will consider evaulating the model performance by designing experiments (A/B experiment testing) by brainstorming the problem with business stakeholders.