## 📘 Project Title: Pistachio Variety Classification Using Machine Learning

### 📌 Overview

This project involves building a machine learning model to classify pistachio varieties based on several physical and morphological features. The goal is to help in the automatic identification of pistachio types, which can be beneficial in agricultural and commercial applications.

---

### 🧐 Problem Statement

Manual classification of pistachio types is time-consuming and error-prone. Automating this process using machine learning models can improve accuracy and efficiency in sorting and quality control.

---

### 📊 Dataset

* **Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/)
* **Features Used:**

  * AREA
  * PERIMETER
  * MAJOR\_AXIS
  * MINOR\_AXIS
  * ECCENTRICITY
  * CONVEX\_AREA
  * EXTENT
  * COMPACTNESS
  * CLASS\_LABEL

---

### ⚙️ Algorithms Used

#### 1. **Logistic Regression**

* **Purpose:** Baseline model for binary classification.
* **Strengths:** Simple, interpretable, works well with linearly separable data.
* **Performance:** Achieved 86% train accuracy and 88% test accuracy with 94% ROC-AUC.

#### 2. **K-Nearest Neighbors (KNN)**

* **Purpose:** Distance-based classifier that considers the `k` closest points.
* **Strengths:** Non-parametric, works well on small datasets.
* **Limitations:** Sensitive to noisy data, slower on large datasets.
* **Performance:** 80% train accuracy, around 85% test accuracy.

#### 3. **Support Vector Machine (SVM)**

* **Purpose:** Constructs a hyperplane for maximum margin separation.
* **Strengths:** Effective in high-dimensional space, works well with clear margins.
* **Performance:** Achieved around 83% train and 85–87% test accuracy.

#### 4. **Decision Tree**

* **Purpose:** A simple tree-based model for classification.
* **Strengths:** Easy to interpret, fast, handles both numerical and categorical data.
* **Performance:** Good accuracy but prone to overfitting.

#### 5. **Random Forest (RF)**

* **Purpose:** Ensemble method based on decision trees.
* **Strengths:** Handles overfitting well, robust to outliers.
* **Performance:** 88% train accuracy, 89% test accuracy, 92% ROC-AUC.

#### 6. **Gradient Boosting**

* **Purpose:** Builds models sequentially to minimize error.
* **Strengths:** High accuracy, handles complex data patterns well.
* **Performance:** Very good performance, close to AdaBoost.

#### 7. **XGBoost**

* **Purpose:** Optimized implementation of gradient boosting.
* **Strengths:** Regularization, speed, and scalability.
* **Performance:** Competitive results, among the top-performing models.

#### 8. **AdaBoost (Adaptive Boosting)**

* **Purpose:** Combines multiple weak learners into a strong classifier.
* **Strengths:** Focuses on hard-to-classify examples, improves accuracy iteratively.
* **Performance:** **Best overall performance** with 90%+ accuracy and high ROC-AUC. Selected as the final model.

---

### 🧹 Data Preprocessing

* Handled missing values (if any)
* Normalized numerical features using standard scaler
* Encoded class labels
* Outlier removal using IQR method

---

### 🧪 Model Training & Evaluation

| Model               | Train Accuracy | Test Accuracy | ROC-AUC   |
| ------------------- | -------------- | ------------- | --------- |
| Logistic Regression | 86%            | 88%           | 94%       |
| KNN                 | 80%            | \~85%         | 83%        |
| SVM                 | 84%            | 85–87%        | 94%       |
| Decision Tree       | 85%            | 86%           | 90%      |
| Random Forest       | 91%            | 89%           | 92%       |
| Gradient Boosting   | 89%            | 88%           | 93%       |
| XGBoost             | 92%            | 88%           | 94%       |
| **AdaBoost**        | 89%+        | 89%           | 94%       |

> ✅ **AdaBoost** was selected for deployment due to its superior generalization and stability.

---

### 📈 Evaluation Metrics

* Confusion Matrix
* Accuracy, Precision, Recall, F1-Score
* ROC-AUC Curve
* Cross-validation

---

### 💻 Deployment

* Final model saved as `model.pkl`
* Flask web application built to allow users to input pistachio measurements and receive predictions.


### 📂 Project Structure

```
├── Project_Pistacho.ipynb
├── app.py
├── model.pkl
├── templates/
│   └── index.html
├── static/
│   └── style.css
├── README.md
└── requirements.txt
```
