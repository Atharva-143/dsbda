```txt id="c5m4t1"
DATA ANALYTICS I PRACTICAL
LINEAR REGRESSION

Aim:
To predict house prices using Linear Regression on Boston Housing dataset.

Important Terms:
1. Machine Learning -> Systems learning from data
2. Linear Regression -> Algorithm for numerical prediction
3. Features -> Input variables
4. Target Variable -> Output variable
5. Training Data -> Data used for learning
6. Testing Data -> Data used for evaluation
7. Prediction -> Estimated output
8. MSE -> Prediction error measure
9. R2 Score -> Model performance measure

Code Explanation:

import pandas as pd
Used for dataframe handling.

from sklearn.model_selection import train_test_split
Used to split dataset into training and testing data.

from sklearn.linear_model import LinearRegression
Imports Linear Regression algorithm.

from sklearn.metrics import mean_squared_error, r2_score
Used for model evaluation.

df = pd.read_csv("BostonHousing.csv")
Loads Boston Housing dataset.

df.head()
Displays first 5 rows.

df.columns
Displays column names.

df.info()
Displays:
- datatypes
- non-null values
- memory usage

df.describe()
Displays statistical summary:
- mean
- min
- max
- std deviation

df.isnull().sum()
Checks missing values.

df = df.dropna()
Removes rows containing null values.

X = df.drop('medv', axis=1)
Selects input features.

Features:
All columns except medv.

y = df['medv']
Target variable.

medv:
Median house value.

train_test_split()
Splits data into:
- training data
- testing data

test_size=0.2
20% data used for testing.

random_state=42
Ensures same random split every time.

model = LinearRegression()
Creates Linear Regression model.

model.fit(X_train, y_train)
Trains model using training data.

Training means:
Model learns patterns from data.

y_pred = model.predict(X_test)
Predicts house prices.

mean_squared_error(y_test, y_pred)
Calculates prediction error.

Lower MSE means better model.

r2_score(y_test, y_pred)
Measures model performance.

R2 Score range:
0 to 1

Closer to 1 means better model.

Important Viva Questions:

Q1. What is Data Analytics?
Answer:
Process of analyzing data for useful insights.

Q2. What is Machine Learning?
Answer:
Systems learning from data and making predictions.

Q3. What is Linear Regression?
Answer:
Algorithm used for numerical prediction.

Q4. Which dataset did you use?
Answer:
Boston Housing dataset.

Q5. What is target variable?
Answer:
Output variable to predict.

Q6. What is target variable in your practical?
Answer:
medv

Q7. What are features?
Answer:
Input variables used for prediction.

Q8. Why split dataset?
Answer:
To train and evaluate model separately.

Q9. What is training data?
Answer:
Data used for learning.

Q10. What is testing data?
Answer:
Data used for evaluation.

Q11. What does fit() do?
Answer:
Trains the model.

Q12. What does predict() do?
Answer:
Predicts output values.

Q13. What does dropna() do?
Answer:
Removes rows with missing values.

Q14. What is MSE?
Answer:
Mean Squared Error.

Q15. What does MSE measure?
Answer:
Prediction error.

Q16. What does low MSE indicate?
Answer:
Better model performance.

Q17. What is R2 Score?
Answer:
Measure of model accuracy/performance.

Q18. Range of R2 Score?
Answer:
0 to 1

Q19. What does R2 close to 1 indicate?
Answer:
Better model performance.

Q20. What type of problem is house price prediction?
Answer:
Regression problem.

Q21. Difference between regression and classification?
Answer:
Regression predicts numerical values.
Classification predicts categories.

Q22. What is supervised learning?
Answer:
Learning using labeled data.

Q23. What does describe() do?
Answer:
Provides statistical summary.

Q24. What does info() display?
Answer:
- datatypes
- non-null values
- memory usage

Q25. Why remove null values?
Answer:
Machine learning models cannot handle missing values directly.

Simple Viva Flow:
1. Imported libraries
2. Loaded Boston Housing dataset
3. Displayed dataset information
4. Checked missing values
5. Removed null values
6. Selected features and target
7. Split dataset into training and testing data
8. Trained Linear Regression model
9. Predicted house prices
10. Evaluated model using MSE and R2 Score

Conclusion:
This practical demonstrates house price prediction using Linear Regression and evaluates model performance using MSE and R2 Score.

```
