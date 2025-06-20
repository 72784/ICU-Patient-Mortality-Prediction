# ICU Mortality Prediction Using Real-World Clinical Data

This project explores the development of machine learning models to predict patient mortality in Intensive Care Units (ICUs) using real-world clinical datasets. The models are trained and validated on the MIMIC-III and eICU Collaborative Research databases to ensure cross-dataset generalization and real-world applicability.

---

## Objective

To build interpretable, generalizable, and high-performing models capable of identifying high-risk ICU patients using structured clinical features such as vital signs, lab values, and comorbidities.

---

## Models Used

- XGBoost for gradient-boosted decision trees  
- Neural Network (PyTorch) for deep learning-based binary classification

---

## Datasets

- [MIMIC-III](https://physionet.org/content/mimiciii/1.4/)
- [eICU Collaborative Research Database](https://eicu-crd.mit.edu/)

Access to these datasets requires credentialed approval from PhysioNet.

---

## Methodology

- Feature engineering from vital signs, lab tests, demographics, and comorbidities
- Imputation using `SimpleImputer` (mean strategy)
- Feature scaling with `StandardScaler`
- Class imbalance handled via SMOTE
- Patient-level train-test split to avoid data leakage
- Cross-dataset validation (train on MIMIC-III, test on eICU and vice versa)

---

## Performance Summary

| Model        | AUC-ROC | Recall  |
|--------------|---------|---------|
| XGBoost      | 0.771   | 55.3%   |
| Neural Net   | 0.758   | 64.8%   |

---

## Project Structure

.
├── data/ # Preprocessed data files (not uploaded)
├── models/ # Trained models (saved weights)
├── src/ # Scripts for training and evaluation
│ ├── train_xgboost.py
│ ├── train_nn.py
│ └── evaluate.py
├── requirements.txt # Python dependencies
└── README.md



## Key Features

- Cross-hospital validation across **MIMIC-III** and **eICU** datasets  
- Robust pipeline with clean preprocessing, feature engineering, and model training steps  
- Demonstrates strong generalization in real-world ICU mortality prediction tasks  
- Modular, well-documented, and reproducible codebase for easy experimentation and extension



