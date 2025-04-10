# 🐍 Logistic Regression - Multiclass Classification in Python

Two common approaches using `scikit-learn`:  
🔹 **One-vs-Rest (OvR)**  
🔹 **Multinomial (Softmax)**

---

## 📦 Import Libraries

```python
from sklearn.linear_model import LogisticRegression
from sklearn.datasets import load_iris
from sklearn.model_selection import train_test_split
from sklearn.metrics import classification_report
```

---

## 🌸 Load Data (Example: Iris Dataset)

```python
X, y = load_iris(return_X_y=True)
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
```

---

## ⚔️ One-vs-Rest (OvR)

```python
# OvR is default for LogisticRegression
ovr_model = LogisticRegression(multi_class='ovr', solver='liblinear')
ovr_model.fit(X_train, y_train)

# Prediction & Evaluation
y_pred_ovr = ovr_model.predict(X_test)
print("OvR Classification Report:\n", classification_report(y_test, y_pred_ovr))
```

### ⚙️ Notes:
- `multi_class='ovr'`: Explicitly set OvR.
- `solver='liblinear'`: Required for OvR.

---

## 🌈 Multinomial (Softmax)

```python
# Use multinomial with solver that supports it
multi_model = LogisticRegression(multi_class='multinomial', solver='lbfgs', max_iter=200)
multi_model.fit(X_train, y_train)

# Prediction & Evaluation
y_pred_multi = multi_model.predict(X_test)
print("Multinomial Classification Report:\n", classification_report(y_test, y_pred_multi))
```

### ⚙️ Notes:
- `multi_class='multinomial'`: Enables Softmax.
- `solver='lbfgs'`: Supports multinomial.
- `max_iter`: May need increase for convergence.

---

## 🧠 Summary

| Method      | Param                       | Solver        |
|-------------|-----------------------------|---------------|
| One-vs-Rest | `multi_class='ovr'`         | `liblinear`   |
| Multinomial | `multi_class='multinomial'` | `lbfgs`, `saga` |

---

## ✅ Pro Tips

- Always scale your features (`StandardScaler`) for better convergence.
- Use `model.predict_proba(X)` to get class probabilities.
- For large datasets, consider `saga` solver with `multinomial`.
