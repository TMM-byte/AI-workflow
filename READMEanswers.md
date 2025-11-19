Part 1: AI Problem Definition
Problem Definition
Hypothetical AI Problem: Predicting student dropout rates in a university setting.

Objectives
Identify students at risk of dropping out early in their academic journey.
Provide actionable insights to academic advisors and support services.
Improve student retention and overall institutional performance.
Stakeholders
University Administrators – Interested in improving student retention and institutional outcomes.
Academic Advisors – Use the model to proactively support at-risk students.
Key Performance Indicator (KPI)
Accuracy of prediction: The percentage of students correctly classified as either at-risk or not at-risk of dropping out.
Part 2: Data Collection & Preprocessing
Data Sources
Student Academic Records – Including grades, attendance, and course enrollment history.
Demographic Data – Such as age, gender, socioeconomic background, and first-generation student status.
Potential Bias
Socioeconomic bias: Students from lower-income backgrounds might be disproportionately labeled as "at-risk" due to systemic inequalities, not necessarily their academic performance.
Preprocessing Steps
Handling missing data – Impute missing values using mean, median, or mode, or remove rows with excessive missing data.
Normalization – Scale numerical features (e.g., grades) to a common range (e.g., 0–1).
Encoding categorical variables – Convert non-numeric data (e.g., gender, major) into numerical form using one-hot encoding or label encoding.
Part 3: Model Development
Model Choice
Random Forest – Chosen for its ability to handle non-linear relationships, robustness to overfitting, and interpretability compared to deep learning models.
Data Splitting
Train (70%): Used to train the model.
Validation (15%): Used to tune hyperparameters and prevent overfitting.
Test (15%): Used to evaluate the final model’s performance on unseen data.
Hyperparameters to Tune
Number of trees (n_estimators) – More trees can reduce variance but increase computational cost.
Maximum depth (max_depth) – Controls the complexity of the model to prevent overfitting.
Part 4: Evaluation & Deployment
Evaluation Metrics
Accuracy – Measures the overall correctness of the model.
F1-Score – Balances precision and recall, especially important in imbalanced datasets (e.g., few students drop out).
Concept Drift
Definition: A change in the statistical properties of the input data over time, which can cause the model’s performance to degrade.
Monitoring: Use drift detection tools (e.g., ADWIN, Page-Hinkley) to monitor input data and retrain the model when drift is detected.
Technical Challenge During Deployment
Scalability: Deploying the model to handle high volumes of student data in real-time could be computationally intensive. Solutions include using cloud-based services or model optimization techniques like quantization or pruning.
Part 2: Case Study Application
Problem Scope
Problem: Predict the likelihood of a patient being readmitted to the hospital within 30 days of discharge.
Objectives:
Identify high-risk patients for targeted interventions.
Improve patient outcomes and reduce hospital costs.
Stakeholders:
Hospital Administrators – Interested in reducing readmission rates and improving efficiency.
Nurses and Doctors – Use the model to provide better care for high-risk patients.
Data Strategy
Data Sources
Electronic Health Records (EHRs) – Including diagnosis, treatment history, and lab results.
Patient Demographics – Age, gender, insurance type, and socioeconomic status.
Ethical Concerns
Patient Privacy – Ensuring data is anonymized and complies with regulations like HIPAA.
Bias in prediction – Certain groups may be disproportionately flagged as high-risk due to historical data patterns.
Preprocessing Pipeline
Data Cleaning – Remove duplicates, correct inconsistencies, and handle missing values.
Feature Engineering – Create new features such as "number of previous hospitalizations" or "average length of stay."
Normalization and Encoding – Normalize numerical features and encode categorical variables (e.g., gender, diagnosis codes).
Model Development
Model Choice
Logistic Regression – Chosen for its simplicity, interpretability, and suitability for binary classification (readmission or not).