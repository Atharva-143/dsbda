```txt id="8v3m2q"
DATA VISUALIZATION PRACTICAL
TITANIC DATASET

Aim:
To perform data visualization and statistical analysis using Seaborn and Matplotlib.

Important Terms:
1. Data Visualization -> Graphical representation of data
2. Histogram -> Distribution of numerical data
3. Box Plot -> Detects spread and outliers
4. Violin Plot -> Distribution and density of data
5. Scatter Plot -> Relationship between two variables
6. KDE -> Kernel Density Estimation
7. Outliers -> Extreme values
8. Dataset -> Collection of data

Code Explanation:

import seaborn as sns
Used for statistical visualization.

import matplotlib.pyplot as plt
Used for plotting graphs.

df = sns.load_dataset('titanic')
Loads Titanic dataset from seaborn.

df.head()
Displays first 5 rows.

df.describe().transpose()
Displays statistical summary:
- mean
- std
- min
- max
- quartiles

transpose()
Converts rows into columns for better readability.

sns.histplot(df['age'], kde=True, bins=20)
Creates histogram for Age column.

Histogram:
Shows distribution of data.

kde=True
Displays smooth density curve.

bins=20
Divides graph into 20 intervals.

plt.title()
Adds graph title.

plt.xlabel()
Adds x-axis label.

plt.ylabel()
Adds y-axis label.

plt.show()
Displays graph.

sns.boxplot(x='class', y='age', data=df)
Creates box plot.

Box plot shows:
- median
- quartiles
- outliers

x='class'
Passenger class on x-axis.

y='age'
Age on y-axis.

sns.violinplot(x='class', y='age', data=df)
Creates violin plot.

Violin plot shows:
- data distribution
- density
- spread

sns.histplot(x='fare', bins=10, data=df, hue='survived')
Creates fare distribution histogram.

hue='survived'
Separates graph based on survival.

0 -> Not survived
1 -> Survived

sns.scatterplot(x='age', y='fare', data=df)
Creates scatter plot.

Scatter plot shows relationship between:
- Age
- Fare

sns.scatterplot(x='age', y='fare', hue='survived', data=df)
Scatter plot with survival category.

Different colors represent:
- survived
- not survived

Important Viva Questions:

Q1. What is data visualization?
Answer:
Graphical representation of data.

Q2. Which libraries are used for visualization?
Answer:
Seaborn and Matplotlib.

Q3. What is histogram?
Answer:
Graph showing distribution of numerical data.

Q4. What does kde=True do?
Answer:
Displays density curve.

Q5. What are bins in histogram?
Answer:
Intervals dividing data range.

Q6. What is box plot?
Answer:
Graph showing spread and outliers.

Q7. What does box plot display?
Answer:
Median, quartiles and outliers.

Q8. What is violin plot?
Answer:
Graph showing distribution and density of data.

Q9. What is scatter plot?
Answer:
Graph showing relationship between two variables.

Q10. What is outlier?
Answer:
Extreme abnormal value.

Q11. Which dataset did you use?
Answer:
Titanic dataset.

Q12. What does describe() do?
Answer:
Provides statistical summary.

Q13. What does transpose() do?
Answer:
Converts rows into columns.

Q14. What does hue parameter do?
Answer:
Separates data using colors.

Q15. What does plt.show() do?
Answer:
Displays graph.

Q16. What is KDE?
Answer:
Kernel Density Estimation.

Q17. Why use visualization?
Answer:
To understand patterns and trends in data.

Q18. What does scatter plot help identify?
Answer:
Relationship between variables.

Q19. Which plot is used for distribution?
Answer:
Histogram.

Q20. Which plot helps detect outliers?
Answer:
Box plot.

Q21. What is Seaborn?
Answer:
Python library for statistical visualization.

Q22. What is Matplotlib?
Answer:
Python library used for plotting graphs.

Q23. What is the purpose of title()?
Answer:
Adds title to graph.

Q24. What is xlabel()?
Answer:
Adds x-axis label.

Q25. What is ylabel()?
Answer:
Adds y-axis label.

Simple Viva Flow:
1. Imported visualization libraries
2. Loaded Titanic dataset
3. Displayed dataset and statistics
4. Created histogram for age distribution
5. Created box plot and violin plot
6. Created fare distribution graph
7. Created scatter plots for Age vs Fare
8. Analyzed survival patterns

Conclusion:
This practical demonstrates statistical data visualization using Seaborn and Matplotlib on Titanic dataset.

```
