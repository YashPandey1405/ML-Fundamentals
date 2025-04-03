# 📌 Linear Regression Implementation in Python

## 🚀 1️⃣ Import Libraries
```python
import numpy as np
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
```

## 📊 2️⃣ Load & Split Data
```python
X = np.array([1, 2, 3, 4, 5, 6]).reshape(-1, 1)
y = np.array([2, 4, 5, 4, 5, 7])

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

## 📊 6️⃣ Visualize Results
```python
plt.scatter(X_train, y_train, label="Training Data")
plt.plot(X_train, regressor.predict(X_train), 'r', label="Regression Line")
plt.xlabel("X")
plt.ylabel("y")
plt.legend()
plt.show()
```

