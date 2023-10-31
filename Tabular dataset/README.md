[MEDIUM link](https://medium.com/@saipraneethk181200/unveiling-insights-from-taxi-trip-data-a-deep-dive-with-python-and-automl-c0752306fd9f)

# Taxi Trip Data Analysis and Modeling

## Overview
This document summarizes the steps taken to analyze and model a dataset containing taxi trip data.

## Data Exploration
1. **Dataset Loading**: The dataset was loaded into a DataFrame for analysis.
2. **Basic Exploration**: We examined the dataset's basic properties, such as the first few rows, column data types, and descriptive statistics.
3. **Multivariate Analysis**: We performed multivariate analysis to understand relationships between variables.

## Data Preprocessing
1. **Handling DateTime Columns**: Date-time columns were identified, and features like year, month, day, and hour were extracted from them.
2. **Data Imputation**: 
    - For numerical columns, missing values were filled using the median of the column.
    - For categorical columns, missing values were filled using the mode.
3. **Feature Processing**:
    - Numerical columns were scaled using the RobustScaler.
    - Categorical columns with less than 10 unique values were one-hot encoded.
4. **Anomaly Detection**: Outliers were detected and removed using the Interquartile Range (IQR) method.

## AutoML with TPOT
1. **Problem Determination**: Based on the number of unique values in the target column, it was determined whether the problem was a classification or regression task.
2. **Modeling with TPOT**: TPOT, an AutoML tool, was employed to automatically find the best machine learning pipeline for the task.

## Notes
- While TPOT is a powerful tool, it can be time-consuming on larger datasets. Adjusting parameters like `generations` and `population_size` can control the runtime.
- Ensure that the correct path to the dataset is provided when replicating the process in Google Colab or other environments.
