```txt id="3qk9h2"
DESCRIPTIVE STATISTICS PRACTICAL

Aim:
To perform descriptive statistical analysis using pandas functions.

Important Terms:
1. Descriptive Statistics -> Summarizing data
2. Mean -> Average value
3. Median -> Middle value
4. Standard Deviation -> Spread of data
5. Percentile -> Position of data
6. Grouping -> Combining similar category data
7. DataFrame -> Table-like structure

Code Explanation:

import pandas as pd
Used for data analysis and dataframe operations.

data = {...}
Creates dataset containing:
- Age
- Income
- Age_Group

df = pd.DataFrame(data)
Converts dictionary into dataframe.

print(df)
Displays dataset.

df.groupby('Age_Group')
Groups records based on Age_Group.

Example:
20-30 group together
30-40 group together

df.groupby('Age_Group')['Income'].describe()
Provides statistical summary:
- count
- mean
- std
- min
- max
- quartiles

df.groupby('Age_Group')['Income'].mean()
Calculates average income.

Mean Formula:
Mean = Sum of Values / Number of Values

df.groupby('Age_Group')['Income'].median()
Calculates middle value.

df.groupby('Age_Group')['Income'].min()
Finds minimum income.

df.groupby('Age_Group')['Income'].max()
Finds maximum income.

df.groupby('Age_Group')['Income'].std()
Calculates standard deviation.

Standard deviation measures spread of data.

iris = pd.read_csv("Iris.csv")
Loads Iris dataset.

iris.head()
Displays first 5 rows.

iris.groupby('variety').describe()
Displays statistics grouped by species.

Species:
- Setosa
- Versicolor
- Virginica

iris.groupby('variety').mean()
Calculates average values.

iris.groupby('variety').median()
Calculates median values.

iris.groupby('variety').std()
Calculates standard deviation.

iris.groupby('variety').quantile([0.25,0.50,0.75])
Calculates percentiles:
0.25 -> Q1
0.50 -> Median
0.75 -> Q3

Important Viva Questions:

Q1. What is descriptive statistics?
Answer:
Methods used to summarize and describe data.

Q2. What is pandas?
Answer:
Python library used for data analysis.

Q3. What is DataFrame?
Answer:
Table-like structure with rows and columns.

Q4. What does groupby() do?
Answer:
Groups similar category data together.

Q5. Why use groupby()?
Answer:
To perform category-wise analysis.

Q6. What is mean?
Answer:
Average of values.

Q7. What is median?
Answer:
Middle value of sorted data.

Q8. What is standard deviation?
Answer:
Measure of spread of data.

Q9. What does describe() do?
Answer:
Provides statistical summary.

Q10. What does std() calculate?
Answer:
Standard deviation.

Q11. What is percentile?
Answer:
Value below which percentage of data lies.

Q12. What does quantile() do?
Answer:
Calculates percentile values.

Q13. What is 50th percentile?
Answer:
Median.

Q14. Which dataset did you use?
Answer:
Iris dataset.

Q15. Which species are present in Iris dataset?
Answer:
Setosa, Versicolor, Virginica.

Q16. What does head() do?
Answer:
Displays first 5 rows.

Q17. Difference between mean and median?
Answer:
Mean is average value.
Median is middle value.

Q18. Which measure is less affected by outliers?
Answer:
Median.

Q19. Why use descriptive statistics?
Answer:
To understand dataset before analysis.

Q20. What is grouping?
Answer:
Combining similar category data.

Simple Viva Flow:
1. Imported pandas
2. Created dataframe
3. Grouped data using Age_Group
4. Calculated mean, median, min, max and std deviation
5. Loaded Iris dataset
6. Grouped by species
7. Calculated statistical measures and percentiles

Conclusion:
This practical demonstrates descriptive statistical analysis using pandas groupby functions and statistical operations.

```
