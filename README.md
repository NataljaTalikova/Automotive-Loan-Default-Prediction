# Automotive Loan Default Prediction — Binary Classification

The project utilizes data from the Indian Financial Data Science Hackathon 2019([Analytics Vidhya](#ref4), [Mishra, S.](#ref5), [Bhavsar, N., 2019](#ref6)), where 470 teams competed, and the dataset has since been downloaded 1,960 times on Kaggle, resulting in seven published projects. The hackathon's AUC-ROC evaluation method recorded a leader's result of 0.67317. Given that a few years have passed since 2019, this project aims to explore advancements that could improve predictions. As a first-time endeavor in Financial Data Science, the primary objective is to gain experience with Data Science tools and techniques while leveraging clean and well-researched data.

The goal is to learn and optimize three classifying algorithms at an intermediate level: Logistic Regression, Support Vector Machine, and the recently popularized GXBoost, which is known for its exceptional performance([Bentéjac, C., Csörgő, A. and Martínez-Muñoz, G., 2021](#ref7)). The project will compare results using the competition's metrics. While Logistic Regression and Support Vector Machines will not be explained in detail, a brief overview of GXBoost will be provided. GXBoost is a scalable ensemble technique based on gradient boosting that has proven to be a dependable and efficient machine learning challenge solver([Rao, C., Liu, Y. and Goh, M., 2022](#ref8)).

---

## Problem Framing

- **Objective:** Predict loan default (binary outcome)
- **Business context:** Credit risk assessment, where false negatives (missed defaults) are costly
- **Challenge:** Mixed data types, heavy class imbalance, noisy financial features

---

## Models Implemented

- **Logistic Regression** (baseline and regularised)
- **Support Vector Machine** (RBF / Polynomial kernels)
- **XGBoost** (gradient-boosted ensemble)

Logistic Regression and SVM are used as **diagnostic and comparative baselines**.  
**XGBoost is the primary model**, reflecting its emergence as a high-performing algorithm in tabular credit-risk problems after the original hackathon period. 

Hyperparameter tuning notebooks (Optuna + XGBoost) are kept in the `Experiments-Folding,-Feature-Target-Hyst,-Lasso-Regression-with-Search-Grid` branch.
---

## Methodology Highlights

- Feature engineering for mixed numerical and categorical data
- Outlier analysis and selective trimming
- Standard scaling for linear and kernel-based models
- **SMOTE-based oversampling** to address class imbalance
- Threshold tuning with emphasis on **recall**
- Evaluation on a held-out test set using:
  - AUC-ROC
  - Recall
  - F1-score
  - Balanced accuracy

---

## Key Results

- **XGBoost achieves AUC-ROC ≈ 0.80**
- Substantial performance improvement relative to linear and kernel-based baselines
- Feature importance analysis confirms the relevance of engineered variables

---

## Repository Contents

- Jupyter notebooks covering:
  - EDA and feature engineering
  - Model training and tuning
  - Comparative evaluation
- Project report (PDF)
- Presentation slides
- Supporting plots (ROC curves, feature importance, class distribution)

---

## Data Source

- **Analytics Vidhya — LTFS Data Science FinHack (2019)**
- Publicly available dataset used for educational and benchmarking purposes

---

## Author

**Natalja Talikova**, 2023  
MSc Quantitative Finance with Data Science (Merit)  
University of London (Birkbeck)

---

## License

MIT License

