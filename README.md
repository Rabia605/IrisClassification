# Iris Flower Classification 🌸

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white"/>
  <img src="https://img.shields.io/badge/XGBoost-EC4E20?style=for-the-badge&logo=xgboost&logoColor=white"/>
  <img src="https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white"/>
  <img src="https://img.shields.io/badge/Type-Classification-E74C3C?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Status-Complete-brightgreen?style=for-the-badge"/>
</p>

<p align="center">
  A multi-class classification project identifying Iris flower species  comparing <b>Logistic Regression, Random Forest, SVM & XGBoost</b> with full EDA, feature scaling, and model evaluation.
</p>

---

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Project Workflow](#project-workflow)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Models Used](#models-used)
- [Results](#results)
- [Tech Stack](#tech-stack)
- [How to Run](#how-to-run)
- [Project Structure](#project-structure)
- [Author](#author)

---

## Overview

This project applies **supervised multi-class classification** to the **Iris Dataset** from sklearn to identify flower species based on sepal and petal measurements. Four classification models are trained, evaluated, and compared using Accuracy, Precision, Recall, F1-Score, and ROC-AUC (One-vs-Rest).

---

**Features:**

| Feature | Description |
|:---|:---|
| sepal length (cm) | Length of the sepal |
| sepal width (cm) | Width of the sepal |
| petal length (cm) | Length of the petal |
| petal width (cm) | Width of the petal |
| target | 0 = Setosa, 1 = Versicolor, 2 = Virginica |

---

| Step | Description |
|:---:|:---|
| 1 | Load Iris dataset as DataFrame |
| 2 | Basic info, null & duplicate check |
| 3 | Found & removed 1 duplicate row (149 samples retained) |
| 4 | Target exploration — class distribution (pie chart + count plot) |
| 5 | Feature boxplots, histograms, correlation heatmap |
| 6 | Stratified 80/20 Train-Test Split (`random_state=42`) |
| 7 | StandardScaler applied to features |
| 8 | Four classification models trained |
| 9 | Evaluated on Accuracy, Macro F1, ROC-AUC (OvR) |
| 10 | Best model (SVM) retrained and evaluated with full report + confusion matrix + ROC curves |

---

## Exploratory Data Analysis

| Analysis | Method |
|:---|:---|
| Data Overview | `.head()`, `.describe()`, `.shape`, `.info()` |
| Null Check | `.isnull().sum()` |
| Duplicate Check | `.duplicated().sum()` — 1 duplicate found and removed |
| Target Distribution | Pie chart + Count plot |
| Feature Boxplots | Horizontal boxplot of all features |
| Feature Histograms | All features visualized |
| Feature Correlation | Heatmap (`seaborn`, `coolwarm` palette) |
| ROC Curves | One-vs-Rest ROC curves for final SVM model |

**Class Distribution (after deduplication):**

| Class | Count |
|:---|:---:|
| Setosa (0) | 50 |
| Versicolor (1) | 50 |
| Virginica (2) | 49 |

---

## Models Used

| Model | Library | Key Parameters |
|:---|:---|:---|
| Logistic Regression | `sklearn.linear_model` | `max_iter=1000, random_state=42` |
| Random Forest | `sklearn.ensemble` | `n_estimators=300, random_state=42` |
| SVM | `sklearn.svm` | `probability=True, random_state=42` |
| XGBoost | `xgboost` | `eval_metric="logloss", random_state=42` |

> Feature scaling applied using `StandardScaler` before model training. Stratified split used to preserve class balance.

---

## Results

| Model | Accuracy ↑ | Macro F1 ↑ | ROC AUC (OvR) ↑ |
|:---|:---:|:---:|:---:|
| **SVM**  | **96.67%** | **0.967** | **0.997** |
| Logistic Regression | 93.33% | 0.933 | 0.997 |
| XGBoost | 93.33% | 0.933 | 0.965 |
| Random Forest | 90.00% | 0.900 | 0.993 |

> ↑ Higher is better

**Best Model → SVM** — highest accuracy of 96.67% with perfect classification on Setosa and Virginica classes.

**Final SVM Confusion Matrix:**
```
[[10  0  0]
 [ 0  9  1]
 [ 0  0 10]]
```

---

## Tech Stack

| Tool | Purpose |
|:---|:---|
| Python | Core language |
| Pandas | Data manipulation |
| NumPy | Numerical operations |
| Matplotlib | Visualization |
| Seaborn | Statistical plots |
| Scikit-learn | ML models & evaluation |
| XGBoost | Gradient boosting classifier |
| Jupyter Notebook | Development environment |

---

## How to Run

**1. Clone the repository**
```bash
git clone https://github.com/Rabia605/IrisClassification.git
cd IrisClassification
```

**2. Install dependencies**
```bash
pip install -r requirements.txt
```

**3. Launch Jupyter Notebook**
```bash
jupyter notebook irisclassification.ipynb
```

**4. Run all cells**

`Kernel` → `Restart & Run All`

---

## Project Structure

```
IrisClassification/
│
├── irisclassification.ipynb
├── README.md
└── requirements.txt
```

---

## Author

**Rabia Noreen**
*Software Engineer | Building with AI & ML*

---

<p align="center">If this project inspired you, hit that ⭐ button!</p>
