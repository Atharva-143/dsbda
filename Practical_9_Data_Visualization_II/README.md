```txt id="4p8m1z"
DATA VISUALIZATION PRACTICAL
TITANIC DATASET ANALYSIS

Aim:
To perform statistical analysis and visualization using Titanic dataset.

Important Terms:
1. Mean -> Average value
2. Median -> Middle value
3. Mode -> Most frequent value
4. Histogram -> Distribution graph
5. Box Plot -> Detects spread and outliers
6. Violin Plot -> Distribution and density graph
7. Catplot -> Categorical count graph
8. Outlier -> Extreme value
9. Data Visualization -> Graphical representation of data

Code Explanation:

import seaborn as sns
Used for statistical visualization.

import matplotlib.pyplot as plt
Used for plotting graphs.

from collections import Counter
Used for counting frequency of values.

df = sns.load_dataset('titanic')
Loads Titanic dataset.

df.head()
Displays first 5 rows.

df.describe()
Displays statistical summary.

df.describe().transpose()
Displays transposed statistical summary.

transpose()
Converts rows into columns.

age_data = df['age'].dropna()
Selects age column and removes missing values.

dropna()
Removes null values.

sorted_age_data = sorted(age_data)
Sorts age values.

n = len(sorted_age_data)
Finds total number of values.

mean_age = sum(age_data) / len(age_data)
Calculates mean age.

Mean:
Average of values.

Median Calculation:
If total values are odd:
Middle value selected.

If total values are even:
Average of two middle values selected.

Counter(age_data)
Counts frequency of age values.

most_common(1)
Finds most repeated value.

mode_age
Stores mode value.

Mode:
Most frequently occurring value.

sns.boxplot(x='sex', y='age', hue='survived', data=df)
Creates box plot.

x='sex'
Gender on x-axis.

y='age'
Age on y-axis.

hue='survived'
Separates survived and non-survived data using colors.

Box plot shows:
- median
- quartiles
- outliers

palette='viridis'
Applies color theme.

sns.violinplot(x='sex', y='age', hue='survived', data=df)
Creates violin plot.

Violin plot shows:
- data distribution
- density
- spread

palette='pastel'
Applies pastel colors.

sns.catplot(x='sex', hue='survived', data=df, kind='count')
Creates categorical count plot.

kind='count'
Counts number of records.

Shows:
- survival count by gender

plt.title()
Adds graph title.

plt.xlabel()
Adds x-axis label.

plt.ylabel()
Adds y-axis label.

plt.show()
Displays graph.

Important Viva Questions:

Q1. What is data visualization?
Answer:
Graphical representation of data.

Q2. Which libraries are used for visualization?
Answer:
Seaborn and Matplotlib.

Q3. What is mean?
Answer:
Average of values.

Q4. What is median?
Answer:
Middle value of sorted data.

Q5. What is mode?
Answer:
Most frequent value.

Q6. What is histogram?
Answer:
Graph showing distribution of numerical data.

Q7. What is box plot?
Answer:
Graph showing spread and outliers.

Q8. What is violin plot?
Answer:
Graph showing distribution and density.

Q9. What is catplot?
Answer:
Categorical plot for count analysis.

Q10. What does hue parameter do?
Answer:
Separates data using colors.

Q11. What does dropna() do?
Answer:
Removes missing values.

Q12. What does Counter() do?
Answer:
Counts frequency of values.

Q13. What does most_common(1) do?
Answer:
Finds most frequent value.

Q14. What is outlier?
Answer:
Extreme abnormal value.

Q15. Which dataset did you use?
Answer:
Titanic dataset.

Q16. What does describe() do?
Answer:
Provides statistical summary.

Q17. What does transpose() do?
Answer:
Converts rows into columns.

Q18. What does kind='count' do?
Answer:
Displays count of records.

Q19. What is palette in seaborn?
Answer:
Color theme for graphs.

Q20. What does plt.show() do?
Answer:
Displays graph.

Q21. Which graph is used for distribution?
Answer:
Histogram and violin plot.

Q22. Which graph helps detect outliers?
Answer:
Box plot.

Q23. Why remove null values before calculation?
Answer:
Because missing values affect calculations.

Q24. What is Seaborn?
Answer:
Python library for statistical visualization.

Q25. What is Matplotlib?
Answer:
Python library used for plotting graphs.

Simple Viva Flow:
1. Imported libraries
2. Loaded Titanic dataset
3. Displayed statistical summary
4. Calculated mean, median and mode
5. Created box plot
6. Created violin plot
7. Created categorical count plot
8. Analyzed survival patterns by gender

Conclusion:
This practical demonstrates statistical analysis and data visualization using Titanic dataset with Seaborn and Matplotlib.

```
