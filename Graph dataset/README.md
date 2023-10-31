[MEDIUM link](https://medium.com/@saipraneethk181200/eda-clustering-anomaly-detection-and-automl-on-the-cora-dataset-c25238f83db0)
# Clustering, Anomaly Detection, and AutoML with TPOT

This guide outlines the process of clustering, anomaly detection, and automated machine learning on the Cora dataset.

## Prerequisites

1. Ensure you have Python 3.x installed.
2. Install necessary libraries using pip:
   ```
   pip install pandas numpy scikit-learn tpot
   ```

3. Download the Cora dataset (`nodes.csv`).

## Steps

### 1. Data Loading

Load the `nodes.csv` file using pandas:
```python
import pandas as pd
nodes = pd.read_csv("path_to_nodes.csv")
```
Replace `"path_to_nodes.csv"` with the path to your downloaded file.

### 2. Data Sampling

Given memory constraints, you might want to work with a subset of the data:
```python
sample_size = 100
nodes_sample = nodes.sample(n=sample_size, random_state=42)
```

### 3. Feature Preparation

Prepare the feature matrix. For simplicity, we're using a subset of the features:
```python
import numpy as np
X = np.array(nodes_sample['features'].apply(lambda x: x[:50]).tolist())
```

### 4. Clustering (Optional)

Apply KMeans clustering to the sampled data for demonstration:
```python
from sklearn.cluster import KMeans
y = KMeans(n_clusters=7, random_state=42).fit_predict(X)
```

### 5. Splitting the Data

Split the data into training and testing sets:
```python
from sklearn.model_selection import train_test_split
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
```

### 6. Automated Machine Learning with TPOT

Run TPOT to find the best machine learning pipeline:
```python
from tpot import TPOTClassifier
tpot = TPOTClassifier(generations=5, population_size=20, verbosity=2, random_state=42)
tpot.fit(X_train, y_train)
```

Evaluate the best model on the test set:
```python
print(f"Test set accuracy: {tpot.score(X_test, y_test)}")
```

Finally, export the best pipeline to a Python script:
```python
tpot.export('tpot_exported_pipeline.py')
```

## Conclusion

This guide provided a walkthrough of clustering, anomaly detection, and AutoML for the Cora dataset. Due to memory constraints, it's recommended to run these operations on a system with ample memory or consider cloud-based solutions.


