# Predicting-the-Probability-of-Potentially Preventable Complications(PPC)-Status-Change-in-Patient-Records-to-Prioritize-Reviews


### Project Overview

* Potentially Preventable Complications (PPCs) are assigned to patient records after discharge and directly affect hospital quality scores and reimbursement.
* However, these assignments are often revised after clinical documentation review.
* This project develops machine learning models to **predict which assigned PPC cases are likely to change**, enabling hospitals to prioritize high-impact record reviews earlier.



**Problem Context**

* PPCs influence Quality-Based Reimbursement (QBR) and hospital performance metrics.
* Clinical documentation teams review PPC cases without knowing which ones will change.
* This leads to wasted effort on stable cases and missed opportunities to correct high-impact records before penalties are finalized.

**Goal:** Predict PPC status change probability for assigned cases to support smarter review prioritization.

<img width="1149" height="440" alt="image" src="https://github.com/user-attachments/assets/46603106-1bd6-486d-83cf-9367acf6c6d2" />



### Data

* 20,185 PPC occurrences derived from hospital EHR data.
* Temporal sequences per patient and complication
* Features include demographics, diagnosis/procedure activity, POA changes, severity/mortality indicators,PPC metadata, etc.



### Modeling Approach

Built a hybrid ML system to predict whether an assigned PPC will change:

* **LSTM** for longitudinal PPC records
* **XGBoost** for short or single-snapshot cases
* **Clustering** for explainability and pattern discovery
* **SHAP** used to explain feature importance and model behavior.




### Results

* LSTM achieved ~91–95% accuracy with AUC ≈ 0.92.
* Static model performed well on sparse cases
* Diagnosis changes and POA updates were the strongest predictors



### Impact
* This work demonstrates how predictive modeling can improve clinical documentation workflows by prioritizing high-risk PPC rework cases, supporting better quality performance and operational efficiency


---


### Tech Stack
```
Data & Infrastructure
- Databricks
- Apache Spark (PySpark)
- SQL

Data Processing & Feature Engineering
- Python
- Pandas
- NumPy

Machine Learning
- TensorFlow / Keras (LSTM)
- XGBoost
- Scikit-learn

Explainability & Analysis
- SHAP
- Matplotlib
- Seaborn

Workflow & Development
- Jupyter Notebooks
- Git & GitHub
```


