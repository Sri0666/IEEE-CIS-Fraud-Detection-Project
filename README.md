# IEEE-CIS Fraud Detection Project

This project focuses on detecting fraudulent online transactions using the IEEE-CIS Fraud Detection dataset from Kaggle. We explore both classical machine learning and deep learning approaches, with additional work on adversarial robustness and performance optimisation under extreme class imbalance.

## Objective

The goal of this project is to build robust models that can accurately detect fraudulent transactions (`isFraud = 1`) while handling:
- Highly imbalanced data
- Missing and noisy features
- Real-world transaction variability
- Robustness under adversarial attacks

---

## Dataset

We use the **IEEE-CIS Fraud Detection dataset**, which contains:

- Transaction data (`train_transaction`)
- Identity data (`train_identity`)

Both datasets are merged using `TransactionID` to form a unified feature space.

---

## Models

### Machine Learning Models
- Logistic Regression
- Random Forest
- XGBoost

### Deep Learning Models
- Fully connected neural networks (Model 1–3)
- Final optimised PyTorch model (`Final_model.ipynb`)
- Model weights saved as `.pt` files in `Model_outputs/`

---

## Preprocessing

Key steps include:

- Merging identity and transaction tables
- Handling missing values
- Encoding categorical variables
- Feature scaling and transformation
- Train/validation splitting to avoid leakage

---

## Adversarial Robustness

We evaluate model robustness using:

- Iterative Fast Gradient Sign Method (I-FGSM)
- Adversarial perturbations applied to input features
- Analysis of performance degradation under attack

This tests whether the model remains stable under small but malicious input changes.

---

## How to Run

1. Extract dataset files in the `Data/` folder
2. Run preprocessing:
