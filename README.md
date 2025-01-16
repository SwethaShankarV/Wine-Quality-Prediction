# Wine Quality Prediction Using Machine Learning

This repository contains a project focused on predicting wine quality based on physicochemical properties using various machine learning techniques. The project explores **Supervised Learning (SL)**, **Semi-Supervised Learning (SSL)**, and **Unsupervised Learning (USL)** approaches to classify wine into three quality categories: low, medium, and high.

## Table of Contents

1. [Introduction](#introduction)
2. [Dataset](#dataset)
3. [Preprocessing](#preprocessing)
4. [Models Used](#models-used)
   - [Supervised Learning (SL)](#supervised-learning-sl)
   - [Semi-Supervised Learning (SSL)](#semi-supervised-learning-ssl)
   - [Unsupervised Learning (USL)](#unsupervised-learning-usl)
5. [Results](#results)
6. [Future Work](#future-work)
7. [Contributors](#contributors)

## Introduction

This project classifies wine quality into three categories—low, medium, and high—using the **UCI Wine Quality Dataset**. The dataset includes physicochemical properties of wines such as alcohol content, volatile acidity, and pH levels. We implemented different machine learning algorithms and compared their performance to predict wine quality.

The project was implemented using Python and the following libraries:
- **scikit-learn**: For machine learning models
- **matplotlib**, **seaborn**: For visualization
- **pandas**: For data manipulation

## Dataset

The dataset used in this project is the **Wine Quality Dataset** from the UCI Machine Learning Repository. It contains red and white wine samples with the following features:

- Fixed acidity
- Volatile acidity
- Citric acid
- Residual sugar
- Chlorides
- Free sulfur dioxide
- Total sulfur dioxide
- Density
- pH
- Sulphates
- Alcohol content
- Quality label (target: low, medium, high)

### Dataset Information:
- **Number of data points**: 6497
- **Features**: 12
- **Classes**: 3 (low, medium, high)

## Preprocessing

The dataset was preprocessed with the following steps:
1. **Data cleaning**: Removal of duplicates and missing values.
2. **Feature scaling**: Standardization of features to have zero mean and unit variance using `StandardScaler`.
3. **Handling class imbalance**: Resampling using **SMOTE** (Synthetic Minority Over-sampling Technique).
4. **Dimensionality reduction**: PCA was applied for visualization and clustering.

## Models Used

### Supervised Learning (SL)
- **Decision Trees (CART)**: A simple, interpretable model used for baseline comparison.
- **Random Forest**: An ensemble method that reduces overfitting and captures non-linear relationships.
- **Random Forest with AdaBoost**: Combines Random Forest with AdaBoost to enhance generalization.

### Semi-Supervised Learning (SSL)
- **Self-Training Random Forest**: A semi-supervised method that iteratively uses pseudo-labels to enhance model performance.
- **S3VM (Semi-Supervised SVM)**: An extension of SVM for semi-supervised learning, optimizing on both labeled and unlabeled data.

### Unsupervised Learning (USL)
- **K-Means Clustering**: Used to cluster the data based on similarity, with the number of clusters determined using the elbow method.
- **Gaussian Mixture Models (GMM)**: A probabilistic clustering approach that handles overlapping data distributions.
- **Hierarchical Clustering**: Provides a dendrogram for understanding the relationships between clusters.

## Results

- **Best Performing Model**: Random Forest (Supervised Learning) achieved an accuracy of **69.92%** and an F1-score of **73.14%**.
- **SSL**: The Self-Training Random Forest model achieved **67.86%** accuracy with balanced data at 90% labeled samples.
- **USL**: K-Means performed best with a **Silhouette Score of 0.4943**, reflecting well-separated clusters for low and high-quality wines.

## Future Work

- **Ensemble Clustering**: Combine multiple clustering techniques for improved performance.
- **Density-Based Clustering**: Experiment with algorithms like **DBSCAN** to address the overlapping medium category.
- **Feature Engineering**: Investigate additional feature engineering methods to improve model accuracy.

## Contributors

- **Aaryan Siddharthan** - asiddhar@usc.edu
- **Swetha Shankar** - swethash@usc.edu

---

