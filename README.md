# Author: Baraka Mandi
# Class : Machine Learning (CS 5710)

# Linear Regression: Closed-Form vs Gradient Descent

This code demonstrates **Linear Regression** implemented from scratch using:

- **Closed-form solution (Normal Equation)**
- **Gradient Descent optimization**

It also visualizes:
- The fitted regression lines
- The loss (MSE) convergence during training

The goal is to show that both approaches converge to similar parameters while highlighting how gradient descent learns iteratively.

---

## Features

- Synthetic dataset generation with noise
- Manual implementation of:
  - Normal Equation
  - Gradient Descent
- Comparison of learned parameters
- Visualization of:
  - Data + fitted regression lines
  - Mean Squared Error loss curve

---

## Dataset Description

The dataset is generated using the linear equation:

y = 3 + 4x + ε

Where:
- x is sampled uniformly from [0, 5]
- ε is Gaussian noise
- 200 data points are generated
- A bias term (column of ones) is added manually

---

## Methods Used

### 1. Closed-Form Solution (Normal Equation)

The model parameters are computed directly using:

θ = (XᵀX)⁻¹Xᵀy

This provides the exact solution (when the matrix inverse exists).

---

### 2. Gradient Descent

An iterative optimization technique that minimizes **Mean Squared Error (MSE)**:

MSE = (1/m) Σ (Xθ − y)²

**Configuration:**
- Learning rate: 0.05
- Iterations: 1000
- Initial parameters: [0, 0]


---

## Visualizations

### Plot 1: Linear Regression Comparison
- Scatter plot of raw data
- Regression line from:
  - Closed-form solution
  - Gradient Descent

### Plot 2: Loss Curve
- Mean Squared Error vs Iterations
- Shows how gradient descent converges over time

---

## Requirements

```bash
pip install numpy matplotlib
```

---

## How to Run

run it as a python notebook (ipynb)

---


