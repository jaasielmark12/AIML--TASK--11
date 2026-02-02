# AIML--TASK--11
SVM – Breast Cancer Classification
# Breast Cancer Classification using SVM (ROC & AUC Analysis)

##  Project Overview
This project implements a **Support Vector Machine (SVM)** based classification model to predict whether a breast tumor is **Malignant (M)** or **Benign (B)**.  
The workflow includes **data preprocessing, feature scaling, kernel comparison, hyperparameter tuning, evaluation using ROC–AUC**, and **model persistence**.

---

##  Dataset
- **Dataset:** Breast Cancer Wisconsin Dataset
- **Target Variable:** `diagnosis`
  - `M` → Malignant (1)
  - `B` → Benign (0)
- **Features:** Numerical measurements derived from tumor images

---

##  Libraries Used
- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Joblib

---

##  Workflow Steps

### 1️ Data Loading & Inspection
- Load dataset using Pandas
- Inspect feature columns and target label distribution
- Remove unnecessary columns such as ID

---

### 2️ Feature Scaling
- Applied **StandardScaler**
- Necessary for SVM as it is distance-based

---

### 3️ Train–Test Split
- Dataset split into **80% training** and **20% testing**
- Stratified split to preserve class balance

---

### 4️ Baseline Model (Linear SVM)
- Trained SVM using **linear kernel**
- Evaluated accuracy on test data

---

### 5️ Advanced Model (RBF Kernel)
- Trained SVM using **RBF kernel**
- Compared accuracy with linear SVM
- RBF kernel showed better performance

---

### 6️ Hyperparameter Tuning (GridSearchCV)
- Tuned parameters:
  - `C` (Regularization parameter)
  - `gamma` (Kernel coefficient)
- Used **5-fold cross-validation**
- Selected best performing model

---

### 7️ Model Evaluation
- **Confusion Matrix**
- **Classification Report**
  - Precision
  - Recall
  - F1-score
- Ensured balanced performance on both classes

---

##  ROC Curve & AUC Score

### ROC Curve
- Plots **True Positive Rate vs False Positive Rate**
- Demonstrates model performance at different thresholds

### AUC Score
- **AUC (Area Under Curve)** quantifies overall performance
- AUC value close to **1.0** indicates excellent classification ability

### Interpretation
- Tuned RBF SVM achieved **high AUC (> 0.95)**  
- Model is highly effective at distinguishing malignant and benign tumors

---

##  Model Saving & Reuse

### Saved Model File
- The final tuned pipeline (StandardScaler + SVM) is saved as:

