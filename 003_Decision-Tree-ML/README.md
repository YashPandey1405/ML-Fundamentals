# 🌳 Decision Tree in Machine Learning

## 🧠 What is a Decision Tree?
A Decision Tree is a supervised learning algorithm used for:
- **Classification** (e.g., spam detection)
- **Regression** (e.g., predicting prices)

It splits the data into subsets based on feature values using decision nodes and leaf nodes.

---

## 🔍 Key Concepts

- **Root Node:** Represents the entire dataset (initial decision point)
- **Decision Nodes:** Nodes that split the dataset on a feature
- **Leaf Nodes:** Final output/classification
- **Gini Index:** Impurity measure used by some tree algorithms
- **Entropy:** Measures impurity of a dataset  
- **Information Gain:** Reduction in entropy after a dataset is split

---

## ⚙️ Python Implementation (Using Scikit-learn)

### 1. **Import Libraries**
```python
from sklearn.datasets import load_iris
from sklearn.tree import DecisionTreeClassifier, plot_tree
from sklearn.model_selection import train_test_split
from sklearn.metrics import accuracy_score
import matplotlib.pyplot as plt
```

---

### 2. **Load and Split Dataset**
```python
# Load Iris dataset
data = load_iris()
X = data.data
y = data.target

# Split into train and test sets
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
```

---

### 3. **Train the Model**
```python
# Create Decision Tree Classifier
clf = DecisionTreeClassifier(criterion='entropy', random_state=42)
clf.fit(X_train, y_train)
```

---

### 4. **Make Predictions**
```python
y_pred = clf.predict(X_test)

# To Evaluate The Accuracy Of The Model....
accuracy = accuracy_score(y_test, y_pred)
print(f"Accuracy: {accuracy * 100:.2f}%")
```

---

### 5. **Visualize the Tree**
```python
plt.figure(figsize=(12, 8))
plot_tree(clf, filled=True, feature_names=data.feature_names, class_names=data.target_names)
plt.show()
```

---

## 📌 Advantages
- Easy to understand and interpret
- No need for feature scaling
- Can handle both numerical and categorical data

## ⚠️ Disadvantages
- Prone to overfitting
- Can be unstable to small data variations

---

## 🧪 Real-World Use Cases
- Fraud detection
- Customer segmentation
- Medical diagnosis
- Credit scoring
