# Superstore_data_cleaning

## GOAL:
To clean the dataset for ease in data analysis and satisfying business requirements

### Data Cleaning Notes:
Pre-processing the dataset entails handling null values, deleting or transforming irrelevant values, changing the data type, getting rid of duplicates, and validating the data. You will receive a streamlined and cleaner data collection for future analysis once you have finished this task.


Data pre-processing procedures:

* Step 1: Eliminating duplicate rows (except for the Row ID column, multiple rows may exist).

* Step 2: Rows with a small number of missing values are removed in step two.

* Step 3: If necessary, delete any irrelevant data from each column. verification of every value in a column ( order date and ship date value must be in correct date format ). Ship date >= order date for each entry in the dataset

* Step 4: Export the cleaned dataset as a.csv file in step 4 using your preferred UTF-8 encoding.


### Notes: Pandas used, basics overview

* Check the overview of the dataset first
.describe - checks the mean,std etc of the dataset
.info() - will check the datatype of the columns (Change the ones thats incorrect)
* check missing values
.isna()- check number of missing value in boolean format
.isna.sum()-check number of missing value can sum the number of missing values
* check for empty rows
#to remove empty rows
df1.dropna(inplace = True)                      # Remove rows with NaN
#convert the 'Date' column to datetime format
df['Date']= pd.to_datetime(df['Date'])
