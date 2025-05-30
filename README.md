This project focuses on cleaning a dataset containing information about worldwide layoffs. The data was originally raw and unstandardized, and the goal was to prepare it for future analysis or visualization by applying fundamental data cleaning steps using SQL.

Project Steps:
1. Removing Duplicates
A temporary staging table was created to avoid affecting the original dataset.

Used the ROW_NUMBER() window function to identify duplicate records based on multiple relevant columns (company, location, industry, total_laid_off, etc.).

Removed duplicate rows to ensure accuracy and avoid skewed analysis.

2. Standardizing the Data
Trimmed whitespace from text fields such as company and country.

Unified similar category values (e.g., different forms of “Crypto” in the industry column were standardized to “Crypto”).

Cleaned country names by removing unwanted characters like trailing periods.

3. Handling Null and Blank Values
Replaced empty strings with NULL to ensure consistent handling of missing data.

Filled missing industry values by matching company names where the industry was available for the same company in other rows.

Removed rows where both total_laid_off and percentage_laid_off were missing, as they did not contribute useful information.

4. Removing Irrelevant Columns
Dropped the row_num column used for duplicate tracking once cleanup was complete.

Skills Demonstrated:

-Data profiling and duplicate identification

-Data standardization and formatting

-Null handling and imputation

-SQL table creation, modification, and cleanup

-Use of CTEs and subqueries

This project showcases my ability to work with raw datasets and prepare them for analysis through structured data cleaning techniques using SQL. It reflects a critical step in the data analytics workflow — turning messy data into reliable, usable information.
