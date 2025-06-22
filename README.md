# 🏥 Predictive-Analysis: Emergency Department Outcome Prediction

This project predicts **Emergency Department (ED) outcomes** using machine learning (ML) models on data from **MIMIC-IV-ED**.

We used demographic info, vital signs, and chief complaints to predict outcomes like hospital admission, discharge, or mortality. The models help with early triage decisions and resource planning.

---

## 📊 Problem Statement

Emergency Departments are resource-constrained and need fast decisions. Using ML models trained on structured and unstructured data, we aim to:

- Predict **disposition** (e.g., discharge, admit)
- Estimate **mortality risk**
- Improve triage support using early-available data

---

## 🧠 Data & Tools

- **Dataset**: MIMIC-IV-ED v2.2 (PhysioNet)
- **Tools**: Python 3, Google Colab
- **Libraries**: Pandas, NumPy, Matplotlib, Plotly, Scikit-learn, XGBoost

---

## 🧪 Features Used

- Demographics: age, gender, race
- Chief complaint (text, processed using NLP)
- Vital signs: temperature, heart rate, BP, SpO₂, respiratory rate
- Social factors: marital status, insurance, language
- ED details: arrival method, triage acuity, length of stay

---

## 🛠️ ML Workflow

1. **Preprocessing**
   - Filter ICD-10 cases only
   - Cleaned triage, vitals, and meds tables
   - Categorical encoding + scaling
   - NLP categorization of chief complaints (reduced to 19 groups)

2. **Modeling**
   - Feature selection + PCA
   - K-Means clustering (4 clusters)
   - Classification models:
     - Logistic Regression
     - Decision Tree
     - XGBoost (best performer)
     - LLM (Me-LLaMA)

3. **Performance**
   - Best AUC-ROC: **0.88**
   - Evaluated with accuracy, precision, recall, F1-score

---

## 📌 Key Insights

- **Chief Complaints** + **Vital Signs** were the most predictive
- **XGBoost** outperformed all baseline models
- NLP helped convert free-text into structured inputs

---

## 📁 Files in Repo
📦 Predictive-Analysis
├── Clustering_and_Classification.ipynb # ML model and clustering
├── ED_exploratory_analysis.ipynb # EDA & preprocessing
├── Final Report.pdf # Detailed report
└── README.md # Project summary


---

## 📬 Contact

Gaurav More  
📧 more.56@buckeyemail.osu.edu  
🔗 [LinkedIn](https://linkedin.com/in/gauravmore1527)

---

## 📎 Data Sources

- [MIMIC-IV-ED Dataset (v2.2)](https://physionet.org/content/mimic-iv-ed/2.2/)
- [MIMIC-IV Dataset (v3.1)](https://physionet.org/content/mimiciv/3.1/)
