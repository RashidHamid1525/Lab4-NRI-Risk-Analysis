# Lab4-NRI-Risk-Analysis
## Evaluating Bias in FEMA’s National Risk Index: Iowa & Oklahoma Risk Analysis

## Project Overview
This project analyzes natural disaster risk in **Iowa and Oklahoma** using data from FEMA’s National Risk Index (NRI). The goal is to compare the official NRI risk calculation with a custom-defined risk metric to determine if any **categorical bias** exists in how risk is assessed.

The analysis focuses on two hazards:
- Tornadoes
- Wildfires

---

## Objective
- Understand how FEMA defines and calculates risk
- Develop an alternative risk model using selected hazard variables
- Compare results between the NRI method and the custom model
- Evaluate how different definitions of risk impact communities

---

## Data Sources
- FEMA National Risk Index (NRI): https://hazards.fema.gov/nri/data-resources  
- CDC/ATSDR Social Vulnerability Index (SVI):  
  https://www.atsdr.cdc.gov/place-health/php/svi/svi-data-documentation-download.html  

---

## Plan of Action

### NRI Risk Definition
The NRI defines risk as a combination of:
- Expected Annual Loss (EAL)
- Social Vulnerability
- Community Resilience

These are combined into a percentile-based risk score across all U.S. census tracts.

---

### Custom Risk Definition
We defined risk using only hazard-based variables:

- Tornado Frequency (`TRND_AFREQ`)
- Wildfire Frequency (`WFIR_AFREQ`)

Custom Risk Formula:

my_risk = TRND_AFREQ × WFIR_AFREQ
This approach focuses on hazard probability and impact without including social or resilience factors.

---

## Project Workflow
1. Download NRI and SVI datasets
2. Clean and organize data for Iowa and Oklahoma
3. Handle missing values
4. Create a shared key (`STCNTY`) for merging datasets
5. Merge datasets into one 
6. Calculate custom risk values
7. Generate summary tables and visualizations
8. Create maps using GeoPandas

---

## Results & Insights
- The NRI assigns higher risk to areas with greater social vulnerability
- The custom model highlights areas with higher hazard frequency and impact
- Differences between models suggest potential bias in how risk is categorized
- These differences can influence funding, planning, and disaster response decisions

---


## Technologies Used
- Python
- Pandas
- GeoPandas
- Matplotlib
- Jupyter Notebook

---

## How to Run
1. Clone the repository
2. Install required libraries: pip install pandas geopandas matplotlib
3. Open the notebook or Python file and run all cells

---

## Deliverables
- Cleaned datasets
- Python code file
- Annotated code document
- Scope of Work
- Gantt chart
- Engineering timesheet
- Written summary report

