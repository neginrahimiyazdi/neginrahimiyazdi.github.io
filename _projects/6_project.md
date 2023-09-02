---
layout: page
title: Enhancing Breast Cancer Prediction using MLP
description:
img:
importance: 6
category: 
---

In this project, I applied machine learning techniques to classify breast cancer cells as either benign or malignant based on a dataset containing characteristics of cell nuclei observed in images of breast mass tissue. The primary goal was to develop a predictive model to aid in the early detection of breast cancer.

**Key Steps**:

**Data Split**: I divided the dataset into an 80% training set and a 20% testing set to train and evaluate the model's performance.

**Data Preprocessing**: I performed data preprocessing tasks such as normalization and handling missing values to ensure the data was suitable for training. Feature selection was also carried out using correlation matrix analysis and Random Forest feature importances.

**Model Architecture**: I designed a Multi-Layer Perceptron (MLP) model with carefully chosen hyperparameters, including the number of layers, nodes per layer, and activation functions. The model was trained for an appropriate number of epochs on the training data, and a validation split was used to prevent overfitting.

**Evaluation**: To assess the model's performance, I evaluated it on the test data using various metrics such as the confusion matrix, precision, recall, and F1-score. These metrics were computed using the scikit-learn library.

**Baseline Comparison**: As a point of reference, I also trained an MLP model on the MNIST dataset to compare the performance of the breast cancer classification model against a commonly used benchmark.

For more details and to explore the code repository, please visit [GitHub Repository](https://github.com/neginrahimiyazdi/Breast-Cancer-Prediction-using-MLP).
