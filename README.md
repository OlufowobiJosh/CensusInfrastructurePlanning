# Census Population Analysis & Community Planning

**Python | Pandas | Exploratory Data Analysis | Demographic Scenarios**

## Business problem
A local council needs to understand the demographic profile of a community and explore how future population change could affect demand for housing, schools and health services.

## Project background
This portfolio project is based on my updated university Jupyter notebook, `censusa(3).ipynb`, which explored data cleaning, duplicate records, inconsistent demographic entries, age/gender structure, household occupancy, employment, marital status, religion, and approximate birth/death indicators. The original dataset contained **7,758 individual records**.

## What I did
- Inspected missing values, duplicates and age-related inconsistencies.
- Explored age and gender distributions and created age bands.
- Examined employment categories, marital status and household occupancy.
- Investigated proxy birth and mortality estimates in the updated coursework.
- Created a **separate public scenario analysis** for 5, 10, 15 and 20 years ahead using explicit annual growth assumptions (-0.5%, 0%, +0.5%).

## Dashboard / analysis
Open [`Census_Analysis_Public.ipynb`](Census_Analysis_Public.ipynb) for charts and scenario tables.

## Repository files
- `Census_Analysis_Public.ipynb`: runnable notebook using aggregate data.
- `population_by_age_gender.csv`: grouped population counts.
- `employment_category_summary.csv`: grouped employment categories.
- `marital_status_summary.csv`: grouped marital-status counts.
- `illustrative_population_scenarios.csv`: hypothetical growth-rate scenarios.
- `REPORT.md`: methods, findings and limitations.
- `DATA_DICTIONARY.md`: column definitions.
- `requirements.txt`: Python dependencies.

## Important limitations
**This is not a validated population forecasting model.** The updated original notebook estimated demographic proxies from a single census snapshot, rather than a measured time series. The public scenario projections are newly created, hypothetical and should not be represented as the original notebook's results. A reliable forecast would need longitudinal population, births, deaths and migration data.

## Privacy
The original census CSV and notebook include identifiable names and street addresses and are intentionally **not uploaded**. Public CSV files contain aggregated counts only. The project is a privacy-preserving portfolio recreation, not a release of the source data.

## How to run
```bash
pip install -r requirements.txt
jupyter notebook Census_Analysis_Public.ipynb
```
