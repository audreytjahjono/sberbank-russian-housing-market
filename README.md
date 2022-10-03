# Russian House Market 

For the cleaning data exercise, I'm using the [Russian housing market](https://www.kaggle.com/c/sberbank-russian-housing-market/data) dataset from Kaggle.
The goal of the exercise is to predict housing prices.
```python:
df = pd.read_csv('train.csv')

df.info(verbose=True)

df.head()
```
First, I am looking at the data in Python. I learned that the dataset has 30,471 rows and 292 columns from the results. 
```python:
numerics_col = df.select_dtypes(include=['number']).columns
print(numerics_col)

non_numerics_col = df.select_dtypes(exclude=['number']).columns
print(non_numerics_col)
```

I, then, identify the numeric and non-numeric columns. These are necessary since we often treat them using different methods.
Now I can go through the ‘dirty’ data types checklist and fix them!

## Cleaning - Missing Data
Here are some of the things I did to check for missing data and clean the missing data:

:arrow_right: Checking missing data using counts and percentage

:arrow_right: Checking missing data with heatmap

:arrow_right: Checking missing data (by rows) with histogram

:arrow_right: Cleaning the missing data : drop column with over 30% missing data and drop row to only keep with less than 35 missing columns.

:arrow_right: Cleaning the missing data : by imputing constant value and statistics value

## Cleaning - Irregular data (outliers)
Here are the steps I did to identify/spot outliers in numeric columns:

:arrow_right: Detect potential outliers

:arrow_right: Look at the column’s common descriptive statistics

:arrow_right: Use histogram in the data visualization method to detect outliers

:arrow_right: Use boxplot in the data visualization method to detect outliers

## Cleaning - Unnecessary Data
Here are the steps I did to clean or fix unnecessary data:

:arrow_right: Check for repetitive & uninformative value and show columns with over 99.9% rows being the same value

:arrow_right: Check for duplicates value in rows and columns

:arrow_right: Drop the duplicate value

:arrow_right: Cleaning capitalization because python is case sensitive

:arrow_right: Cleaning inconsistent data types

:arrow_right: Set criteria to convert these typos to the correct values.

