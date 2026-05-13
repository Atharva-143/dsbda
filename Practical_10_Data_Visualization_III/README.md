```txt id="2k7n5v"
DATA VISUALIZATION PRACTICAL
IRIS DATASET ANALYSIS

Aim:
To perform visualization and outlier analysis on Iris dataset using Matplotlib and Seaborn.

Important Terms:
1. Histogram -> Distribution graph
2. Boxplot -> Detects spread and outliers
3. Violin Plot -> Distribution and density graph
4. Outlier -> Extreme abnormal value
5. Mean -> Average value
6. Median -> Middle value
7. Standard Deviation -> Spread of data
8. IQR -> Inter Quartile Range
9. Distribution -> Spread pattern of data

Code Explanation:

import pandas as pd
Used for dataframe handling.

import matplotlib.pyplot as plt
Used for plotting graphs.

import seaborn as sns
Used for statistical visualization.

df = pd.read_csv("Iris.csv")
Loads Iris dataset.

df.head()
Displays first 5 rows.

df.dtypes
Displays datatype of each feature.

plt.figure(figsize=(12,8))
Creates figure with specified size.

for i, column in enumerate(df.columns[:-1])
Loops through all features except target column.

[:-1]
Excludes variety column.

plt.subplot(2,2,i+1)
Creates subplot arrangement.

plt.hist(df[column], bins=10, edgecolor='black')
Creates histogram.

Histogram:
Shows distribution of data.

bins=10
Divides data into 10 intervals.

edgecolor='black'
Adds black border to bars.

plt.title()
Adds graph title.

plt.xlabel()
Adds x-axis label.

plt.ylabel()
Adds y-axis label.

plt.tight_layout()
Adjusts spacing automatically.

plt.show()
Displays graph.

sns.boxplot(x=df[column], color='salmon')
Creates boxplot.

Boxplot shows:
- median
- quartiles
- outliers

color='salmon'
Applies salmon color.

Q1 = df[column].quantile(0.25)
Calculates first quartile.

Q3 = df[column].quantile(0.75)
Calculates third quartile.

IQR = Q3 - Q1
Calculates Inter Quartile Range.

IQR Formula:
IQR = Q3 - Q1

lower_bound = Q1 - 1.5 * IQR
Calculates lower limit.

upper_bound = Q3 + 1.5 * IQR
Calculates upper limit.

Values outside limits are outliers.

outliers = df[(df[column] < lower_bound) | (df[column] > upper_bound)]
Detects outliers.

df[column].mean()
Calculates average value.

df[column].median()
Calculates middle value.

df[column].std()
Calculates standard deviation.

sns.violinplot(x='variety', y=column, hue='variety', data=df)
Creates violin plot.

Violin plot shows:
- distribution
- density
- spread

palette='Set2'
Applies color theme.

legend=False
Hides legend.

Important Viva Questions:

Q1. What is data visualization?
Answer:
Graphical representation of data.

Q2. Which libraries are used for visualization?
Answer:
Matplotlib and Seaborn.

Q3. What is histogram?
Answer:
Graph showing distribution of numerical data.

Q4. What is boxplot?
Answer:
Graph showing spread and outliers.

Q5. What is violin plot?
Answer:
Graph showing distribution and density.

Q6. What is outlier?
Answer:
Extreme abnormal value.

Q7. Which method is used for outlier detection?
Answer:
IQR method.

Q8. What is IQR?
Answer:
Inter Quartile Range.

Q9. Formula of IQR?
Answer:
IQR = Q3 - Q1

Q10. What is mean?
Answer:
Average of values.

Q11. What is median?
Answer:
Middle value of sorted data.

Q12. What is standard deviation?
Answer:
Measure of spread of data.

Q13. What does quantile() do?
Answer:
Calculates percentile values.

Q14. What does std() calculate?
Answer:
Standard deviation.

Q15. What does dtypes display?
Answer:
Datatypes of columns.

Q16. What does subplot() do?
Answer:
Creates multiple graphs in one figure.

Q17. What does bins parameter do?
Answer:
Divides histogram into intervals.

Q18. What does tight_layout() do?
Answer:
Adjusts spacing between plots.

Q19. Which dataset did you use?
Answer:
Iris dataset.

Q20. Which target column is excluded?
Answer:
variety

Q21. What does hue parameter do?
Answer:
Separates data using colors.

Q22. Why use boxplot?
Answer:
To identify outliers and spread.

Q23. Why use histogram?
Answer:
To understand data distribution.

Q24. What does violin plot show better than boxplot?
Answer:
Density and distribution shape.

Q25. What is distribution?
Answer:
Spread pattern of data values.

Simple Viva Flow:
1. Imported libraries
2. Loaded Iris dataset
3. Displayed datatypes
4. Created histograms
5. Created boxplots
6. Calculated IQR and detected outliers
7. Calculated mean, median and standard deviation
8. Created violin plots for feature comparison

Conclusion:
This practical demonstrates data visualization and outlier analysis using Matplotlib and Seaborn on Iris dataset.

```
