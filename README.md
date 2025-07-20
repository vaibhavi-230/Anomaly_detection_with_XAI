# Anomaly_detection_with_XAI
# Anomaly Detection in Bitcoin Blockchain Transactions with Advanced ML and Explainable AI

This project focuses on building a robust system to detect anomalous (potentially fraudulent) transactions in Bitcoin using advanced Machine Learning (ML) techniques and Explainable AI (XAI). Addressing a highly imbalanced dataset (30M+ transactions, only 108 anomalies), the project integrates custom sampling, ensemble modeling, and SHAP-based interpretation for model transparency and real-time deployment.

## Key Features & Methodology
#### Handling Class Imbalance:
Implemented 7 sampling techniques including Random Undersampling (RUS), NearMiss, SMOTE, ADASYN, SMOTENN, SMOTETomek, and a custom clustering-based undersampling technique—XGBCLUS—which showed superior performance in improving true positive rates.

#### Model Development:
Trained and compared 4 tree-based classifiers:

Decision Tree

Random Forest

Gradient Boosting

AdaBoost

#### Evaluated 3 ensemble methods:

Stacking (with Logistic Regression as meta-model)

Hard Voting

Soft Voting


In total, 49 model–sampling combinations were tested to identify the optimal pipeline for anomaly detection.

#### Explainable AI (XAI):
Used SHAP (SHapley Additive Explanations) for both global and local interpretability.

Bar plots of mean absolute SHAP values revealed key features driving predictions.

Force plots explained individual transaction classifications and helped interpret model decisions transparently.

Derived interpretable decision rules from trained models for actionable insights.

#### Deployment
Deployed the best-performing stacked ensemble model (trained on XGBCLUS-sampled data) using Google Colab for real-time fraud detection.
Also prepared the pipeline for Docker containerization, enabling portability and future third-party use.

### Technologies Used
Programming Language: Python

Libraries: NumPy, pandas, scikit-learn, imbalanced-learn, matplotlib, seaborn, SHAP

Sampling Techniques: SMOTE, ADASYN, SMOTENN, SMOTETomek, XGBCLUS

Machine Learning Models: Decision Tree, Random Forest, Gradient Boosting, AdaBoost, Stacking Classifier

Explainability: SHAP (bar plots, force plots)

Deployment Tools: Google Colab
