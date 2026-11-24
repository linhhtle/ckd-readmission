# 30-Day Readmission in Chronic Kidney Disease

## Research question

Hospitals need to identify patients at high risk of returning shortly after discharge. Chronic kidney disease (CKD) patients may have other health conditions, such as diabetes or heart failure, which could affect their risk of being readmitted within 30 days. Can machine-learning models predict 30-day readmission among CKD patients, and how does multimorbidity affect readmission risk?

## Approach

This academic team project used MIMIC-IV hospital and emergency department tables. The cohort included approximately 79,000 hospitalizations. BigQuery supported cohort construction and feature preparation. Predictors included prior hospital and ED utilization, comorbidities, length of stay, and admission characteristics.

## Reported test results

| Logistic regression threshold | Precision | Recall | F1 |
| --- | ---: | ---: | ---: |
| 0.50 | 0.604 | 0.102 | 0.175 |
| 0.20 | 0.303 | 0.787 | 0.438 |

The lower threshold identified more readmissions and generated more false alerts. Test AUROC was approximately 0.65. Clinical use would require external validation and an assessment of the workload created by false alerts.

## Explore the analysis

- [Project notebook](BA878_Team_Project.ipynb)

## Data access

MIMIC-IV is distributed through [PhysioNet](https://physionet.org/content/mimiciv/). Running the notebook requires authorized access to the prepared BigQuery dataset. The notebook includes aggregate results.
