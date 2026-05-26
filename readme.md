Hospital Readmission Risk Prediction

Dataset: Diabetes 130-US Hospitals (UCI) | 100,000+ records

1. Problem Statement
Diabetic patients account for a large share of costly unplanned hospital readmissions. This project explores:
Can we predict whether a diabetic patient will be readmitted within 30 days of discharge, using clinical and administrative data?
Key questions:
•	Which patient characteristics most strongly predict readmission?
•	Do medication changes during admission affect readmission risk?
•	How does number of prior visits relate to future readmission?

2. Tools and Technologies Used
•	Data Preparation: Python (pandas, numpy)
•	Machine Learning: scikit-learn (Logistic Regression), imbalanced-learn (SMOTE)
•	Visualization: matplotlib, seaborn

3. Methodology
Step 1: Data Collection- Dataset source:UCI ML Repository. Contains patient demographics, admission details, lab results, medications, and readmission outcomes across 130 US hospitals.
Step 2: Preprocessing - Remove high-missing columns, encoded categorical variables, mapped ICD-9 codes to clinical categories, and retained only the first encounter per patient.
Step 3: EDA - Explore class distribution, correlation between features and readmission, and breakdown of readmission rates by age, diagnosis, and discharge type.
Step 4: Handling Imbalance - Apply SMOTE to address the ~11% minority class (readmitted within 30 days).
Step 5: Modelling- Logistic Regression will be used as the primary model, with additional classifiers explored for comparison
Step 6: Evaluation- Asses using Precision, Recall, F1-Score etc

4. Insights & Discoveries
•	Patients with more prior inpatient visits show higher readmission rates
•	Medication changes during admission correlate with readmission likelihood
•	Certain primary diagnoses (circulatory, respiratory) are disproportionately linked to 30-day readmission
•	Older age groups and higher diagnosis counts indicate greater risk
•	Socioeconomic Status (SES): Patients with no insurance/self-pay admission sources may show higher readmission rates, reflecting limited access to post-discharge care, medications, and follow-up appointments

5. Potential Solutions
•	Assign readmission risk scores at discharge to trigger follow-up care
•	Flag high-risk patients for case manager assignment
•	Inform hospital quality teams about the highest-risk patient segments

6. Business and Community Impact
Hospitals- Reduces financial penalties tied to excess readmissions under value-based care models.
Clinical Teams- Supports better discharge decisions and earlier interventions. 
Patients- Earlier support leads to better post-discharge health outcomes.

7. Future Improvements
•	Test ensemble models (Random Forest) for improved accuracy
•	Deploy as an API integrated with EHR systems

8. Project Repository
https://github.com/WambuiiMaina/ML_foundations-capstone-project.git
