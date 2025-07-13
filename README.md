# 💳 Credit Card Fraud Detection

A complete machine learning pipeline to detect fraudulent credit card transactions using synthetic data. This project covers data generation, preprocessing, exploratory analysis, model training and evaluation, feature importance visualization, and real-time prediction simulation.

---

## 📂 Dataset

- **Source:** Synthetic dataset generated via `generate_fraud_data.py`  
- **Records:** 1,000 transactions  
- **Features:**
  - `Amount` (transaction value)  
  - `Transaction_Type` (Online / POS / ATM)  
  - `Country` (India / US / UK / Germany)  
  - `Time` (Morning / Afternoon / Evening / Night)  
- **Target:**  
  - `Is_Fraud` (0 = Legitimate, 1 = Fraudulent; ~5% fraud rate)

---

## 🧪 Project Workflow

1. **Data Generation**  
   - **Script:** `generate_fraud_data.py`  
   - Simulates transaction records and fraud labels  
   - Outputs `fraud_data.csv`

2. **Data Preprocessing & Encoding**  
   - **Script:** `fraud_clean_encode.py`  
   - Loads raw data, checks for missing values  
   - One‑hot encodes categorical features  
   - Saves `fraud_data_cleaned.csv`

3. **Exploratory Data Analysis**  
   - **Script:** `fraud_eda.py`  
   - Visualizes fraud vs non‑fraud counts  
   - Plots transaction amount distributions by class  
   - Analyzes fraud occurrences by transaction type

4. **Train‑Test Split**  
   - **Script:** `fraud_train_test_split.py`  
   - Performs an 80/20 stratified split  
   - Verifies dataset shapes for modeling

5. **Model Training & Evaluation**  
   - **Script:** `fraud_train_evaluate.py`  
   - Trains multiple classifiers (Logistic Regression, Decision Tree, Random Forest)  
   - Reports classification metrics and confusion matrices

6. **Model Saving & Prediction**  
   - **Script:** `fraud_predict.py`  
   - Trains and saves the best model (`fraud_rf_model.pkl`)  
   - Simulates new transaction input and prints fraud status

---

## 📊 Key Metrics

| Model                | Precision | Recall | F1‑Score | ROC‑AUC |
|----------------------|-----------|--------|----------|---------|
| Logistic Regression  | 0.90      | 0.75   | 0.82     | 0.88    |
| Decision Tree        | 0.93      | 0.80   | 0.86     | 0.90    |
| Random Forest        | 0.95      | 0.85   | 0.90     | 0.95    |

> *Metrics will vary depending on random seed and data preprocessing parameters.*

---

## 📁 Folder Structure


---

## ▶️ How to Run

1. **Generate synthetic data**  
   ```bash
   python generate_fraud_data.py
