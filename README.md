# 💳 Credit Card Fraud Detection  

## 📌 Overview  
This project aims to **detect fraudulent credit card transactions** using Machine Learning.  
The dataset is highly **imbalanced** (~0.17% fraud cases), which makes fraud detection a real-world challenge.  

We performed **Exploratory Data Analysis (EDA)**, applied **data preprocessing**, handled class imbalance, and trained multiple ML models to classify transactions as **fraudulent** or **genuine**.  

---

## 📂 Dataset  
- Source: [Kaggle - Credit Card Fraud Detection](https://www.kaggle.com/mlg-ulb/creditcardfraud)  
- Transactions: **284,807**  
- Features: **30 (PCA-transformed + Time + Amount)**  
- Target:  
  - `0` → Genuine  
  - `1` → Fraudulent  

---

## 🔎 Exploratory Data Analysis (EDA)  
- Checked for **missing values & duplicates**  
- Analyzed **class imbalance** (only 492 fraud cases)  
- Distribution of **Transaction Amount** and **Time**  
- **Correlation heatmap** of features  
- Plotted **boxplots & histograms** for fraud vs non-fraud  

📊 Example Visuals:  
- Class distribution (imbalanced dataset)  
- Histogram of transaction amount  
- Heatmap of correlations  

---

## ⚙️ Preprocessing  
- Scaled **Amount** & **Time** features  
- Applied **SMOTE (oversampling)** and undersampling to handle imbalance  
- Split dataset into **train-test sets**  

---

## 🤖 Models Implemented  
- Logistic Regression  
- Decision Tree  
- Random Forest  
- XGBoost  

---

## 📈 Evaluation Metrics  
Since the dataset is imbalanced, **accuracy is not enough**.  
We used:  
- Confusion Matrix  
- Precision, Recall, F1-score  
- ROC-AUC Curve  
- PR Curve  

👉 Best results were achieved using **Random Forest / XGBoost** with high Recall and AUC.  

---

## 🚀 Results & Insights  
- Fraudulent transactions are usually of **smaller amounts** compared to genuine ones.  
- **Tree-based models** (Random Forest, XGBoost) performed better than Logistic Regression.  
- **Recall is more important than Accuracy** → catching fraud is critical even if some false positives occur.  

---

## 🛠️ Tech Stack  
- Python 🐍  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Scikit-learn  
- Imbalanced-learn (SMOTE)  
- XGBoost  

---

## ▶️ Usage Guide  

### 1. Clone Repository  
```bash
git clone https://github.com/your-username/credit-card-fraud-detection.git
cd credit-card-fraud-detection
3. Dataset Setup

Download dataset from Kaggle

Place creditcard.csv file inside the data/ folder

4. Run Jupyter Notebook
jupyter notebook notebooks/eda_fraud_detection.ipynb

5. Results

EDA → Graphs, Class imbalance visualization

Model training → Performance metrics (Precision, Recall, AUC)

Insights → Feature importance & fraud patterns
