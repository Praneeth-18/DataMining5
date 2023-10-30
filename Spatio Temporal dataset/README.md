# Chickenpox Cases Analysis and Modeling

## Table of Contents
1. Data Exploration and Preprocessing
2. Clustering
3. Anomaly Detection
4. Modeling with AutoML Approach
5. Conclusions

## 1. Data Exploration and Preprocessing
- The dataset contains the number of chickenpox cases for various regions in Hungary for specific dates.
- No missing values or duplicates were found in the dataset.
- A temporal analysis showed a clear seasonal pattern in chickenpox cases.
- Spatial analysis revealed that Budapest has the highest average number of chickenpox cases.
- Date was split into 'Year', 'Month', and 'Day' columns.
- Data normalization was performed using Min-Max Scaling.

## 2. Clustering
- KMeans clustering was applied to cluster regions based on chickenpox cases.
- Four clusters were identified, grouping regions with similar chickenpox patterns.

## 3. Anomaly Detection
- Isolation Forest was used to detect anomalies in the dataset.
- The region "NOGRAD" was identified as an anomalous region based on its chickenpox pattern.

## 4. Modeling with AutoML Approach
- Time-series forecasting was performed for the "BUDAPEST" region.
- Four models were trained and evaluated:
    1. Linear Regression
    2. Random Forest
    3. Gradient Boosted Trees
    4. Ensemble of the above models
- Gradient Boosted Trees achieved the best RMSE, followed closely by the ensemble model.

## 5. Conclusions
- The dataset provides valuable insights into the temporal and spatial patterns of chickenpox cases in Hungary.
- Modeling suggests that the Gradient Boosted Trees and ensemble methods can be effective for predicting future chickenpox cases.

---
