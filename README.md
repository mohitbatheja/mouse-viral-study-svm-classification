# Mouse Viral Study - Support Vector Machine (SVM) Classification

A machine learning project implementing a **Support Vector Machine (SVM)** classifier using `scikit-learn` to predict virus presence based on medication dosages.

---

## 📌 Project Overview

This project analyzes the `mouse_viral_study.csv` dataset containing 400 experimental samples. The goal is to classify whether a virus is present (`Virus Present`) based on two feature measurements: `Med_1_mL` and `Med_2_mL`.

---

## 📊 Dataset Information

* **Total Samples:** 400


* **Features:**
* `Med_1_mL` (*float64*): Dosage of Medication 1


* `Med_2_mL` (*float64*): Dosage of Medication 2




* **Target:**
* `Virus Present` (*int64*): Binary class (`0` = Absence, `1` = Presence)




* **Missing Values:** None (0 null values across all columns)



---

## 🛠️ Tech Stack & Dependencies

* **Python** (3.x)


* **Pandas** — Data loading and manipulation


* **Scikit-Learn** — Preprocessing, modeling, and evaluation


---

## 🚀 Workflow & Implementation

1. **Data Loading & Preprocessing:**
* Loaded `mouse_viral_study.csv` via Pandas.


* Split data into features (`X`) and target (`y`).


* Applied `train_test_split` (80% training set, 20% test set with `random_state=42`).


* Standardized feature scales using `StandardScaler`.




2. **Model Training:**
* Trained a Support Vector Classifier (`SVC`) from `sklearn.svm` on scaled training data.




3. **Evaluation:**
* Evaluated model performance on the scaled test set using accuracy, precision, recall, F1-score, and confusion matrix.





---

## 📈 Model Performance & Results

The trained Support Vector Machine model achieved **100% accuracy** on the test set.

### 1. Classification Metrics

* **Accuracy:** `100.00%`

* **Test Set Size:** 80 samples (42 Class `0`, 38 Class `1`)



```text
               precision    recall  f1-score   support

           0       1.00      1.00      1.00        42
           1       1.00      1.00      1.00        38

    accuracy                           1.00        80
   macro avg       1.00      1.00      1.00        80
weighted avg       1.00      1.00      1.00        80

```

### 2. Confusion Matrix

```text
[[42  0]
 [ 0 38]]

```

* **True Positives / True Negatives:** 80


* **False Positives / False Negatives:** 0



---

## 💡 Conclusion

The Support Vector Classifier perfectly separated the two classes with zero misclassifications on the test set. Both classes achieved ideal scores across Precision, Recall, and F1-score.
