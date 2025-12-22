# Predicting Inpatient Clinical Deterioration Using FHIR EHR Data

## Project Overview
This project aims to predict which hospitalized patients are at risk of clinical deterioration within the next 24 hours using routinely collected vitals and labs from a FHIR server.

**Outcome:** ICU transfer or Rapid Response Team call.

**Approach:** 
- Extract data from public FHIR server, data anonymized
- Clean and preprocess vitals and lab measurements
- Feature engineering with time windows
- Train and evaluate predictive models (logistic regression, tree-based models, boosting)


## Project Structure
Deterioration_Prediciton_FHIR/

├── notebooks/ 

├── data/

    │ ├── raw/ # raw data 
    
    │ └── processed/ # cleaned data for reproducibility

├── src/ 

├── README.md 

├── requirements.txt 

└── .gitignore 



## Notebooks Workflow
1. **01_Data_Pull.ipynb** – Pull patients, observations, and encounters from a public FHIR server
2. **02_Data_Cleaning.ipynb** – Clean raw data, handle missing values, normalize units
3. **03_Feature_Engineering.ipynb** – Aggregate features for modeling
4. **04_EDA.ipynb** – Exploratory data analysis 
5. **05_Modeling.ipynb** – Train baseline and advanced predictive models 
6. **06_Evaluation.ipynb** – Evaluate models with ROC, PR curves, confusion matrices, and calibration


## How to Run

1. Clone the repo:
git clone https://github.com/yourusername/ehr-fhir-deterioration.git
cd ehr-fhir-deterioration

2. Install dependencies:
pip install -r requirements.txt

3. Open Jupyter and run notebooks:
jupyter notebook

## Data
Raw data: data/raw/ (ignored by Git)
Processed data: data/processed/ (small, cleaned dataset for reproducibility)
Note: Synthetic or anonymized data is used for privacy

## Results & Insights
Model evaluation metrics (e.g., ROC-AUC, F1, Balanced Accuracy) will be reported in 06_Evaluation.ipynb
EDA visualizations in 04_eda.ipynb.

## Author
Sana Siddiqui, MD
