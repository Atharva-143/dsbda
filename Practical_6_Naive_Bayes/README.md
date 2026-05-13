```txt id="1l5z8k"
DATA ANALYTICS PRACTICAL
NAIVE BAYES CLASSIFICATION

Aim:
To perform classification using Gaussian Naive Bayes algorithm on Iris dataset.

Important Terms:
1. Classification -> Predicting classes/categories
2. Naive Bayes -> Probability-based classification algorithm
3. GaussianNB -> Naive Bayes for continuous data
4. Features -> Input variables
5. Target Variable -> Output variable
6. Standardization -> Scaling data
7. Confusion Matrix -> Evaluation table
8. Accuracy -> Overall correctness
9. Precision -> Correct positive predictions
10. Recall -> Ability to identify actual positives

Code Explanation:

import pandas as pd
Used for dataframe handling.

import numpy as np
Used for numerical operations.

import seaborn as sns
Used for visualization.

import matplotlib.pyplot as plt
Used for plotting graphs.

train_test_split
Splits dataset into training and testing data.

StandardScaler
Used for standardization.

GaussianNB
Naive Bayes classification algorithm.

confusion_matrix, accuracy_score, precision_score, recall_score
Used for model evaluation.

df = pd.read_csv("Iris.csv")
Loads Iris dataset.

df.head()
Displays first 5 rows.

X = df.drop('variety', axis=1)
Selects input features.

Features:
- sepal length
- sepal width
- petal length
- petal width

y = df['variety']
Target variable.

Target classes:
- Setosa
- Versicolor
- Virginica

train_test_split()
Splits dataset into:
- training data
- testing data

test_size=0.2
20% data used for testing.

random_state=42
Ensures same random split every time.

scaler = StandardScaler()
Creates scaler object.

X_train_scaled = scaler.fit_transform(X_train)
Standardizes training data.

X_test_scaled = scaler.transform(X_test)
Standardizes testing data.

Standardization:
Mean = 0
Standard deviation = 1

Why standardization?
Because features may have different scales.

model = GaussianNB()
Creates Gaussian Naive Bayes model.

model.fit(X_train_scaled, y_train)
Trains model.

Training means:
Model learns patterns from data.

y_pred = model.predict(X_test_scaled)
Predicts flower species.

confusion_matrix(y_test, y_pred)
Creates confusion matrix.

Confusion Matrix:
TP -> True Positive
TN -> True Negative
FP -> False Positive
FN -> False Negative

pd.DataFrame(cm)
Converts confusion matrix into table format.

sns.heatmap()
Displays confusion matrix as heatmap.

annot=True
Displays numbers inside heatmap.

cmap='Blues'
Applies blue color theme.

plt.show()
Displays graph.

accuracy_score()
Calculates overall accuracy.

precision_score()
Calculates precision.

recall_score()
Calculates recall.

error_rate = 1 - accuracy
Calculates incorrect prediction percentage.

average='macro'
Calculates average metric across all classes.

Important Viva Questions:

Q1. What is Naive Bayes?
Answer:
Probability-based classification algorithm.

Q2. What is GaussianNB?
Answer:
Naive Bayes algorithm used for continuous numerical data.

Q3. What type of learning is Naive Bayes?
Answer:
Supervised learning.

Q4. What is classification?
Answer:
Predicting categories/classes.

Q5. Which dataset did you use?
Answer:
Iris dataset.

Q6. What are the classes in Iris dataset?
Answer:
Setosa, Versicolor, Virginica.

Q7. What are features?
Answer:
Input variables used for prediction.

Q8. What is target variable?
Answer:
Output variable to predict.

Q9. What is target variable in your practical?
Answer:
variety

Q10. Why split dataset?
Answer:
To train and evaluate model separately.

Q11. What is training data?
Answer:
Data used for learning.

Q12. What is testing data?
Answer:
Data used for evaluation.

Q13. What is standardization?
Answer:
Scaling data so mean becomes 0 and standard deviation becomes 1.

Q14. Why use StandardScaler?
Answer:
To balance feature scales.

Q15. What does fit() do?
Answer:
Trains the model.

Q16. What does predict() do?
Answer:
Predicts output values.

Q17. What is confusion matrix?
Answer:
Table used to evaluate classification model.

Q18. What is TP?
Answer:
Correct positive prediction.

Q19. What is TN?
Answer:
Correct negative prediction.

Q20. What is FP?
Answer:
Incorrect positive prediction.

Q21. What is FN?
Answer:
Incorrect negative prediction.

Q22. What is accuracy?
Answer:
Overall correctness of model.

Q23. What is precision?
Answer:
Correctness of positive predictions.

Q24. What is recall?
Answer:
Ability to identify actual positives.

Q25. What is heatmap?
Answer:
Graphical representation of matrix values using colors.

Q26. Which library is used for heatmap?
Answer:
Seaborn.

Q27. Which library is used for plotting?
Answer:
Matplotlib.

Q28. Why use GaussianNB?
Answer:
Because data is continuous numerical data.

Q29. What does average='macro' mean?
Answer:
Calculates average metric equally across all classes.

Q30. What is supervised learning?
Answer:
Learning using labeled data.

Simple Viva Flow:
1. Imported libraries
2. Loaded Iris dataset
3. Selected features and target
4. Split dataset into training and testing data
5. Standardized data
6. Trained Gaussian Naive Bayes model
7. Predicted outputs
8. Generated confusion matrix
9. Displayed heatmap
10. Calculated accuracy, precision and recall

Conclusion:
This practical demonstrates classification using Gaussian Naive Bayes and evaluates performance using confusion matrix and evaluation metrics.

```
