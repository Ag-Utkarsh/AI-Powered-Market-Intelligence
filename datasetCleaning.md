# Dataset Cleaning Summary

This document describes the main cleaning and formatting steps applied to the Google Play Store dataset (`googleplaystore.csv`) in `googleStoreData.ipynb`:

- **Duplicate rows were removed** based on the 'App' column.
- **Reviews**: Converted from string to integer type for accurate analysis.
- **Price**: Converted from string (with '$' sign) to numeric (float) type.
- **Last Updated**: Converted from string to datetime format for better time series analysis.
- **Installs**: Converted from string (with ',' and '+') to integer type.

**Note:**  
- The **Size** column was not changed. Keeping values like 'M', 'K', 'G', and 'Varies with Devices' helps LLMs provide better insights and results.
- No changes were made to the **Android Version** column for the same reason.

The cleaned dataset is saved as `cleaned_googleplaystore.csv`.