# Polynomial Regression in Python  

## 🚀 Overview  
Polynomial Regression is an extension of Linear Regression that models the relationship between independent and dependent variables as an **n-degree polynomial**.  

## 📌 Steps to Implement  
1. **Import Libraries**: `numpy`, `matplotlib`, `sklearn`  
2. **Prepare Data**: Independent (`X`) & Dependent (`y`) variables  
3. **Transform Features**: Use `PolynomialFeatures` to generate polynomial terms  
4. **Train Model**: Fit using `LinearRegression()`  
5. **Predict & Visualize**: Plot results for better understanding  

## 📝 Code Example  
```python
import numpy as np
import matplotlib.pyplot as plt
from sklearn.preprocessing import PolynomialFeatures
from sklearn.linear_model import LinearRegression

# Sample Data
X = np.array([1, 2, 3, 4, 5]).reshape(-1, 1)
y = np.array([2, 5, 10, 17, 26])  # Quadratic Relationship: y = x^2 + 1

# Polynomial Transformation (Degree = 2)
poly = PolynomialFeatures(degree=2)
X_poly = poly.fit_transform(X)

# Train Model
model = LinearRegression()
model.fit(X_poly, y)

# Predictions
X_test = np.linspace(1, 5, 100).reshape(-1, 1)
X_test_poly = poly.transform(X_test)
y_pred = model.predict(X_test_poly)

# Visualization
plt.scatter(X, y, color='red', label='Data')
plt.plot(X_test, y_pred, color='blue', label='Polynomial Fit')
plt.legend()
plt.show()
```

## 🎯 Key Points  
- `PolynomialFeatures(degree=n)`: Generates polynomial terms  
- `LinearRegression()`: Fits transformed data  
- Use higher-degree polynomials cautiously to avoid **overfitting**  

## 📖 Dependencies  
```bash
pip install numpy matplotlib scikit-learn
```