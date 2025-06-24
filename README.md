# 🫀 Arrhythmia Classification in Healthcare

Welcome to **Arrhythmia Classification in Healthcare** – a complete machine learning pipeline to detect and classify arrhythmias from real clinical data.

<p align="center">
  <img src="assets/arrhythmia_ppt_screenshot.png" alt="Arrhythmia Project Screenshot" width="700"/>
</p>

---

## 🚀 Project Overview

This project demonstrates the use of modern machine learning for predicting and classifying cardiac arrhythmias in healthcare.

* **Clinical dataset** (UCI Arrhythmia)
* **Data cleaning, outlier removal, feature selection**
* **Supervised learning models:** KNN, Logistic Regression, SVM, Decision Tree, Random Forest, Kernelized SVM
* **Dimensionality reduction:** PCA
* **Clear results/visualizations:** Confusion matrices, bar charts (with/without PCA), model comparison

**Goals:**
* Support early and accurate diagnosis of cardiac risk
* Show practical ML steps: cleaning, feature engineering, cross-validation, and model evaluation
* Highlight how recall/sensitivity is prioritized for real healthcare

---

## 🗂️ Project Structure

Arrhythmia_Classification_Healthcare/
│
├── data/
│ └── processed_arrhythmia.csv
│
├── models/
│ ├── knn_classifier.pkl
│ ├── logistic_regression.pkl
│ └── ... (other models)
│
├── notebooks/
│ ├── 01_eda_preprocessing.ipynb
│ ├── 02_modeling.ipynb
│
├── Arrhythmia_ML_Project.pptx
├── requirements.txt
└── README.md


---

## 📊 The Dataset

* **Source:** [UCI Arrhythmia Dataset](https://archive.ics.uci.edu/ml/datasets/arrhythmia)
* **452 samples × 279 features** (ECG, demographics, clinical info)
* **Target:** Multi-class arrhythmia type

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

---

## 💾 Files Used

* `processed_arrhythmia.csv` – Cleaned data
* `/models/*.pkl` – Trained models
* `Classification_of_Arrhythmia.pptx` – Full analysis and presentation



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

   * Open `Classification_of_Arrhythmia.pptx` for results, explanations, and model comparison

---

## 📝 Example Use Case

> *“Given a patient’s ECG data, predict arrhythmia type using a robust ML workflow and highlight clinical risk.”*

---

## 🔬 Key Innovations

* Handles real-world medical data issues: Outliers, missing data, class imbalance
* Compares models with and without dimensionality reduction
* Focuses on recall to minimize false negatives in a clinical context
* All code, results, and presentation are fully reproducible

---

## 📚 Acknowledgements

* **Dataset:** UCI Machine Learning Repository
* **Tech stack:** Python, scikit-learn, pandas, seaborn, matplotlib

---

## ❓ Questions?

Open an issue or connect on [LinkedIn](https://www.linkedin.com/in/akshith-goud/)!

---


