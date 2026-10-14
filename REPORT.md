# Census Analysis — Project Report

## Objective
Describe the population's demographic composition and examine implications for community infrastructure planning.

## Data and scope
The original census CSV contained **7,758 rows and 11 fields**, including identifiable personal information. This public report uses only aggregate exports. The newer notebook `censusa(3).ipynb` was used to update the methods discussion.

## Work evidenced in the updated notebook
1. **Cleaning:** reviewed nulls, duplicate rows, age anomalies, inconsistent relationships and categorical values. Some corrections were based on household assumptions and would require independent validation in production.
2. **Demographics:** plotted age-by-gender population pyramids, age histograms and marital/religion breakdowns.
3. **Employment:** categorised occupations and calculated an unemployment proportion using the *whole population* as denominator. The notebook describes ~6.4%, but this is **not the standard unemployment rate** (which uses an economically active labour-force denominator).
4. **Housing:** explored occupancy and household usage. The notebook calculates both occupants and available rooms from row counts, making the resulting usage ratio uninformative; actual room-count data is needed.
5. **Forward-looking estimates:** used age-specific cross-sectional counts as rough proxies for birth and death patterns. The notebook itself notes that birth rates were manipulated estimates rather than directly observed vital statistics. These calculations cannot establish future population levels.

## Public scenario extension
For transparency, a separate **illustrative scenario model** was added, with formula `population_t = 7758 × (1 + annual_rate)^years`. Assumptions: -0.5%, 0%, +0.5% annual net change. These are hypothetical assumptions, not fitted rates.

| Years ahead | Low (-0.5%) | Stable (0%) | High (+0.5%) |
|---|---:|---:|---:|
| 0 | 7,758 | 7,758 | 7,758 |
| 5 | 7,566 | 7,758 | 7,954 |
| 10 | 7,379 | 7,758 | 8,155 |
| 15 | 7,196 | 7,758 | 8,361 |
| 20 | 7,018 | 7,758 | 8,572 |

## Interpretation
The census supports descriptive insights into age composition and population characteristics. Hypothetical scenario ranges help frame questions about future schools, healthcare and housing, but do not quantify how many facilities will be required.

## Recommended next iteration
Obtain several years of population estimates and observed birth/death/migration data; validate cleaning rules; build cohort-component or statistical forecasts with backtesting and uncertainty intervals; combine projected demand with actual service capacity.

## Ethical handling
Only aggregated data and a new public notebook are included. The original notebook and raw census data must remain private due to personal identifiers.
