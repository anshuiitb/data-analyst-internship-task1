# Data Analyst Internship Task 1: Data Cleaning and Preprocessing

## Dataset
- Original: marketing_campaign.csv (from Kaggle Customer Personality Analysis)
- Cleaned: cleaned_marketing_campaign.csv

## Tools Used
- Python (Pandas)

## Summary of Changes
- **Loaded and Inspected**: Dataset has 2240 rows and 29 columns; identified missing values in 'Income' (24 nulls).
- **Renamed Columns**: Standardized to lowercase with underscores (e.g., 'Year_Birth' -> 'year_birth').
- **Handled Missing Values**: Filled 24 missing 'Income' with median (~$52,247) to preserve data.
- **Removed Duplicates**: No duplicates found after checking.
- **Standardized Text**: Trimmed and title-cased 'Education' and 'Marital_Status' (e.g., mapped '2n Cycle' to 'Master').
- **Fixed Data Types/Formats**: Converted 'Dt_Customer' to datetime (format '%d-%m-%Y'); ensured 'year_birth' as int and 'income' as float.
- **Outlier and Validation**: Capped 'Income' >$200,000 (affected 3 rows); corrected any negative purchases to 0; validated 'year_birth' <=2025 and added 'age' column (flagged ages >120 as NaN).
- **Final Stats**: No remaining issues; dataset ready for analysis.

## Screenshots
- Before/after df.info() [insert images]

## Code
See cleaning_script.py for full code.
