# 📌 Multiple Linear Regression Implementation in Python

## 🚀 1️⃣ Import Libraries

```python
import numpy as np
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
```

## 📊 2️⃣ Load & Split Data

```python
# Sample dataset with multiple features
X = np.array([[1, 2], [2, 3], [3, 4], [4, 5], [5, 6], [6, 7]])
y = np.array([3, 5, 7, 9, 11, 13])

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
```

## 🎯 3️⃣ Train the Model

```python
regressor = LinearRegression()
regressor.fit(X_train, y_train)
```

## 🔍 4️⃣ Get Model Parameters

```python
print("Coefficients:", regressor.coef_)
print("Intercept:", regressor.intercept_)
```

## 📈 5️⃣ Make Predictions

```python
y_pred = regressor.predict(X_test)
```

## 📊 6️⃣ Evaluate Model Performance

```python
from sklearn.metrics import mean_squared_error, r2_score

mse = mean_squared_error(y_test, y_pred)
r2 = r2_score(y_test, y_pred)

print("Mean Squared Error:", mse)
print("R-Squared Score:", r2)
```
