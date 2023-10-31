# Image Analysis with AutoML

A comprehensive guide to exploring, clustering, and modeling an image dataset using Automated Machine Learning (AutoML).

## 📌 Table of Contents

- [Introduction](#-introduction)
- [Initial Exploration and Visualization](#-initial-exploration-and-visualization)
- [Clustering with KMeans](#-clustering-with-kmeans)
- [Anomaly Detection](#-anomaly-detection)
- [Building Models with H2O's AutoML](#-building-models-with-h2os-automl)
- [Conclusion](#-conclusion)

## 🚀 Introduction
This repository provides a step-by-step guide to analyzing an image dataset containing two categories: "Kirmizi_Pistachio" and "Siirt_Pistachio". From initial exploration to predictive modeling, the guide covers a range of machine learning techniques.

## 🧐 Initial Exploration and Visualization
The dataset comprises:
- 1,232 images in the "Kirmizi_Pistachio" category.
- 916 images in the "Siirt_Pistachio" category.
All images are of consistent 600x600 pixel dimensions.

## 🛠️ Feature Extraction with Pre-trained Models
We use the VGG16 model, pre-trained on ImageNet, to extract features from the images, converting high-dimensional image data into a format suitable for clustering and modeling.

## 📊 Clustering with KMeans
Group similar images using the KMeans clustering algorithm.

## 🚫 Anomaly Detection
The Isolation Forest algorithm helps identify and potentially remove outliers or unusual images in the dataset.

## 🤖 Building Models with H2O's AutoML
AutoML platforms simplify the process of model selection and hyperparameter tuning. The H2O platform is employed for this purpose, automatically selecting the best algorithm and optimizing its parameters for the task at hand.

## 💡 Conclusion
Through a systematic approach, we've created a pipeline to handle image datasets efficiently. This pipeline can be adapted for various datasets and can serve as a foundation for more advanced tasks.

