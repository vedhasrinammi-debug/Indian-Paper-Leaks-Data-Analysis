# Stage 1 — Data Loading & Reading

## Purpose

Load the India Paper Leaks dataset and understand its basic structure before further extraction, validation, cleaning and analysis.

**Notebook:** [Data_Loading_and_Reading.ipynb](Data_Loading_and_Reading.ipynb)

## Required checks

- Load the `paper_leaks.csv` dataset using Pandas.
- Display the first five and last five records.
- Check the number of rows and columns.
- Display the column names.
- Check the data types of all columns.
- Inspect the dataset information using `df.info()`.
- Generate basic descriptive statistics.
- Explore important categorical fields such as leak status, conducting body type, era and confidence.
- Select the columns required for the project analysis.
- Filter cases by leak status, conducting body type, era and confidence level.
- Identify records containing arrest and conviction information.

**Important:** The notebook uses the actual dataset loaded from the CSV file. The row and column counts are obtained from the loaded data rather than being hard-coded.

## Input and Output

- **Input:** `data/paper_leaks.csv` (110 records, 18 columns), uploaded in Google Colab when the notebook runs.
- **Output:** A Pandas DataFrame with its structure inspected (shape, columns, data types and summary statistics), and filtered subsets of records by leak status, conducting body type, era, confidence, and reported arrests and convictions. No file is saved in this stage.
