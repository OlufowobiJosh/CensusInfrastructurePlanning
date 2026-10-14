# Census Population Analysis & Community Planning

**Python · Pandas · Jupyter Notebook · Exploratory Data Analysis · Demographic Scenarios**

## Project overview

This portfolio project explores a community census dataset to understand population structure, employment, marital status and household characteristics, with the aim of informing questions about future demand for schools, healthcare, housing and other local services.

The original university coursework, including the updated `censusa(3).ipynb` notebook, examined **7,758 individual census records**. The public repository uses aggregated data and a privacy-preserving notebook instead of the identifiable source records.

## Business problem

A local council needs to understand its community's demographic profile before planning future services. This analysis explores:

- What is the age and gender composition of the community?
- How are employment and marital-status categories distributed?
- What do household occupancy and age patterns suggest about potential service needs?
- How might population totals change over **5, 10, 15 and 20 years** under different *illustrative* growth assumptions?

## What I did

1. **Data quality:** Inspected missing values, duplicates, inconsistent demographic entries and age anomalies.
2. **Exploratory analysis:** Investigated age and gender distributions, age bands, employment, marital status and household occupancy.
3. **Demographic indicators:** Explored approximate birth and mortality indicators in the updated coursework; these are proxies rather than independently validated rates.
4. **Visualisation:** Created charts to communicate demographic patterns.
5. **Scenario planning:** Added separate hypothetical population-change scenarios for 5–20 years using clearly stated annual growth assumptions.

## Selected visualisations

These five charts were extracted from the original coursework notebook. They are **static historical coursework illustrations**, not charts produced by the privacy-preserving public notebook. They should not be treated as independently validated official statistics.

### 1. Population pyramid by age and gender

![Population pyramid by age and gender](images/Census_Chart_01_Cell_126.png)

Shows the age structure across male and female records, helping identify broad demographic groups.

### 2. Employment categories

![Employment category counts](images/Census_Chart_02_Cell_141.png)

Explores recorded employment categories. Definitions and denominators should be checked before making labour-market comparisons.

### 3. Marital-status distribution

![Marital-status distribution](images/Census_Chart_04_Cell_148.png)

Shows the distribution of records across marital-status categories.

### 4. Age distribution

![Age distribution histogram](images/Census_Chart_09_Cell_161.png)

Highlights the spread of ages in the dataset, providing context for planning services across different life stages.

### 5. Unemployment by age

![Unemployment counts by age](images/Census_Chart_11_Cell_164.png)

Illustrates counts of records classified as unemployed by age. **These counts are not official unemployment rates.**

## Illustrative population scenarios

The public portfolio includes a **scenario exercise, not a trained or validated population forecast**. It applies:

\[
P_n = 7{,}758 \times (1+r)^n
\]

where `r` is an assumed annual population growth rate and `n` is the number of years ahead.

| Years ahead | Low (−0.5% annually) | Stable (0%) | High (+0.5% annually) |
| ---: | ---: | ---: | ---: |
| 0 | 7,758 | 7,758 | 7,758 |
| 5 | 7,566 | 7,758 | 7,954 |
| 10 | 7,379 | 7,758 | 8,155 |
| 15 | 7,196 | 7,758 | 8,361 |
| 20 | 7,018 | 7,758 | 8,572 |

The annual rates are **hypothetical**, not estimated from historical population time-series data. The original notebook's demographic proxies do not establish a validated forecasting model. Reliable service-demand projections would require longitudinal data on births, deaths, migration, local geography and service capacity, with appropriate validation.

## Tools and skills

**Python · Pandas · Jupyter Notebook · Data Cleaning · Exploratory Data Analysis · Demographic Visualisation · Scenario Modelling**

## Repository contents

| File or folder | Purpose |
| --- | --- |
| `Census_Analysis_Public.ipynb` | Privacy-preserving notebook using aggregate inputs |
| `population_by_age_gender.csv` | Aggregated population counts |
| `employment_category_summary.csv` | Aggregated employment categories |
| `marital_status_summary.csv` | Aggregated marital-status counts |
| `illustrative_population_scenarios.csv` | Hypothetical 5–20-year population scenarios |
| `images/` | Selected original coursework charts |
| `REPORT.md` | Methods, findings and limitations |
| `DATA_DICTIONARY.md` | Definitions of public data fields |
| `requirements.txt` | Python dependencies |

## Run the public notebook

Install the dependencies and launch Jupyter from the repository folder:

```bash
pip install -r requirements.txt
jupyter notebook Census_Analysis_Public.ipynb
```

The public notebook works with the **aggregated CSV files** rather than the original identifiable dataset.

## Limitations and confidentiality

The original census CSV and coursework notebook are **not included** because they contain potentially identifiable names and street addresses. The public CSV files contain aggregated counts only. The public scenario analysis is an extension created for portfolio demonstration and should not be represented as a validated model or as a result of the original coursework.

**Before publishing any extracted image**, review it for identifiable names, addresses or other sensitive content. The images shown here are intended to contain aggregate charts only.

## Future improvements

With suitable longitudinal and service-capacity data, the project could be extended to cohort-based population forecasting, out-of-sample evaluation, geographic comparisons and estimated demand for schools, housing and healthcare.
