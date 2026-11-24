# 30-Day Readmission in Chronic Kidney Disease

## Research question

Can hospital encounter data help identify patients with chronic kidney disease at elevated risk of readmission within 30 days?

## Approach

This academic team project used MIMIC-IV hospital and emergency department tables. The cohort included approximately 79,000 hospitalizations. BigQuery supported cohort construction and feature preparation. Predictors included prior hospital and ED utilization, comorbidities, length of stay, and admission characteristics.

## Reported test results

| Logistic regression threshold | Precision | Recall | F1 |
| --- | ---: | ---: | ---: |
| 0.50 | 0.604 | 0.102 | 0.175 |
| 0.20 | 0.303 | 0.787 | 0.438 |

The lower threshold identified more readmissions and generated more false alerts. Test AUROC was approximately 0.65. Clinical use would require external validation and an assessment of the workload created by false alerts.

## Data access

MIMIC-IV is distributed through [PhysioNet](https://physionet.org/content/mimiciv/). This case study contains aggregate results only.
