# Hospital Readmission Rates Analysis

## Project Objective

The goal of this project is to review and analyze CMS hospital readmission data. From this analysis, we aim to identify any existing patterns in excess readmission ratio across clinical measures and states. This project focuses on exploratory data analysis, finding existing readmission patterns, and gaining insights for monitoring hospital outcomes.

## Language and libraries

- Python
- pandas
- matplotlib

## Dataset

This project uses the Hospital Readmissions Reduction Program dataset from the Centers for Medicare & Medicaid Services (CMS). The dataset is made up of 18,330 rows and 12 columns. The columns include facility name, facility ID, state, measure name, number of discharges, footnote, excess readmission ratio, predicted readmission rate, expected readmission rate, number of readmissions, start date, and end date.

## Data Cleaning

The dataset was cleaned by standardizing column names, converting necessary readmission related columns into numeric format, and removing records without usable readmission rates metrics.

These are the main columns that were used in the analysis:

- excess_readmission_ratio
- predicted_readmission_rate
- expected_readmission_rate
- measure_name
- state
- facility_id

## Analysis

The excess readmission ratio compares a hospital's predicted readmission rate with its expected readmission rate. Having an ERR above 1.0 indicates that predicted readmissions were greater than expected.

For this project, I added a new column called "high_readmission_rate" to categorize hospital measure records with an excess readmission ratio above 1.0. Then, using the refined dataframe, analyzed readmission patterns across clinical measures and states.


## Analysis Summary

1. 48.15% of hospital measure records had an excess readmission ratio above 1.0, which means that nearly half of the hospital measure records had more readmissions than their expectations of risk adjusted benchmark even after adjusting for patient risk factors.

2. The analyzed results shows that most of the excess readmission ratio values were centered near 1.0. This suggests that overall readmission rates was close to the expectations. However, individual hospital measure records still showed variation.

3. According to the analysis, CABG and AMI are the measures that show the highest proportion of hospital measure records with an excess readmission ratio above 1.0 among all the clinical measures analyzed. These results suggest that hospitals may benefit from monitoring closer to the post discharge care for coronary artery bypass graft surgery and acute myocardial infarction patients.

4. Some states had more than 60% of hospital measure records with excess readmission ratio above 1.0, which indicates there might be significant regional variation in readmission rates.

## Insights and Recommendations

1. I would recommend hospitals to monitor readmission rates of individual measures, instead of only monitoring the at the level of overall hospital. Although most of the average ERR values were close to 1.0, nearly half of the records had ERR above 1.0 at the same time. This analysis results showing that specific measures may still need attention.

2. Improved efforts of prioritizing clinical measures with higher proportion of records above the expected benchmark, such as CABG and AMI, may be needed. 

3. The results indicated state dependent variation, which suggests that regional monitoring can help identify where readmission rates issues are more common. Healthcare organizations could use this type of analysis to prioritize support based on regions and their levels of risks.

## References

Centers for Medicare & Medicaid Services. (2026). *Hospital Readmissions Reduction Program*. CMS Provider Data Catalog.  
https://data.cms.gov/provider-data/dataset/9n3s-kdb3

