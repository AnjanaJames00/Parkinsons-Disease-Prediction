# 🧠 Parkinson’s Disease Prediction using Ensemble Learning

## 📌 Overview

This project focuses on predicting Parkinson’s Disease using machine learning models trained on biomedical voice measurement data. The goal was not just to achieve high accuracy, but to perform a rigorous benchmarking study comparing multiple algorithms under identical experimental conditions.
Unlike many ML healthcare projects that report results from a single selected model, this project systematically evaluates multiple ensemble techniques to understand which model truly performs best for this dataset and why.

---

# 🎯 Objectives

* Detect Parkinson’s Disease using voice biomarkers
* Compare multiple machine learning models fairly
* Reduce overfitting and improve generalization
* Evaluate models using medical-grade metrics
* Understand how ensemble learning impacts healthcare prediction tasks

---

# 📂 Dataset

Dataset Used:

* Oxford Parkinson’s Disease Detection Dataset

The dataset contains biomedical voice measurements extracted from speech recordings.

### Key Features

* MDVP Jitter
* MDVP Shimmer
* HNR (Harmonics-to-Noise Ratio)
* RPDE
* DFA
* PPE
* Fundamental Frequency Features

### Target

* Parkinson’s Disease
* Healthy Control

---

# ⚙️ Project Pipeline

## 1️⃣ Data Preprocessing

### ✔ Missing Value Handling

Validated dataset quality and checked for null values.

### ✔ Feature Scaling

Applied `StandardScaler` to normalize feature ranges.

### ✔ Feature Selection

Used correlation analysis and statistical filtering to remove redundant features.

### ✔ Data Balancing

Handled class imbalance using oversampling techniques.

### ✔ Leakage Prevention

Ensured patient-level separation to avoid train-test contamination.

---

# 🧪 Models Compared

| Model               | Type               |
| ------------------- | ------------------ |
| Logistic Regression | Linear Baseline    |
| Random Forest       | Bagging Ensemble   |
| XGBoost             | Gradient Boosting  |
| LightGBM            | Leaf-wise Boosting |

---

# 🔬 Experimental Methodology

To ensure scientific fairness:

* Same preprocessing for all models
* Same train/test split
* Same cross-validation folds
* Same hyperparameter tuning effort
* Same evaluation metrics

This ensured that performance differences came only from the algorithms themselves.

---

# 📊 Evaluation Metrics

The following metrics were used:

* Accuracy
* Precision
* Recall
* F1 Score
* ROC-AUC
* Precision-Recall AUC

### Why Recall Matters

In medical diagnosis, false negatives are dangerous. Missing a Parkinson’s patient is far worse than generating a false alarm, making Recall an especially important metric.

---

# 🚀 Hyperparameter Tuning

## Random Forest

Optimized:

* Number of estimators
* Maximum depth
* Minimum samples split

## XGBoost

Optimized:

* Learning rate
* Max depth
* Subsampling
* Estimators

## LightGBM

Optimized:

* num_leaves
* learning rate
* max_depth
* regularization parameters

---

# 📈 Results

### Key Findings

* Ensemble models outperformed traditional models
* Boosting algorithms achieved the highest ROC-AUC
* Random Forest provided strong interpretability
* LightGBM offered the best speed-performance tradeoff

The project demonstrated how ensemble learning significantly improves robustness and prediction quality in medical ML tasks.

---

# 🔍 Overfitting Analysis

Compared training vs validation performance across all models.

### Observations

* Single Decision Trees heavily overfit
* Ensemble methods generalized better
* Boosting models achieved stronger stability across folds

---

# 🛠 Tech Stack

* Python
* Scikit-learn
* XGBoost
* LightGBM
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Imbalanced-learn


---

# 💡 Key Learnings

* Importance of fair benchmarking in ML research
* Difference between bagging and boosting
* Handling class imbalance in healthcare datasets
* Preventing data leakage
* Evaluating medical AI systems beyond simple accuracy

Output

<img width="676" height="608" alt="image" src="https://github.com/user-attachments/assets/9927f617-40bd-4610-8431-1461407ab421" />
<img width="521" height="512" alt="image" src="https://github.com/user-attachments/assets/9476e7fa-c250-4bda-9454-9249ad0800d3" />

