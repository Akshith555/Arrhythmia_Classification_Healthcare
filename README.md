# 🫀 Arrhythmia Classification in Healthcare

Welcome to **Arrhythmia Classification in Healthcare** – a complete machine learning pipeline to detect and classify arrhythmias from real clinical data.

## 🚀 Project Overview

This project demonstrates the use of modern machine learning for predicting and classifying cardiac arrhythmias in healthcare.

* **Clinical dataset** (UCI Arrhythmia)
* **Data cleaning, outlier removal, feature selection**
* **Supervised learning models:** KNN, Logistic Regression, SVM, Decision Tree, Random Forest, Kernelized SVM
* **Class imbalance solutions:** SMOTE and class weighting
* **Dimensionality reduction:** PCA
* **Clear results/visualizations:** Confusion matrices, bar charts (with/without PCA), model comparison

**Goals:**
* Support early and accurate diagnosis of cardiac risk
* Show practical ML steps: cleaning, feature engineering, cross-validation, and model evaluation
* Highlight how recall/sensitivity is prioritized for real healthcare

---

## 🗂️ Project Structure

```
├── data/
│   ├── arrhythmia.csv                   # Raw dataset
│   └── processed_arrhythmia.csv         # Dataset description
│
├── notebooks/
│   ├── 01_eda_preprocessing.ipynb
│   └── 02_modeling.ipynb                # Combined baseline + PCA modeling
│
├── Arrhythmia_ML_Project.pptx
├── requirements.txt                     # Project dependencies
├── README.md                            # Project overview and instructions
└── .gitignore                           # Files to ignore in version control
```

---

## 📊 The Dataset

- **Source:** [UCI Arrhythmia Dataset](https://archive.ics.uci.edu/ml/datasets/arrhythmia)
- **Full Dataset:** 452 patient records × 279 features (+ 1 target class)
- **Features:**  
  - **Demographics:** Age, Sex, Height, Weight  
  - **ECG Measurements:** 200+ time-series derived attributes  
  - **Clinical Info:** 20+ patient medical and risk indicators  
  - **Target:** Multi-class label (1–16), representing arrhythmia types
---

## 🧠 How It Works

### 1. Data Cleaning & EDA

* Outlier detection, missing value imputation
* Feature selection with correlation
* Save processed dataset for reproducibility

### 2. Baseline Modeling (No PCA)

* KNN, Logistic Regression, Decision Tree, Random Forest, Linear SVM, Kernelized SVM
* Stratified train/test split
* Class weighting (`class_weight='balanced'`) for imbalanced classes

### 3. Modeling With PCA

* PCA for dimensionality reduction (retain 98% variance)
* Retrain all models using PCA features

### 4. Class Imbalance Handling

* **SMOTE**: Tested for minority class oversampling (not final choice)
* **Class weighting**: Used in all main models

### 5. Cross-Validation & Evaluation

* 5-fold stratified cross-validation
* Metrics: Accuracy, recall, F1-score, confusion matrix

### 6. Visualization

* Compare all models side-by-side (with/without PCA)
* Professional bar charts, annotated confusion matrices

---

## 💾 Files Used

* `processed_arrhythmia.csv` – Cleaned data
* `/models/*.pkl` – Trained models
* `Arrhythmia_ML_Project.pptx` – Full analysis and presentation



````markdown
## 🛠️ How to Run Locally

1. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
````

2. **Open the Notebooks**

   * `notebooks/01_eda_preprocessing.ipynb` (data cleaning & EDA)
   * `notebooks/02_modeling.ipynb` 

3. **See All Results**

   * Open `Arrhythmia_ML_Project.pptx` for results, explanations, and model comparison


---
## Key Highlights & Innovations

- **Clinical Focus:** Designed to minimize false negatives—crucial for medical risk prediction.
- **Robust Preprocessing:** Outlier handling, missing value imputation, and class balancing for real-world healthcare data.
- **Model Comparisons:** Rigorous benchmarking with and without PCA across multiple classifiers (SVM, Random Forest, etc.).
- **Interpretable Results:** Feature importance, confusion matrices, and rich visualizations to support clinical understanding.
- **Fully Reproducible:** Step-by-step notebooks and saved models enable reproducibility and easy extension.

---

## Future Work

- Integrate raw ECG signal processing for even richer features.
- Try advanced ensemble and deep learning approaches (e.g., XGBoost, CNN for signals).
- Deploy as a clinical decision support web tool for easy use by healthcare professionals.
- Optimize for recall and ROC-AUC using clinical cost-based metrics.
- Expand to larger, multi-center arrhythmia datasets.

---


## ❓ Questions?

Open an issue or connect on [LinkedIn](https://www.linkedin.com/in/akshith-goud/)!

---


