```txt id="l66b8j"
=========================================
DATA WRANGLING II PRACTICAL
EXPLANATION + VIVA QUESTIONS
=========================================


-----------------------------------------
1. AIM OF PRACTICAL
-----------------------------------------

To perform data preprocessing operations such as:
- Missing value handling
- Inconsistency handling
- Outlier treatment
- Data transformation
using Python libraries.


=========================================
2. IMPORTANT TERMS
=========================================

1. Data Wrangling
Process of cleaning and transforming raw data.

2. Data Preprocessing
Preparing raw data before analysis.

3. Missing Values
Empty/null values in dataset.

4. Inconsistent Data
Incorrect or invalid data.

5. Outliers
Extreme abnormal values.

6. Mean
Average of values.

7. Quartiles
Values dividing data into four equal parts.

8. IQR
Inter Quartile Range.

9. Transformation
Changing data into suitable format.

10. Normalization
Scaling values between 0 and 1.

11. DataFrame
Table-like structure in pandas.


=========================================
3. EASY CODE EXPLANATION
=========================================


-----------------------------------------
STEP 1 : IMPORT LIBRARIES
-----------------------------------------

import pandas as pd
import numpy as np
from sklearn.preprocessing import MinMaxScaler


Explanation:

1. pandas
Used for dataframe handling.

2. numpy
Used for numerical operations.

3. MinMaxScaler
Used for normalization.


-----------------------------------------
STEP 2 : CREATE DATASET
-----------------------------------------

data = {
    'Name':['A','B','C'],
    ...
}

Explanation:
Dictionary containing:
- Name
- Age
- Marks
- Attendance
- Grade


-----------------------------------------
STEP 3 : CREATE DATAFRAME
-----------------------------------------

df = pd.DataFrame(data)

Explanation:

DataFrame
Converts dictionary into table format.


-----------------------------------------
STEP 4 : DISPLAY INITIAL DATASET
-----------------------------------------

print(df)

Explanation:
Displays original dataset.


-----------------------------------------
STEP 5 : CHECK MISSING VALUES
-----------------------------------------

print(df.isnull().sum())

Explanation:

isnull()
Checks missing values.

sum()
Counts total missing values.


Missing values present in:
- Age
- Marks
- Attendance


-----------------------------------------
STEP 6 : HANDLE MISSING VALUES
-----------------------------------------

df['Age'] = df['Age'].fillna(df['Age'].mean())

Explanation:

fillna()
Replaces missing values.

mean()
Calculates average value.

Missing Age values replaced using average.


-----------------------------------------
STEP 7 : HANDLE MARKS MISSING VALUES
-----------------------------------------

df['Marks'] = df['Marks'].fillna(df['Marks'].mean())

Explanation:
Missing Marks values replaced using mean.


-----------------------------------------
STEP 8 : HANDLE ATTENDANCE MISSING VALUES
-----------------------------------------

df['Attendance'] = df['Attendance'].fillna(df['Attendance'].mean())

Explanation:
Missing Attendance values replaced using mean.


-----------------------------------------
MEAN FORMULA
-----------------------------------------

Mean = Sum of Values / Number of Values


-----------------------------------------
WHY MEAN IS USED
-----------------------------------------

Because it preserves overall data distribution.


-----------------------------------------
STEP 9 : HANDLE INCONSISTENT DATA
-----------------------------------------

df['Grade'] = df['Grade'].replace('Z', 'B')

Explanation:

replace()
Replaces invalid values.

Here:
Z is invalid grade.

It is replaced with B.


-----------------------------------------
WHAT IS INCONSISTENT DATA
-----------------------------------------

Incorrect or invalid data.

Examples:
- Wrong spellings
- Invalid grades
- Incorrect formats


-----------------------------------------
STEP 10 : FIND QUARTILES
-----------------------------------------

Q1 = df['Marks'].quantile(0.25)
Q3 = df['Marks'].quantile(0.75)

Explanation:

Q1
25th percentile.

Q3
75th percentile.


-----------------------------------------
STEP 11 : FIND IQR
-----------------------------------------

IQR = Q3 - Q1

Explanation:

IQR
Inter Quartile Range.

Used for outlier detection.


-----------------------------------------
IQR FORMULA
-----------------------------------------

IQR = Q3 - Q1


-----------------------------------------
STEP 12 : CALCULATE LOWER AND UPPER LIMITS
-----------------------------------------

lower = Q1 - 1.5 * IQR
upper = Q3 + 1.5 * IQR

Explanation:

Values outside these limits are considered outliers.


-----------------------------------------
STEP 13 : HANDLE OUTLIERS
-----------------------------------------

df['Marks'] = np.where(df['Marks'] > upper, upper, df['Marks'])

Explanation:

np.where(condition, true, false)

If Marks > upper limit:
replace with upper limit.

Otherwise:
keep original value.


-----------------------------------------
STEP 14 : HANDLE LOWER OUTLIERS
-----------------------------------------

df['Marks'] = np.where(df['Marks'] < lower, lower, df['Marks'])

Explanation:
Values smaller than lower limit replaced.


-----------------------------------------
WHICH VALUE IS OUTLIER
-----------------------------------------

500

Because it is extremely larger than other values.


-----------------------------------------
STEP 15 : DATA TRANSFORMATION
-----------------------------------------

scaler = MinMaxScaler()

Explanation:
Creates normalization object.


-----------------------------------------
STEP 16 : APPLY NORMALIZATION
-----------------------------------------

df['Scaled_Attendance'] = scaler.fit_transform(
    df[['Attendance']]
)

Explanation:

fit()
Learns minimum and maximum values.

transform()
Scales values between 0 and 1.

fit_transform()
Performs both together.


-----------------------------------------
NORMALIZATION FORMULA
-----------------------------------------

x' = (x - xmin) / (xmax - xmin)


-----------------------------------------
WHY DOUBLE SQUARE BRACKETS
-----------------------------------------

df[['Attendance']]

Because fit_transform() expects 2D input.


-----------------------------------------
STEP 17 : DISPLAY FINAL DATASET
-----------------------------------------

print(df)

Explanation:
Displays transformed dataset.


-----------------------------------------
STEP 18 : FINAL DATASET INFORMATION
-----------------------------------------

print(df.info())

Explanation:

info()
Displays:
- Datatypes
- Non-null values
- Memory usage


=========================================
4. IMPORTANT VIVA QUESTIONS
=========================================


Q1. What is Data Wrangling?

Answer:
Process of cleaning and transforming raw data.


Q2. What preprocessing steps did you perform?

Answer:
- Missing value handling
- Inconsistency handling
- Outlier treatment
- Normalization


Q3. What are missing values?

Answer:
Empty or null values in dataset.


Q4. Which function checks missing values?

Answer:
isnull()


Q5. What does fillna() do?

Answer:
Replaces missing values.


Q6. Why use mean for missing values?

Answer:
Because it preserves overall data distribution.


Q7. What is inconsistent data?

Answer:
Incorrect or invalid data.


Q8. Which inconsistent value existed?

Answer:
Grade Z.


Q9. How did you fix inconsistency?

Answer:
Using replace() function.


Q10. What are outliers?

Answer:
Extreme abnormal values.


Q11. Which value was outlier?

Answer:
Marks = 500


Q12. Which method did you use for outlier detection?

Answer:
IQR method.


Q13. What is IQR?

Answer:
Inter Quartile Range.


Q14. Formula of IQR?

Answer:
IQR = Q3 - Q1


Q15. Why handle outliers?

Answer:
To improve analysis accuracy.


Q16. What is normalization?

Answer:
Scaling values between 0 and 1.


Q17. Which normalization technique did you use?

Answer:
Min-Max Normalization.


Q18. What is MinMaxScaler?

Answer:
Scikit-learn class used for normalization.


Q19. Why normalization is important?

Answer:
To balance feature scales.


Q20. What does np.where() do?

Answer:
Performs conditional replacement.


Q21. What is transformation?

Answer:
Changing data into suitable format.


Q22. What is DataFrame?

Answer:
Table-like structure with rows and columns.


Q23. What does info() display?

Answer:
- Datatypes
- Non-null values
- Memory usage


Q24. What does quantile() do?

Answer:
Calculates percentile values.


Q25. What are quartiles?

Answer:
Values dividing data into four equal parts.


Q26. What is the purpose of lower and upper limits?

Answer:
To detect outliers.


Q27. What is data cleaning?

Answer:
Removing errors and inconsistencies.


Q28. What is numpy?

Answer:
Python library for numerical operations.


Q29. What is pandas?

Answer:
Python library for data analysis.


Q30. Why use double square brackets in scaler?

Answer:
Because scaler requires 2D input.


=========================================
5. MOST EXPECTED EXAMINER QUESTIONS
=========================================

Q. Why is 500 considered outlier?

Answer:
Because it is extremely far from other Marks values.


Q. Why use IQR method?

Answer:
Because it is simple and effective for outlier detection.


Q. Why replace outliers instead of deleting rows?

Answer:
To avoid losing useful information.


Q. Why normalize attendance column?

Answer:
To scale values into fixed range.


Q. What happens if missing values are not handled?

Answer:
Analysis and machine learning models may give incorrect results.


=========================================
6. SIMPLE FLOW TO EXPLAIN IN VIVA
=========================================

1. Imported libraries
2. Created dataframe
3. Checked missing values
4. Filled missing values using mean
5. Corrected inconsistent values
6. Detected outliers using IQR
7. Treated outliers using np.where()
8. Applied Min-Max normalization
9. Displayed final dataset information


=========================================
7. ONE LINE CONCLUSION
=========================================

This practical demonstrates data preprocessing techniques including missing value handling, inconsistency correction, outlier treatment and normalization using pandas, numpy and sklearn.

```
