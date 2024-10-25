# Health Premium Prediction Model

This project implements a **Health Premium Prediction Model** that predicts insurance premium amounts for different age groups. The project uses **Multiple Linear Regression** for the "age <= 25" group and **XGBoost with Random Search Tuning** for the "age > 25" group. A web interface is built with **Streamlit** where users can input personal and medical attributes to estimate their insurance premiums.

## 1. Project Overview

The **Health Premium Prediction Model** takes into account multiple features such as age, BMI, smoking habits, and more to predict health insurance premiums. This project is valuable for insurance companies or individuals who want to estimate health insurance premiums based on personal health and lifestyle attributes.

## 2. Project Structure

The repository is structured as follows:

- `main.py` — Streamlit application file
- `prediction_helper.py` — Helper functions for preprocessing and making predictions
- `requirements.txt` — Python dependencies for the project
- `README.md` — Project README file
- `ml_premium_prediction_young_with_gr.ipynb` — Jupyter notebook for the "age <= 25" group, including data exploration, preprocessing, and model training
- `ml_premium_prediction_rest_with_gr.ipynb` — Jupyter notebook for the "age > 25" group, including data exploration, preprocessing, and model training
- `artifacts/` — Directory containing model artifacts:
  - `model_young.joblib` — Serialized model for the "age <= 25r" group
  - `model_rest.joblib` — Serialized model for the "age > 25" group
  - `scaler_young.joblib` — Scaler for the "age <= 25r" group
  - `scaler_rest.joblib` — Scaler for the "age > 25" group

## 3. Features

The model predicts health insurance premiums based on the following features:

- **Age:** Applicant's age in years.
- **BMI:** Body Mass Index of the applicant.
- **Smoking:** Whether the applicant smokes (Yes/No).
- **Medical History:** Previous medical conditions.
- **Number of Dependents:** Number of dependents covered under the policy.
- **Health Score:** A composite score indicating the applicant's overall health.
- **Region:** Geographical region of the applicant.
- **Policy Type:** Type of health insurance policy (individual, family, etc.).

## 4. Installation Instructions

### Clone the repository
```bash
git clone https://github.com/Vraj-Data-Scientist/ml-health-premium-prediction.git
cd ml-health-premium-prediction

python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
pip install -r requirements.txt

streamlit run main.py
