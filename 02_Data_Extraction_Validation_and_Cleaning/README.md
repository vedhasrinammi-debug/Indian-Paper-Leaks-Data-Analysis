# Stage 2 — Data Extraction, Validation & Cleaning

## Purpose

Extract the information required for the project analysis, identify common data-quality issues, and apply only the necessary cleaning steps to prepare the dataset for later stages.

**Notebook:** [Data_Extraction_Validation_Cleaning.ipynb](Data_Extraction_Validation_Cleaning.ipynb)

## Required checks

**Extraction**
- Extract selected fields such as incident location, exam name, era and conducting body.
- Summarize incidents by location, and find locations with incidents in both the UPA and NDA eras.
- Identify locations with more than one conducting body and All India level incidents.
- Extract incidents by confidence level and by Central and State conducting bodies.
- Extract incidents with recorded arrests, convictions and other legal action.

**Validation**
- Check for missing values and calculate missing-value percentages.
- Check for duplicate records and duplicate Incident IDs.
- Validate the Incident ID format and date values, including the expected date range.
- Validate categorical values (era, body type, leak status and confidence).
- Check for blank text values and unnecessary leading or trailing spaces.
- Check numerical columns for negative values and for records where convictions are greater than arrests.
- Validate linked-death notes and source information (source names and URLs).

**Cleaning**
- Remove duplicate records.
- Remove leading and trailing spaces from text and categorical columns.
- Standardize the spacing in the `action_taken` field.
- Convert the `date` column to a datetime type and the numerical columns to numeric types.
- Preserve missing values where the source does not report information instead of automatically replacing them with zero.
- Flag records that need source-level verification instead of changing them automatically.
- Re-run the validation checks on the cleaned dataset.

**Important:** The original dataset is kept separate from the cleaned dataset. Cleaning is performed on a copy and only where a data-quality issue is identified.

## Input and Output

- **Input:** `data/paper_leaks.csv` (110 records, 18 columns), uploaded in Google Colab when the notebook runs.
- **Output:** The validated and cleaned dataset, saved as `paper_leaks_cleaned.csv`. It is used by the aggregation, analysis and visualization stages of the project.
