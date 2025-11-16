# Hospital Readmission Prediction

## Overview
A machine learning system to predict the risk of patient readmission within 30 days after hospital discharge, using structured health record data. This project demonstrates the end-to-end AI workflow, from data preprocessing to model evaluation and result submission, tailored for real-world healthcare use cases.

## Project Structure
```
project-root/
│
├── data/                  # Raw & processed datasets (train_df.csv, test_df.csv, sample_submission.csv)
├── notebooks/             # Jupyter notebooks for analysis and modeling
├── src/                   # Python modules (e.g., preprocessing.py, train_model.py)
├── reports/               # Outputs: figures, evaluation results
├── requirements.txt        # Package dependencies
└── README.md              # This file
```

## Dataset
Download Hospital Readmission Prediction from _`kaggle.com`_  
https://www.kaggle.com/datasets/vanpatangan/readmission-dataset

- **Train:** `train_df.csv` — includes features + `readmitted` (target)
- **Test:** `test_df.csv` — same features, no `readmitted`
- **Sample Submission:** `sample_submission.csv` — shows required output format

**Features:**
- age (numeric)
- gender (categorical)
- primary_diagnosis (categorical)
- num_procedures (numeric)
- days_in_hospital (numeric)
- comorbidity_score (numeric)
- discharge_to (categorical)
- readmitted (0/1, only in training set)

## How to Run
1. **Clone repo / download code.**
2. Place dataset CSVs in /data directory.
3. Create a Python virtual environment (optional, but recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # or venv\Scripts\activate on Windows
   pip install -r requirements.txt
   ```
4. Launch the primary notebook or script:
   ```bash
   jupyter notebook notebooks/01_full_workflow.ipynb
   ```
   Follow step-by-step: data exploration, preprocessing, training, evaluation, and prediction on the test set.
5. The output `final_submission.csv` (in /data or /output) is formatted for submission.

## Main Scripts/Notebooks
- **notebooks/01_full_workflow.ipynb:** Walks through EDA, data cleaning, feature engineering, model building, and result generation.
- **src/preprocessing.py:** Reusable functions for encoding, normalization, and imputation (modularizes notebook code).
- **src/train_model.py:** (Optional) If models are trained outside notebook.

## Results & Evaluation
After training and tuning, model results include:
- **Validation Metrics:** Precision, recall, accuracy, confusion matrix.
- **Model Artifacts:** Best estimator parameters are saved for reproducibility.
- **Submission:** Test predictions for external scoring.

## Key Dependencies
- Python 3.8+
- pandas, numpy (data manipulation)
- scikit-learn (models & metrics)
- jupyter (for exploratory notebooks)

## AI Workflow Stages
1. Problem Definition
2. Data Collection
3. Data Preprocessing & Feature Engineering
4. Model Development & Evaluation
5. Model Selection & Hyperparameter Tuning
6. Test Prediction & Submission
7. (Optional) Model Deployment Demo

## Contact & Issues
Please raise issues via GitHub, or contact project contributors as listed in the repository.