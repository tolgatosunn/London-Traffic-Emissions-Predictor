
# London CO2 Emissions Prediction from Traffic Data

## Introduction

This project aims to predict CO2 emissions in London by analyzing traffic data. Using Anaconda and the Scikit-Learn Python ML framework, we've developed a pipeline that cleans, transforms, and analyzes traffic and emissions data to create predictive models.

## Data Sources

- Traffic Data: 2013 Vehicle-Kilometers (VKM) data for London.
- Emissions Data: CO2 emissions data from 'LAEI2013_MajorRoads_EmissionsbyLink_2013.xlsx'.

Both datasets are publicly available on the London Datastore.

## Installation

Use the following command to install required libraries.

pip install -r requirements.txt

## Data Cleaning and Preparation

1-) Traffic Data: The LAEI2013_2013_AADT-VKM.xlsx file is split into major and minor grids, cleaned to standardize column names, remove unnecessary columns, and merge into a single dataset.

2-) Emissions Data: The emissions data is filtered to focus on CO2 emissions, and vehicle-specific emissions columns are dropped to simplify the dataset.

3-) Combining Data: Traffic and emissions data are merged by their unique identifiers, providing a complete dataset for analysis.

## Feature Engineering

1-) Categorical variables are encoded into binary features.

2-) Numeric data fields are normalized using MinMaxScaler.

3-) Feature selection is conducted through correlation analysis, identifying the most significant features for predicting CO2 emissions.

## Model Development and Evaluation

Three regression models are explored:

- Linear Regression
- Random Forest Regressor
- LightGBM Regressor

GridSearchCV is used to find the best hyperparameters for each model. The models are evaluated based on mean squared error, mean absolute error, root mean squared error, and R-squared scores.

## Results

The Random Forest Regressor, with specific hyperparameters, achieved the best performance, showcasing the predictive capabilities of the selected features in relation to CO2 emissions.