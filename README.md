# Fraud Detection using Random Forest Classifier

This repository contains a Python-based fraud detection system using machine learning. The project primarily uses a **Random Forest Classifier** to classify credit card transactions as fraudulent or not. The dataset used for this project contains real-world anonymized credit card transaction data.

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Model Improvements](#model-improvements)
  - [Handling Class Imbalance](#handling-class-imbalance)
  - [Hyperparameter Tuning](#hyperparameter-tuning)
  - [Feature Selection](#feature-selection)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

This project develops a fraud detection model using a **Random Forest Classifier**. It involves:

1. Data preprocessing.
2. Addressing class imbalance with techniques like **undersampling** and **SMOTE**.
3. Model training and evaluation.
4. Exploring advanced techniques such as **XGBoost** and **hyperparameter tuning** to improve model performance.

---

## Features

- **Random Forest Classifier** for baseline fraud detection.
- **Class imbalance handling** with undersampling and SMOTE.
- **Evaluation metrics**: Accuracy, Precision, Recall, and Classification Report.
- **Hyperparameter Tuning** using GridSearchCV.
- **Feature Importance** visualization.

---

## Dataset

The dataset used is a publicly available **credit card fraud detection dataset** containing anonymized transaction data. The target column `Class` indicates whether a transaction is fraudulent (`1`) or not (`0`).

### Dataset Highlights

- Highly imbalanced (fraudulent transactions make up a small percentage).
- Includes numerical features obtained through PCA transformation.
- Link to dataset: [Kaggle - Credit Card Fraud Detection](https://www.kaggle.com/mlg-ulb/creditcardfraud)

---

## Installation

### Prerequisites

Ensure you have Python installed. Required libraries include:

- **pandas**
- **scikit-learn**
- **imbalanced-learn**
- **xgboost**
- **matplotlib**

Install dependencies with pip:

```bash
pip install pandas scikit-learn imbalanced-learn xgboost matplotlib
```

---

## Usage

### Steps to Run the Project

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/fraud-detection.git
   cd fraud-detection
   ```
2. Place the dataset (`creditcard.csv`) in the project directory.
3. Run the script:
   ```bash
   python fraud_detection.py
   ```

### Prediction Function

A sample function is included to predict whether a single transaction is fraudulent. Modify and test with:

```python
# Example usage
sample_transaction = X_test.iloc[0].values
print(predict_transaction(sample_transaction))
```

---

## Model Improvements

### Handling Class Imbalance

- **Undersampling**: Reduce the majority class size to balance the dataset.
- **SMOTE**: Use Synthetic Minority Oversampling Technique to create synthetic samples for the minority class.

### Hyperparameter Tuning

Use GridSearchCV to find optimal hyperparameters for the Random Forest Classifier. This improves performance metrics like precision and recall.

### Feature Selection

Visualize feature importance using the Random Forest Classifier to identify significant predictors for fraud detection.

---

## Results

- **Baseline Model**: Random Forest Classifier with default parameters.
  - Accuracy: ~99%
  - Precision: High for minority class (fraudulent transactions).
  - Recall: Moderate to high depending on threshold.

- **Improvements**: Using SMOTE and hyperparameter tuning resulted in better recall and overall balanced performance.

---

## Contributing

Contributions are welcome! If you have suggestions or improvements, please create an issue or submit a pull request.

1. Fork the repository.
2. Create a new branch for your feature.
3. Commit your changes.
4. Submit a pull request.

---

## License

This project is licensed under the MIT License. See the LICENSE file for details.
