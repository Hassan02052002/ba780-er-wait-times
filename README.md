# What Drives Emergency Department Wait Times Across U.S. Hospitals?

**BA780 Team Assignment · Boston University MSBA · Cohort A · Team 4**

Emergency department (ED) wait times vary widely across the United States. This project asks **which hospital and community characteristics are associated with longer ED visits**. We clean three public datasets, explore each one, and combine them into a single hospital-level table that will be used for the final analysis.

**Main outcome:** `OP_18b`, the median time (in minutes) patients spend in the ED from arrival to departure, excluding psychiatric and transfer patients.

## Data

| File | Source | Unit of observation |
|---|---|---|
| `data/timely_effective_care_hospital.csv` | [CMS Timely and Effective Care – Hospital](https://data.cms.gov/provider-data/dataset/yv7e-xc69) | Hospital × quality measure |
| `data/hospital_general_information.csv` | [CMS Hospital General Information](https://data.cms.gov/provider-data/dataset/xubh-q36u) | Hospital |
| `data/acs_dp03_2024_states.csv` | [U.S. Census ACS 2024 1-Year, Table DP03](https://data.census.gov/table/ACSDP1Y2024.DP03?g=010XX00US$0400000) (selected columns, all states) | State |

All three datasets are U.S. government public data.

## Notebook

`A04-ER-Wait-Times-US-Hospitals.ipynb` loads the data directly from this repository, so it runs as-is in Google Colab or Jupyter (**Runtime / Kernel → Restart & Run All**). It contains:

1. **ED wait times and crowding** (CMS Timely and Effective Care)
2. **Hospital characteristics** (CMS Hospital General Information)
3. **State economic conditions** (Census ACS DP03)
4. **Combined dataset**: one row per hospital, ready for the final analysis

Requirements: `pandas`, `numpy`, `matplotlib`.
