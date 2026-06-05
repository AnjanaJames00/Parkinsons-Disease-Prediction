# Parkinsons-Disease-Prediction

Parkinson’s Disease affects speech patterns due to motor control impairment. This project uses biomedical voice measurements such as jitter, shimmer, HNR, and RPDE to classify whether a patient has Parkinson’s Disease.

Instead of testing only one model, this project performs a structured benchmarking study across multiple machine learning algorithms to compare their strengths fairly and scientifically.

---

🎯 Objective

Detect Parkinson’s Disease from voice features
Compare multiple ML models under identical conditions
Reduce overfitting and improve generalization
Evaluate models using medical-grade performance metrics
Identify the most reliable algorithm for this dataset


🧠 Models Compared
Model	Purpose
Logistic Regression	Linear baseline model
Decision Tree	Rule-based interpretable model
Random Forest	Ensemble bagging model
XGBoost	Gradient boosting model
LightGBM	Optimized boosting framework
⚙️ Methodology
1️⃣ Data Preprocessing
✔ Missing Value Check


Validated dataset quality and ensured no missing records existed.

✔ Patient-Level Aggregation

Multiple recordings from the same patient were averaged together to prevent data leakage and memorization.

✔ Correlation Analysis

Highly correlated features (>0.7 correlation) were removed to reduce redundancy and multicollinearity.

✔ Feature Selection

Used Chi-Square feature selection to retain the top 30 most informative features.

✔ Class Imbalance Handling

Applied Random Oversampling to balance Parkinson’s vs Healthy samples.

---

📊 Exploratory Data Analysis

Performed:

Correlation heatmaps
Class distribution visualization
Feature importance analysis
ROC curve comparison
Confusion matrix visualization
🚀 Model Training Pipeline

Each model was trained using:

Same train-test split
Same preprocessing
Same validation strategy
Same evaluation metrics

This ensured a fair scientific comparison.

📈 Evaluation Metrics

Medical datasets require more than just accuracy.

The project evaluated:

Accuracy
Precision
Recall
F1 Score
ROC-AUC Score
Cross-validation accuracy

Special focus was placed on Recall because false negatives in medical diagnosis are dangerous.

🔍 Hyperparameter Tuning
Random Forest

Used GridSearchCV to optimize:

Number of trees
Tree depth
Minimum split size
Leaf size
XGBoost

Optimized:

Learning rate
Max depth
Subsampling
Number of estimators
LightGBM

Used RandomizedSearchCV for faster tuning across:

num_leaves
max_depth
regularization
learning rate
subsampling
🧪 Overfitting Analysis

Compared training accuracy vs validation accuracy for every model.

Key Finding:
Basic Decision Tree severely overfit the dataset
Ensemble methods generalized much better
LightGBM and XGBoost achieved the strongest balance between accuracy and stability
📊 Results Summary

The final comparison showed:

Ensemble methods significantly outperformed single-tree models
Boosting models achieved the best ROC-AUC scores
Random Forest provided strong interpretability
LightGBM achieved the best speed-performance balance
🔬 Key Technical Concepts Used
Ensemble Learning
Bagging vs Boosting
Feature Engineering
Feature Selection
Cross Validation
Hyperparameter Optimization
ROC-AUC Analysis
Overfitting Detection
Medical ML Evaluation
🛠 Tech Stack
Python
Scikit-learn
XGBoost
LightGBM
Pandas
NumPy
Matplotlib
Seaborn
Imbalanced-learn
