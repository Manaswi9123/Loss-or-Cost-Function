# Loss-or-Cost-Function
# 📉 Measuring Error: Loss & Cost Functions in Python

In Machine Learning, a model "learns" by trying to minimize the error between its predictions and the actual data. This repository implements the core mathematical functions used to quantify that error, providing a hands-on understanding of how models evaluate their own performance.

---

## 🛠️ The Math Stack
* **Language:** Python
* **Library:** NumPy (for efficient array-based calculations)
* **Concepts:** Error residuals, Squaring vs. Absolute values, and Vectorization.

---

## 🧠 Functions Implemented

### 1. Mean Absolute Error (MAE)
Calculates the average of the absolute differences between predicted and actual values. 
* **Characteristic:** It is robust to outliers since it doesn't "square" the error.
* **Equation:** $\frac{1}{n} \sum_{i=1}^{n} |y_{true} - y_{pred}|$

### 2. Mean Squared Error (MSE)
Calculates the average of the squares of the errors.
* **Characteristic:** It heavily penalizes larger errors (outliers), making it the standard choice for most regression problems.
* **Equation:** $\frac{1}{n} \sum_{i=1}^{n} (y_{true} - y_{pred})^2$

### 3. Log Loss (Binary Cross-Entropy)
Used primarily in classification tasks (like Logistic Regression).
* **Characteristic:** It penalizes false certainties. If a model is very confident about a wrong prediction, the Log Loss increases exponentially.
* **Implementation:** Handled using a small epsilon value ($1e-15$) to avoid `log(0)` errors during calculation.

---

## 📊 Why are these important?
Loss and Cost functions are the "compass" for optimization algorithms like **Gradient Descent**. 
* **Loss Function:** Measures the error for a single data point.
* **Cost Function:** Measures the average error across the entire training dataset.
The goal of any training process is to find the weights and biases that result in the lowest possible value for the Cost Function.

---

## 🚀 How to Run

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/Manaswi9123/Python-DataScience-Fundamentals.git](https://github.com/Manaswi9123/Python-DataScience-Fundamentals.git)

2. **Execute:** Open LossOrCostFunc.ipynb in any Jupyter environment.

3. **Analyze:** Compare the output of the mae and mse functions on the same sample arrays to see how squaring the error changes the final score.
