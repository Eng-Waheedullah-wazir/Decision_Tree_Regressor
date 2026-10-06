# Decision Tree Regressor

This project implements a **Decision Tree Regressor** using Scikit-learn and evaluates the model on training and testing data.

## 📌 Project Overview

A Decision Tree Regressor is a supervised machine learning algorithm used to predict **continuous numerical values**.

In this project, different values of:

* `max_depth`
* `min_samples_split`

were tested to observe their effect on model performance and identify possible **overfitting**.

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Jupyter Notebook / Google Colab

---

## 🤖 Model

The model used in this project is:

```python
from sklearn.tree import DecisionTreeRegressor

regressor = DecisionTreeRegressor(
    max_depth=5,
    min_samples_split=10
)
```

The model was trained using the training dataset and evaluated using the `score()` method.

---

## 📊 Model Evaluation

The `score()` method for `DecisionTreeRegressor` returns the **R² (coefficient of determination)** score.

### Test Score

```text
0.6453379642498638
```

**Test R² Score:**

```text
0.6453
```

This means the model explains approximately **64.53% of the variance** in the test data.

---

## 📈 Training Score

For the initial model:

```text
Training R² Score:
0.817524057791948
```

Approximately:

```text
81.75%
```

### Comparison

| Dataset  | R² Score |
| -------- | -------: |
| Training |   0.8175 |
| Testing  |   0.6453 |

The difference between the training and testing scores indicates that the model has **some overfitting**.

---

## 🌳 Effect of Tree Depth and Minimum Samples Split

Different hyperparameter combinations were tested.

### Experiment 1

```text
max_depth = 5
min_samples_split = 10
```

Training score:

```text
0.817524057791948
```

---

### Experiment 2

```text
max_depth = 20
min_samples_split = 10
```

Scores obtained:

```text
0.7542754888370072
```

and

```text
0.8846757236467796
```

The increase in the training score when the tree is allowed to become deeper shows that the tree is becoming more capable of fitting the training data.

---

## ⚠️ Overfitting Analysis

Decision trees can easily overfit when they become too complex.

A deeper tree can create many branches and learn very specific patterns from the training dataset. This can result in:

```text
High Training Score
        ↓
Complex Tree
        ↓
Poor Generalization
        ↓
Lower Test Score
```

Therefore, parameters such as:

```python
max_depth
min_samples_split
```

are important for controlling tree complexity.

### `max_depth`

Controls the maximum depth of the decision tree.

```python
max_depth=5
```

creates a shallower tree, while:

```python
max_depth=20
```

allows a much deeper tree.

### `min_samples_split`

Controls the minimum number of samples required to split an internal node.

For example:

```python
min_samples_split=10
```

means that a node must contain at least **10 samples** before it can be split.

---

## 🧪 Conclusion

The experiments demonstrate that changing Decision Tree hyperparameters can significantly affect model performance.

The initial model achieved:

```text
Training R² = 0.8175
Testing R²  = 0.6453
```

The difference between these scores suggests that the model does not generalize perfectly to unseen data.

Increasing the tree depth can improve the model's ability to fit training data, but an excessively deep tree may increase the risk of **overfitting**.

Therefore, hyperparameter tuning is important for finding a good balance between **underfitting and overfitting**.

---

```

---

## 🚀 Future Improvements

* Perform systematic hyperparameter tuning.
* Compare different `max_depth` values.
* Compare different `min_samples_split` values.
* Evaluate the model using MAE and RMSE.
* Visualize the decision tree.
* Compare Decision Tree Regression with Random Forest Regression.

---

## 👨‍💻 Author

**Waheed Ullah**

Software Engineering Student
FAST NUCES Peshawar

