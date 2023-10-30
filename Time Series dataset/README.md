
# McDonald's Locations Analysis README

## Overview:

This project involves analyzing a dataset containing information about specific locations, potentially representing McDonald's outlets. The dataset contains geographical data, activity status, and other metadata. This README provides a detailed walkthrough of the data exploration, preprocessing, clustering, anomaly detection, and machine learning modeling using AutoML.

## Table of Contents:

1. **Data Exploration and Preprocessing**:
    - Initial Data Overview
    - Missing Values Handling
    - Data Cleaning and Transformation
    - Geographical Data Visualization

2. **Clustering**:
    - KMeans Clustering based on Geographical Data

3. **Anomaly Detection**:
    - Identifying outliers within clusters

4. **AutoML for Predictive Modeling**:
    - Using H2O's AutoML for automated machine learning

---

## 1. Data Exploration and Preprocessing:

**Initial Data Overview**: The dataset was loaded and examined to get an understanding of the columns, data types, and overall structure.

**Missing Values Handling**: Missing values in the `state` and `city` columns were identified and filled using a placeholder value, "Unknown".

**Data Cleaning and Transformation**: 
- Addressed inconsistencies like "Maharastra" in the `state` column.
- Transformed the `last_checked` column to represent the number of minutes since the last check.

**Geographical Data Visualization**: A scatter plot of the locations based on latitude and longitude was generated to visualize the geographical spread of the outlets.

---

## 2. Clustering:

**KMeans Clustering**: The locations were clustered based on latitude and longitude using the KMeans algorithm. Five clusters were chosen for simplicity, and the cluster centers were visualized on a scatter plot.

---

## 3. Anomaly Detection:

After clustering, anomalies or outliers were detected within each cluster based on their distance from the cluster center. The Z-score was computed for each data point's distance from its cluster center, and points with a Z-score greater than 3 were flagged as anomalies.

---

## 4. AutoML for Predictive Modeling:

H2O's AutoML was used to automate the machine learning process. The target variable chosen for demonstration was `is_broken`.

**Steps**:
- The data was loaded into H2O and split into training and test sets.
- The AutoML process was configured to run for a certain duration or until a specified number of models were trained.
- A leaderboard of models, ranked based on a chosen metric (AUC in this case), was displayed.
- The best model's performance was evaluated on the test set.
  
Note: The H2O AutoML process also includes an ensemble model (Stacked Ensemble) which combines the predictions of multiple models.

---

## Execution:

The provided code snippets can be executed in a Python environment, preferably Jupyter or Google Colab notebooks. Make sure to install the necessary libraries and adjust file paths as needed.

---

This README provides a structured overview of the entire process, from data exploration to predictive modeling. For detailed code and explanations, refer to the provided Python notebooks or scripts.
