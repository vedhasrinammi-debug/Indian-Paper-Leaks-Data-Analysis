# Stage 3 — Data Aggregation, Representation & Analysis

## Purpose

Summarize the cleaned dataset using Pandas and answer the project's analysis questions about paper leak trends, areas, exams, eras, affected aspirants and legal action.

**Notebook:** [Data_Aggregation_Representation_Analysis.ipynb](Data_Aggregation_Representation_Analysis.ipynb)

## Required checks

**Aggregation and representation**
- Load the cleaned dataset and create a `year` column from the `date` column.
- Count paper leak cases by year, era, area and leak status.
- Calculate the yearly totals of affected aspirants, arrests and convictions.
- Create an overall impact summary: total cases, affected aspirants, arrests, convictions and linked deaths.

**Analysis**
- Find the year, area and exam with the highest number of paper leak cases.
- Compare the UPA and NDA eras by number of cases, affected aspirants, arrests and convictions.
- Find the year with the highest number of affected aspirants.
- Calculate the correlation between arrests and convictions.
- Study how the number of cases changed over the years.

**Pandas operations used:** `groupby()`, `agg()`, `size()`, `sum()`, `sort_values()`, `idxmax()` and `corr()`.

**Important:** Totals are calculated only from values reported in the data. Missing values are not counted as zero, so the correlation between arrests and convictions should be read with care, since few incidents report both values.

## Input and Output

- **Input:** The cleaned dataset from Stage 2, `data/paper_leaks_cleaned.csv`, uploaded in Google Colab when the notebook runs.
- **Output:** Summary tables (cases by year, era, area and leak status, yearly impact and legal action totals, and the overall impact summary) and the analysis results used by the visualization stage. No file is saved in this stage.
