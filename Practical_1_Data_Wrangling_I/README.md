===============================
DATA WRANGLING PRACTICAL
IRIS DATASET
EXPLANATION + VIVA QUESTIONS
===============================


-----------------------------------
1. AIM OF PRACTICAL
-----------------------------------

To perform data preprocessing and data wrangling operations on the Iris Dataset using Python libraries like Pandas, NumPy and Scikit-Learn.


-----------------------------------
2. IMPORTANT TERMS
-----------------------------------

1. Dataset
Collection of data arranged in rows and columns.

2. Data Wrangling
Process of cleaning and transforming raw data.

3. Data Preprocessing
Preparing raw data before analysis or machine learning.

4. DataFrame
Table-like structure in Pandas.

5. Normalization
Scaling values between 0 and 1.

6. Categorical Data
Data represented using labels/text.

Example:
Setosa, Virginica

7. Numerical Data
Data represented using numbers.

Example:
5.1, 3.4

8. Duplicate Data
Repeated rows in dataset.

9. Missing Values
Empty/null values in dataset.

10. Encoding
Converting categorical values into numbers.


===================================
3. EASY CODE EXPLANATION
===================================


-----------------------------------
STEP 1 : IMPORT LIBRARIES
-----------------------------------

import pandas as pd
import numpy as np
from sklearn.preprocessing import MinMaxScaler


Explanation:

1. pandas
Used for data handling and dataframe operations.

2. numpy
Used for numerical operations.

3. MinMaxScaler
Used for normalization.


-----------------------------------
STEP 2 : PRINT DATASET DETAILS
-----------------------------------

print("Dataset Name : Iris Dataset")

Explanation:
Displays dataset information.


-----------------------------------
STEP 3 : DATASET DESCRIPTION
-----------------------------------

print("The Iris dataset contains measurements...")

Explanation:
Explains what the dataset contains:
- Sepal Length
- Sepal Width
- Petal Length
- Petal Width
- Flower Species


-----------------------------------
STEP 4 : LOAD DATASET
-----------------------------------

df = pd.read_csv("Iris.csv")

Explanation:

read_csv()
Used to read CSV file.

df
Variable storing dataframe.


-----------------------------------
STEP 5 : DISPLAY FIRST 5 ROWS
-----------------------------------

print(df.head())

Explanation:

head()
Displays first 5 rows.


-----------------------------------
STEP 6 : DISPLAY LAST 5 ROWS
-----------------------------------

print(df.tail())

Explanation:

tail()
Displays last 5 rows.


-----------------------------------
STEP 7 : SHAPE OF DATASET
-----------------------------------

print(df.shape)

Explanation:

shape
Returns:
(Number of Rows, Number of Columns)

Example:
(150,5)


-----------------------------------
STEP 8 : COLUMN NAMES
-----------------------------------

print(df.columns)

Explanation:
Displays all column names.


-----------------------------------
STEP 9 : CHECK MISSING VALUES
-----------------------------------

print(df.isnull().sum())

Explanation:

isnull()
Checks missing values.

sum()
Counts total missing values.


-----------------------------------
STEP 10 : CHECK DUPLICATE ROWS
-----------------------------------

print(df.duplicated().sum())

Explanation:

duplicated()
Checks repeated rows.


-----------------------------------
STEP 11 : REMOVE DUPLICATES
-----------------------------------

df = df.drop_duplicates()

Explanation:

drop_duplicates()
Removes duplicate rows.


-----------------------------------
STEP 12 : STATISTICAL SUMMARY
-----------------------------------

print(df.describe())

Explanation:

describe()
Provides statistical information:
- Mean
- Minimum
- Maximum
- Standard Deviation
- Quartiles


-----------------------------------
STEP 13 : DATASET INFORMATION
-----------------------------------

print(df.info())

Explanation:

info()
Displays:
- Column names
- Datatypes
- Non-null values


-----------------------------------
STEP 14 : VARIABLE DESCRIPTION
-----------------------------------

print("sepal.length -> Numeric")

Explanation:
Explains datatype and meaning of variables.


-----------------------------------
STEP 15 : CHECK DATATYPES
-----------------------------------

print(df.dtypes)

Explanation:

dtypes
Displays datatype of each column.


-----------------------------------
STEP 16 : NORMALIZATION
-----------------------------------

scaler = MinMaxScaler()

Explanation:
Creates normalization object.


-----------------------------------
STEP 17 : APPLY NORMALIZATION
-----------------------------------

scaler.fit_transform()

Explanation:

fit()
Learns minimum and maximum values.

transform()
Scales values between 0 and 1.

fit_transform()
Performs both together.


Normalization Formula:

x' = (x - xmin) / (xmax - xmin)


-----------------------------------
WHY NORMALIZATION IS USED
-----------------------------------

Because different columns may have different ranges.

Example:
One column:
1 to 1000

Another column:
1 to 10

Large values dominate calculations.

Normalization balances them.


-----------------------------------
STEP 18 : DISPLAY NORMALIZED DATA
-----------------------------------

print(df.head())

Explanation:
Displays normalized dataset.


-----------------------------------
STEP 19 : CONVERT CATEGORICAL TO NUMERIC
-----------------------------------

df['variety'] = df['variety'].map({
    'Setosa':0,
    'Versicolor':1,
    'Virginica':2
})

Explanation:

map()
Converts text labels into numbers.

Setosa -> 0
Versicolor -> 1
Virginica -> 2


-----------------------------------
WHY CONVERT CATEGORICAL DATA
-----------------------------------

Machine learning algorithms work with numerical data only.


-----------------------------------
STEP 20 : FINAL DATASET INFO
-----------------------------------

print(df.info())

Explanation:
Displays final cleaned dataset information.


===================================
4. IMPORTANT VIVA QUESTIONS
===================================


Q1. What is Data Wrangling?

Answer:
Process of cleaning and transforming raw data.


Q2. What is Data Preprocessing?

Answer:
Preparing data before analysis or machine learning.


Q3. What is Pandas?

Answer:
Python library used for data analysis.


Q4. What is NumPy?

Answer:
Python library used for numerical operations.


Q5. What is a DataFrame?

Answer:
Table-like data structure with rows and columns.


Q6. Which dataset did you use?

Answer:
Iris Dataset.


Q7. What features exist in Iris Dataset?

Answer:
- Sepal Length
- Sepal Width
- Petal Length
- Petal Width
- Variety


Q8. What are missing values?

Answer:
Empty or null values in dataset.


Q9. Which function checks missing values?

Answer:
isnull()


Q10. What does duplicated() do?

Answer:
Checks duplicate rows.


Q11. What does drop_duplicates() do?

Answer:
Removes duplicate rows.


Q12. What does head() do?

Answer:
Displays first 5 rows.


Q13. What does tail() do?

Answer:
Displays last 5 rows.


Q14. What does shape return?

Answer:
Number of rows and columns.


Q15. What does describe() do?

Answer:
Provides statistical summary.


Q16. What does info() display?

Answer:
- Datatypes
- Non-null values
- Memory usage


Q17. What is normalization?

Answer:
Scaling values between 0 and 1.


Q18. Which normalization technique did you use?

Answer:
Min-Max Normalization.


Q19. What is MinMaxScaler?

Answer:
Scikit-learn class used for normalization.


Q20. Why normalization is important?

Answer:
To balance feature scales.


Q21. What is categorical data?

Answer:
Data represented using labels/text.


Q22. Why convert categorical data into numeric?

Answer:
Machine learning algorithms require numerical input.


Q23. Which method did you use for encoding?

Answer:
Label Encoding using map().


Q24. What does fit_transform() do?

Answer:
Learns and transforms data together.


Q25. Which library provides MinMaxScaler?

Answer:
sklearn.preprocessing


Q26. What are duplicate records?

Answer:
Repeated rows in dataset.


Q27. What is data cleaning?

Answer:
Removing errors and inconsistencies from data.


Q28. What is CSV?

Answer:
Comma Separated Values file.


Q29. What is object datatype?

Answer:
Datatype used for text/string values.


Q30. What is float datatype?

Answer:
Datatype used for decimal values.


===================================
5. MOST EXPECTED EXAMINER QUESTIONS
===================================

Q. Why did you choose Iris dataset?

Answer:
Because it is simple and commonly used for machine learning practice.


Q. Why normalization is necessary?

Answer:
Because different features may have different ranges.


Q. What happens if normalization is not done?

Answer:
Large-value features dominate calculations.


Q. Why remove duplicate rows?

Answer:
To avoid repeated data affecting analysis.


Q. Can machine learning work directly on strings?

Answer:
No, categorical values must be converted into numbers.


===================================
6. SIMPLE FLOW TO EXPLAIN IN VIVA
===================================

1. Imported libraries
2. Loaded Iris dataset
3. Displayed dataset
4. Checked shape and columns
5. Checked missing values
6. Checked duplicates
7. Removed duplicates
8. Viewed statistics
9. Checked datatypes
10. Applied normalization
11. Converted categorical values into numeric
12. Displayed final dataset


===================================
7. ONE LINE CONCLUSION
===================================

This practical demonstrates data preprocessing techniques such as duplicate removal, normalization and categorical encoding using the Iris dataset.
