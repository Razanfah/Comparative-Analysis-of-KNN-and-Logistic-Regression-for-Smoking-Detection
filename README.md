# Comparative-Analysis-of-KNN-and-Logistic-Regression-for-Smoking-Detection

## Table of Contents

1. [Introduction](#introduction)
2. [Project Overview](#project-overview)
3. [K-Nearest Neighbors (KNN)](#k-nearest-neighbors-knn)
   - [Implementation Steps](#implementation-steps)
   - [Performance Metrics](#performance-metrics)
4. [Logistic Regression](#logistic-regression)
   - [Implementation Steps](#implementation-steps-1)
   - [Key Analysis](#key-analysis)
   - [Performance Metrics](#performance-metrics-1)
5. [Comparison of KNN and Logistic Regression](#comparison-of-knn-and-logistic-regression)
6. [Conclusion](#conclusion)

   
## Introduction

This project analyzes the "Body Signal of Smoking" dataset from Kaggle, focusing on classifying smoking status based on physiological signals. We compare the performance of two popular machine learning algorithms:

- **K-Nearest Neighbors (KNN)**
- **Logistic Regression**

By evaluating their accuracy, precision, and recall, we aim to determine which algorithm is more effective for this classification task, ultimately contributing to enhanced methods for smoking detection and health monitoring.

## Project Overview

The analysis begins with K-Nearest Neighbors (KNN), where we preprocess the data, implement the algorithm, and evaluate its performance. We then shift to Logistic Regression, following similar steps to compare the results.

## K-Nearest Neighbors (KNN)

### Implementation Steps

1. **Check for Missing Values**: Assess the dataset for NaN values.
2. **Data Preprocessing**: Convert categorical data into dummy variables.
3. **Model Training**: Train the KNN model with optimal parameters.

### Performance Metrics

- **Best k**: 89 neighbors
- **Cross-Validation Accuracy**: 73.64%
- **Confusion Matrix**:
  - True Non-Smokers (class 0): 510
  - False Non-Smokers: 175
  - True Smokers (class 1): 276
  - False Smokers: 139
- **Precision**:
  - Non-Smokers: 0.79
  - Smokers: 0.61
- **Recall**:
  - Non-Smokers: 0.74
  - Smokers: 0.67
- **Overall Accuracy**: 71%

## Logistic Regression

### Implementation Steps

1. **Data Preprocessing**: Convert categorical data into dummy variables.
2. **Model Training**: Train the KNN model with optimal parameters.
3. **Performance Evaluation**: Assess accuracy, precision, and recall.

### Key Analysis

- **Feature Selection**: The `height(cm)` feature was identified as a significant predictor.
- **Threshold Verification**: Evaluated the height values to determine the tipping point for classification.

### Performance Metrics

- **Cross-Validation Accuracy**: 74.70%
- **Confusion Matrix**:
  - True Non-Smokers: 534
  - False Non-Smokers: 151
  - True Smokers: 284
  - False Smokers: 131
- **Precision**:
  - Non-Smokers: 0.80
  - Smokers: 0.65
- **Recall**:
  - Non-Smokers: 0.78
  - Smokers: 0.68
- **Overall Accuracy**: 74%

## Comparison of KNN and Logistic Regression

| Metric                          | K-Nearest Neighbors (KNN) | Logistic Regression |
|---------------------------------|----------------------------|---------------------|
| Best k                          | 89                         | None                |
| Cross-Validation Accuracy       | 73.64%                     | 74.70%              |
| Confusion Matrix                | [[510, 175]               | [[534, 151]        |
|                                 | [139, 276]]               | [131, 284]]        |
| Precision (Non-smokers)        | 0.79                       | 0.80                |
| Precision (Smokers)            | 0.61                       | 0.65                |
| Recall (Non-smokers)           | 0.74                       | 0.78                |
| Recall (Smokers)               | 0.67                       | 0.68                |
| Overall Accuracy                | 71%                        | 74%                 |

## Conclusion

In this analysis, Logistic Regression demonstrates a slight edge over KNN across most metrics, particularly in overall accuracy and precision for both non-smokers and smokers. While KNN shows competitive recall for smokers, the performance of Logistic Regression remains superior overall. This suggests that for this dataset, Logistic Regression may be the preferred model for predicting outcomes related to smoking status.
