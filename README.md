AIRECRUIT — AI-Powered Resume Screening & Candidate Role Recommendation System
An end-to-end intelligent recruitment platform that automates resume screening, skill extraction, candidate classification, and role recommendation using NLP and Machine Learning.

---
Live Demo
🚀 Launch AIRECRUIT on Streamlit
---
What This System Does
Parses and cleans resume text at scale
Extracts structured skills from unstructured content
Classifies candidates into 42 job-role categories with 98.75% accuracy
Ranks candidates against a job description using cosine similarity
Presents results through an interactive Streamlit dashboard
---
ML Pipeline
```
Raw Resumes (10,000)
    → Data Cleaning & Normalisation
    → TF-IDF Vectorisation (3,000 / 5,000 features)
    → Model Training (SVM / RF / LR / XGBoost)
    → Candidate Classification (42 categories)
    → Cosine Similarity Matching
    → Composite Scoring (60% match + 20% experience + 20% skills)
    → Ranked Candidate Shortlist
```
---
Model Performance
Model	Accuracy
Support Vector Machine (Production)	98.75%
Random Forest	98.15%
Logistic Regression	97.00%
XGBoost	96.50%
---
Repository Structure
```
AIRECRUIT-Resume-Screening-System/
├── app.py
├── requirements.txt
├── .streamlit/
│   └── config.toml
├── data/
│   ├── cleaned_resume_data.csv
│   ├── processed_resume.csv
│   ├── cleaned_jobs_data.csv
│   ├── processed_jobs.csv
│   ├── skills_list.csv
│   └── best_model_name.json
├── models/
│   ├── svm_pipeline.pkl
│   ├── preprocessor.pkl
│   ├── tfidf_match.pkl
│   ├── logistic_regression_pipeline.pkl
│   ├── random_forest_pipeline.pkl
│   ├── xgboost_pipeline.pkl
│   └── kmeans.pkl
└── notebooks/
    ├── 01_EDA.ipynb
    ├── 02_Preprocessing_Feature_Engineering.ipynb
    ├── 03_Model_Training.ipynb
    └── 04_Evaluation_Recommendation_System.ipynb
```
---
Tech Stack
Layer	Tools
Language	Python 3.12
ML & NLP	Scikit-Learn, XGBoost
Data	Pandas, NumPy
Visualisation	Matplotlib, Seaborn, Plotly
Deployment	Streamlit
Dataset	Kaggle Resume Dataset (10,000 records, 42 categories)
---
How to Run Locally
```bash
git clone https://github.com/Hania-Akbar1/AIRECRUIT-Resume-Screening-System.git
cd AIRECRUIT-Resume-Screening-System
pip install -r requirements.txt
streamlit run app.py
```
---
Known Limitations
Live PDF parsing not fully integrated in current version
Recruiter Workspace data persists within session only
Model generalisation outside training corpus not independently validated
Formal bias and fairness audit not yet conducted
