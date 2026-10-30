# Elevate Labs AI/ML Internship

This repository contains the Artificial Intelligence and Machine Learning work completed during my **Elevate Labs AI/ML Internship**.

It includes hands-on Machine Learning tasks, end-to-end AI/ML projects, model evaluation, data preprocessing, exploratory data analysis, NLP, and Streamlit deployment.

---

## 📌 Internship Work

### Task 1: Data Cleaning & Preprocessing

Performed complete data preparation on an E-commerce Customer Churn dataset.

**Work Covered:**

- Dataset inspection and validation
- Duplicate removal
- Missing-value handling using median imputation
- Categorical value standardization
- One-hot encoding
- Outlier analysis using the IQR method
- Feature scaling using `StandardScaler`
- Cleaned dataset generation

**Tools:**

`Python` `Pandas` `NumPy` `Matplotlib` `Seaborn` `Scikit-learn`

---

### Task 2: Exploratory Data Analysis

Performed exploratory analysis on the cleaned E-commerce Customer Churn dataset.

**Work Covered:**

- Summary statistics
- Histograms and boxplots
- Categorical distributions
- Churn distribution analysis
- Correlation matrix and heatmap
- Group-wise churn analysis
- Pairplot visualization
- Data-driven observations and feature-level insights

**Tools:**

`Python` `Pandas` `NumPy` `Matplotlib` `Seaborn` `Plotly`

---

### Task 3: Linear Regression

Implemented Simple and Multiple Linear Regression for house price prediction.

**Work Covered:**

- Data inspection and preprocessing
- Categorical variable encoding
- 80:20 train-test split
- Simple Linear Regression
- Multiple Linear Regression
- MAE, MSE and R² evaluation
- Regression-line visualization
- Actual vs predicted comparison
- Coefficient interpretation

**Results:**

| Model | MAE | MSE | R² |
|---|---:|---:|---:|
| Simple Linear Regression | 1,474,748.13 | 3,675,286,604,768.19 | 0.2729 |
| Multiple Linear Regression | 970,043.40 | 1,754,318,687,330.66 | 0.6529 |

---

### Task 4: Logistic Regression

Implemented Logistic Regression for binary classification using the Breast Cancer Wisconsin dataset.

**Work Covered:**

- Data preprocessing
- Binary target encoding
- Stratified train-test split
- Feature standardization
- Logistic Regression training
- Confusion matrix
- Precision and recall
- ROC-AUC and ROC curve
- Classification threshold tuning
- Sigmoid function visualization

**Results:**

Default threshold `0.5`:

- Precision: **97.50%**
- Recall: **92.86%**
- ROC-AUC: **99.60%**

Tuned threshold `0.3`:

- Precision: **97.62%**
- Recall: **97.62%**

---

### Task 5: Decision Trees and Random Forests

Implemented and compared Decision Tree and Random Forest classifiers using the Heart Disease dataset.

**Work Covered:**

- Duplicate analysis and removal
- Decision Tree training
- Tree-depth analysis
- Overfitting analysis
- Controlled Decision Tree using `max_depth=3`
- Random Forest training
- Feature importance analysis
- 5-fold cross-validation

**Results:**

| Model | Test Accuracy |
|---|---:|
| Decision Tree (`max_depth=3`) | **80.33%** |
| Random Forest (`n_estimators=100`) | **75.41%** |

5-fold cross-validation mean accuracy:

**79.46%**

---

### Task 6: KNN Classification

Implemented K-Nearest Neighbors classification using the Iris dataset.

**Work Covered:**

- Dataset inspection
- Feature standardization
- 80:20 train-test split
- Multiple K-value comparison
- Final KNN model selection
- Accuracy evaluation
- Confusion matrix
- Decision-boundary visualization

**Final Result:**

- Selected K: **7**
- Test Accuracy: **96.67%**
- Correct test predictions: **29/30**

---

## 🚀 End-to-End AI/ML Projects

### 1. Fraud Detection in Credit Card Transactions

An end-to-end Machine Learning project for identifying potentially fraudulent credit card transactions.

**Techniques Used:**

- Exploratory Data Analysis
- Data preprocessing
- Handling severe class imbalance
- Logistic Regression
- Random Forest
- XGBoost
- Isolation Forest
- Threshold tuning
- Feature importance analysis
- Model persistence
- Batch prediction
- Streamlit deployment

**Final XGBoost Performance:**

| Metric | Result |
|---|---:|
| Accuracy | **99.95%** |
| Fraud Precision | **97.26%** |
| Fraud Recall | **74.74%** |
| Fraud F1-score | **84.52%** |
| ROC-AUC | **0.9707** |
| PR-AUC | **0.8153** |

**Live Application:**  
https://fraud-detection-in-credit-card-transactions.streamlit.app/

**Project Folder:**  
`Fraud-Detection-in-Credit-Card-Transactions/`

**Standalone Repository:**  
https://github.com/varungodhani11/Fraud-Detection-in-Credit-Card-Transactions

---

### 2. News Article Classification

An NLP-based Machine Learning project for classifying news articles as **Fake** or **Real**.

**Techniques Used:**

- Text preprocessing
- Regular-expression cleaning
- Tokenization
- Stopword removal
- NLTK
- TF-IDF Vectorization
- Logistic Regression
- Multinomial Naive Bayes
- Model evaluation
- Confusion Matrix
- Streamlit deployment

**Results:**

| Model | Accuracy | Fake F1-score | Real F1-score |
|---|---:|---:|---:|
| Logistic Regression | **98.76%** | **0.9881** | **0.9870** |
| Multinomial Naive Bayes | 93.91% | 0.9420 | 0.9359 |

**Live Application:**  
https://fake-real-news-classifier.streamlit.app/

**Project Folder:**  
`News-Article-Classification/`

**Standalone Repository:**  
https://github.com/varungodhani11/News-Article-Classification

> **Note:** This project is a text-classification demonstration, not a fact-checking system. Model predictions and confidence scores do not prove whether an article is factually true or false.

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- NLTK
- TF-IDF
- Matplotlib
- Seaborn
- Plotly
- Joblib
- Streamlit
- Jupyter Notebook
- Git
- GitHub

---

## 📂 Repository Structure

```text
Elevate-Labs-AIML-Internship/
│
├── Tasks/
│   ├── Task-1-Data-Cleaning-Preprocessing/
│   ├── Task-2-Exploratory-Data-Analysis/
│   ├── Task-3-Linear-Regression/
│   ├── Task-4-Logistic-Regression/
│   ├── Task-5-Decision-Trees-and-Random-Forests/
│   └── Task-6-KNN-Classification/
│
├── Fraud-Detection-in-Credit-Card-Transactions/
│
├── News-Article-Classification/
│
└── README.md
