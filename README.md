Dynamic Ensemble Selection Project
Project Overview
This project implements a Dynamic Ensemble Selection (DES) approach for machine learning classification tasks. DES is an advanced ensemble learning technique that aims to select the most appropriate classifier or set of classifiers for each test instance, potentially improving overall prediction accuracy.

Methodology
Our DES implementation follows these key steps:

Base Model Creation: We use Repeated K-Fold cross-validation to train multiple base models, including:

Logistic Regression
Random Forest
XGBoost
LightGBM
CatBoost


Dynamic Selection: For each test sample:

We use K-Nearest Neighbors (KNN) to identify the most similar training samples.
Based on these similar samples, we employ various strategies to determine the best classifier(s) for the current test sample.


Classification Strategies: We implement multiple strategies for the final classification, including:

Weighted voting based on each model's performance on the similar training samples
Selecting the single best-performing model for the similar training samples



Key Features

Utilizes a diverse set of base models to capture different aspects of the data
Dynamically selects classifiers based on local competence
Implements various ensemble combination strategies
Leverages the strength of different models for different regions of the feature space

