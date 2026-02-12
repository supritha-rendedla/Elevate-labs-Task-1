Data Cleaning and Preprocessing - Task 1
Internship: Elevate Data Analyst Internship 
Organization: Alabs in collaboration with MSME 
Project Objective
The goal of this task was to clean and prepare the raw "Marketing Campaign" dataset to make it ready for analysis. This involved handling missing values, removing duplicates, and ensuring all data formats were consistent.
Tools Used
Language: Python 
Library: Pandas 
Platform: Google Colab / Jupyter Notebook 
Steps Performed
1. Renaming Column Headers 
Action: Converted all column names to lowercase and replaced spaces with underscores (e.g., Year_Birth became year_birth).
Reason: To ensure a clean and uniform naming convention across the dataset.
2. Standardizing Text Values 
Action: Applied .str.strip() to remove accidental white spaces and .str.title() for uniform casing.
Specific Fix: In the marital_status column, I consolidated inconsistent categories like 'Alone', 'Absurd', and 'Yolo' into the standard category 'Single'
3. Handling Missing Values 
Action: Identified missing values using the isnull() function.
Result: Found 24 missing entries in the income column and filled them with the median value to maintain data integrity without losing records.
4. Converting Date Formats 
Action: Converted the dt_customer column from a string to a proper datetime object.
Result: Standardized all dates to a consistent dd-mm-yyyy format.
5. Fixing Data Types & Outliers 
Action: Created a new age column by subtracting year_birth from the current year.
Data Type: Explicitly converted age to an integer (int).
Outliers: Removed records where the age was realistically impossible (e.g., over 100 years) to ensure better data quality for future modeling.
6. Removing Duplicates 
Action: Used the drop_duplicates() function to scan and remove any redundant rows from the dataset.
Conclusion
By performing these preprocessing steps, the dataset was transformed from a raw, inconsistent format into a structured, clean CSV file. It is now ready for exploratory data analysis (EDA) or machine learning.
