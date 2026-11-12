# Stage 4 — Data Visualization, Results & Interpretation

## Purpose

Present the findings of the project through charts and clear results, and interpret what the recorded paper leak data shows.

**Notebook:** [Data_Visualization_Results_Interpretation.ipynb](Data_Visualization_Results_Interpretation.ipynb)

## Required checks

**Visualization (Matplotlib)**
- Load the cleaned dataset and create a `year` column from the `date` column.
- Line chart: paper leak cases by year.
- Horizontal bar charts: top 10 areas and top 10 exams with the most cases.
- Pie chart: distribution of cases by leak status.
- Bar chart: cases by era (UPA and NDA).
- Scatter plot: relationship between arrests and convictions.

**Results and interpretation**
- Find the year, area and exam with the most paper leak cases.
- Find the most common leak status.
- Compare the number of cases in the UPA and NDA eras.
- Calculate the correlation between arrests and convictions and interpret what it shows.

**Important:** The results describe the recorded incidents in this dataset, not every paper leak in India. Missing values are not counted as zero, so the arrests and convictions chart and correlation include only incidents that report both values, and they should be interpreted with care.

## Input and Output

- **Input:** The cleaned dataset from Stage 2, `data/paper_leaks_cleaned.csv`, uploaded in Google Colab when the notebook runs.
- **Output:** Six charts and the printed results, shown in the notebook. The chart images are stored in [`output/figures`](../output/figures):
  - `paper_leak_cases_by_year.png`
  - `top_10_areas.png`
  - `top_10_exams.png`
  - `leak_status_distribution.png`
  - `paper_leak_cases_by_era.png`
  - `arrests_vs_convictions.png`
