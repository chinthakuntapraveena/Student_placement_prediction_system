# AI-Powered Student Placement Prediction, Salary Estimation, Skill Gap Analysis & Career Recommendation System

An end-to-end, production-grade Educational Decision-Support System (EDSS) designed for final-year engineering students, academic placement cells, and data science portfolios.

---

## 🎯 Key Capabilities
1. **Calibrated Placement Prediction**: Probability scores generated via benchmarked classifiers (Logistic Regression, Random Forest, XGBoost).
2. **Conditional Salary Estimation**: CTC package prediction (in LPA) for placed candidates via supervised regressors.
3. **Explainable AI (XAI)**: Individual and global feature attributions calculated using SHAP (SHapley Additive exPlanations).
4. **Skill Gap Diagnostics**: Benchmarking student competencies across Python, SQL, DSA, ML, Power BI, and Soft Skills against market expectations.
5. **Configurable Role Skill Matching**: Multi-track alignment vectors for Data Analyst, Machine Learning Engineer, Software Development Engineer (SDE), and Business Analyst profiles.
6. **Prescriptive Learning Recommendations**: Automated learning checklists and remediation roadmaps.
7. **Production Data Persistence**: Relational storage using MySQL with secure parameterized queries and environment-based secret management.
8. **Interactive Web Dashboard**: Multi-page responsive UI powered by Streamlit and Plotly.

---

## 📁 Repository Directory Structure

```text
student-placement-ai/
│
├── data/
│   ├── raw/                 # Immutable original raw datasets
│   └── processed/           # Cleaned, transformed, and feature-engineered datasets
│
├── notebooks/               # Step-by-step exploratory and experimental Jupyter notebooks
│   ├── 01_data_understanding.ipynb
│   ├── 02_data_cleaning.ipynb
│   ├── 03_eda.ipynb
│   ├── 04_feature_engineering.ipynb
│   ├── 05_model_training.ipynb
│   ├── 06_model_evaluation.ipynb
│   └── 07_explainability.ipynb
│
├── src/                     # Production modular Python source code
│   ├── __init__.py
│   ├── generate_dataset.py       # Statistically grounded data synthesis engine
│   ├── data_preprocessing.py     # Cleaning, validation, and missing-value imputation
│   ├── feature_engineering.py    # Composite domain indices and transformations
│   ├── train_placement_model.py  # Classification training, CV, and tuning
│   ├── train_salary_model.py     # Salary regression pipeline training
│   ├── prediction.py             # Inference pipeline wrapper (Placement + CTC)
│   ├── recommendation.py         # Skill-gap engine and personalized learning advisor
│   └── database.py               # MySQL connection pooling and CRUD operations
│
├── models/                  # Serialized pipelines and model metadata
│   ├── placement_model.pkl
│   ├── salary_model.pkl
│   └── preprocessor.pkl
│
├── app/                     # Interactive Streamlit Web Application
│   ├── app.py               # Main navigation controller
│   └── pages/               # Dedicated multi-page modules
│       ├── 1_Student_Profile.py
│       ├── 2_Placement_Prediction.py
│       ├── 3_Salary_Estimation.py
│       ├── 4_Explainable_AI.py
│       ├── 5_Skill_Gap_Analysis.py
│       ├── 6_Career_Matching.py
│       ├── 7_Recommendations.py
│       └── 8_Admin_Analytics.py
│
├── database/                # Relational schema scripts
│   └── schema.sql
│
├── tests/                   # Pytest test suite for validation and pipelines
│   └── __init__.py
│
├── docs/                    # Formal Software Requirements and Data Dictionaries
│   ├── 01_project_charter_and_srs.md
│   ├── 02_data_dictionary.md
│   └── 03_data_collection_strategy.md
│
├── requirements.txt         # Project dependencies
├── .gitignore               # Ignored artifacts, virtual environments, and secrets
└── README.md                # Project documentation
```

---

## 🚀 Quick Setup & Execution

### 1. Create and Activate Virtual Environment
```bash
python -m venv venv
# On Windows PowerShell:
.\venv\Scripts\Activate.ps1
# On macOS/Linux:
source venv/bin/activate
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Generate Raw Dataset
```bash
python src/generate_dataset.py
```

---

## ⚖️ Ethical & Educational Notice
This application is strictly formulated as an **Educational Decision-Support System**. Its predictions are probabilistic diagnostic indicators intended to help students allocate study time effectively. It is **not** an automated guarantee of employment or recruitment disqualification.
