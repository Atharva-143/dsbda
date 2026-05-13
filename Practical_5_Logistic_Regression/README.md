```txt id="1i9x7n"
DATA ANALYTICS II PRACTICAL
LOGISTIC REGRESSION

Aim:
To perform classification using Logistic Regression and evaluate model performance.

Important Terms:
1. Classification -> Predicting categories/classes
2. Logistic Regression -> Classification algorithm
3. Features -> Input variables
4. Target Variable -> Output variable
5. Standardization -> Scaling data
6. Confusion Matrix -> Evaluation table
7. Accuracy -> Overall correctness
8. Precision -> Correct positive predictions
9. Recall -> Ability to identify actual positives

Code Explanation:

import pandas as pd
Used for dataframe handling.

from sklearn.model_selection import train_test_split
Used to split dataset.

from sklearn.preprocessing import StandardScaler
Used for standardization.

from sklearn.linear_model import LogisticRegression
Imports Logistic Regression algorithm.

from sklearn.metrics import confusion_matrix, accuracy_score, precision_score, recall_score
Used for model evaluation.

df = pd.read_csv("Social_Network_Ads.csv")
Loads dataset.

df.head()
Displays first 5 rows.

df.columns
Displays column names.

df['Gender'] = df['Gender'].map({'Male':0,'Female':1})
Converts categorical values into numeric.

Male -> 0
Female -> 1

X = df[['Gender', 'Age', 'EstimatedSalary']]
Selects input features.

Features:
- Gender
- Age
- EstimatedSalary

y = df['Purchased']
Target variable.

Purchased:
0 -> Not Purchased
1 -> Purchased

train_test_split()
Splits dataset into training and testing data.

test_size=0.25
25% data used for testing.

random_state=42
Ensures same random split every time.

sc = StandardScaler()
Creates scaler object.

X_train = sc.fit_transform(X_train)
Standardizes training data.

X_test = sc.transform(X_test)
Standardizes testing data.

Standardization:
Mean = 0
Standard Deviation = 1

Why standardization?
Because features may have different scales.

model = LogisticRegression()
Creates Logistic Regression model.

model.fit(X_train, y_train)
Trains the model.

Training means:
Model learns patterns from data.

y_pred = model.predict(X_test)
Predicts outputs.

confusion_matrix(y_test, y_pred)
Creates confusion matrix.

Confusion Matrix:
TP -> True Positive
TN -> True Negative
FP -> False Positive
FN -> False Negative

accuracy_score(y_test, y_pred)
Calculates overall accuracy.

precision_score(y_test, y_pred)
Calculates precision.

recall_score(y_test, y_pred)
Calculates recall.

error_rate = 1 - accuracy
Calculates incorrect prediction percentage.

Important Viva Questions:

Q1. What is Logistic Regression?
Answer:
Classification algorithm used for binary prediction.

Q2. What type of learning is Logistic Regression?
Answer:
Supervised learning.

Q3. What is classification?
Answer:
Predicting categories/classes.

Q4. Which dataset did you use?
Answer:
Social Network Ads dataset.

Q5. What are features?
Answer:
Input variables used for prediction.

Q6. What is target variable?
Answer:
Output variable to predict.

Q7. What is target variable in your practical?
Answer:
Purchased

Q8. Why convert Gender into numbers?
Answer:
Machine learning algorithms require numerical input.

Q9. What is standardization?
Answer:
Scaling data so mean becomes 0 and standard deviation becomes 1.

Q10. Why use StandardScaler?
Answer:
To balance feature scales.

Q11. Why split dataset?
Answer:
To train and evaluate model separately.

Q12. What is training data?
Answer:
Data used for learning.

Q13. What is testing data?
Answer:
Data used for evaluation.

Q14. What does fit() do?
Answer:
Trains the model.

Q15. What does predict() do?
Answer:
Predicts output values.

Q16. What is confusion matrix?
Answer:
Table used to evaluate classification model.

Q17. What is TP?
Answer:
Correct positive prediction.

Q18. What is TN?
Answer:
Correct negative prediction.

Q19. What is FP?
Answer:
Incorrect positive prediction.

Q20. What is FN?
Answer:
Incorrect negative prediction.

Q21. What is accuracy?
Answer:
Overall correctness of model.

Q22. What is precision?
Answer:
Correctness of positive predictions.

Q23. What is recall?
Answer:
Ability to identify actual positives.

Q24. What is error rate?
Answer:
Percentage of incorrect predictions.

Q25. Difference between Linear Regression and Logistic Regression?
Answer:
Linear Regression predicts numerical values.
Logistic Regression predicts categories/classes.

Q26. What is supervised learning?
Answer:
Learning using labeled data.

Q27. Why use Logistic Regression here?
Answer:
Because output is categorical (0 or 1).

Q28. What does confusion matrix show?
Answer:
Correct and incorrect classifications.

Q29. Why standardize data before Logistic Regression?
Answer:
Because features have different scales.

Q30. What does accuracy close to 1 indicate?
Answer:
Better model performance.

Simple Viva Flow:
1. Imported libraries
2. Loaded dataset
3. Converted Gender into numeric
4. Selected features and target
5. Split dataset into training and testing data
6. Standardized data
7. Trained Logistic Regression model
8. Predicted outputs
9. Generated confusion matrix
10. Calculated accuracy, precision, recall and error rate

Conclusion:
This practical demonstrates classification using Logistic Regression and evaluates performance using confusion matrix and evaluation metrics.

```
