# Credit Card Fraud Detection

## Overview

This project aims to detect fraudulent credit card transactions using machine learning techniques. The dataset used for this project is from real-world credit card transactions, and it consists of anonymized features to predict whether a transaction is legitimate or fraudulent. The goal is to develop a model that can accurately classify transactions into two categories: **fraudulent** and **non-fraudulent**.

## Dataset

The dataset used for this project contains the following columns:
Here is the link to the dataset https://drive.google.com/file/d/1inQ5W1KDS1v1w6dBd-znRoA67O6ZvD1B/view?usp=drive_link

- **Time**: Time elapsed between this transaction and the first transaction in the dataset.
- **V1, V2, V3, ..., V28**: Anonymized features related to the transaction (you can consider these as transformed features of the original data).
- **Amount**: The transaction amount.
- **Class**: The target variable where:
  - **0** indicates a legitimate transaction.
  - **1** indicates a fraudulent transaction.

The dataset is highly imbalanced, with fraudulent transactions representing a small percentage of the total dataset.

## Installation

To run this project on your local machine, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/Ivykogo/Credit-card-fraud-detection.git
   cd Credit-card-fraud-detection
   pip install -r requirements.txt
   ```

   ## Project Workflow

### 1. **Data Preprocessing**
   - **Loading the Dataset**: The dataset is loaded into a pandas DataFrame.
   - **Handling Missing Values**: Missing or NaN values are handled appropriately.
   - **Feature Scaling**: The features are scaled using Min-Max scaling to improve model performance.
   - **Train-Test Split**: The dataset is split into training and testing sets to evaluate the model's performance.

### 2. **Model Training**
   - **Logistic Regression** is used for classification due to its effectiveness in binary classification problems.
   - **Hyperparameter Tuning**: The model is tuned using GridSearchCV to find the best hyperparameters for optimal performance.

### 3. **Model Evaluation**
   - The model's performance is evaluated using:
     - **Accuracy**
     - **Precision**
     - **Recall**
     - **F1-Score**
     - **ROC-AUC** (Receiver Operating Characteristic - Area Under Curve)
   - A confusion matrix and other classification metrics are used to measure how well the model distinguishes between legitimate and fraudulent transactions.

### 4. **Model Optimization**
   - The model is further optimized based on evaluation metrics. Techniques such as adjusting regularization strength (`C` parameter) are applied to improve performance.

### 5. **Final Predictions**
   - Once the model is trained and tuned, it is ready for making predictions on new or unseen data.

  

