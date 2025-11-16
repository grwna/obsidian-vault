# Keywords
- Dependent vs Independent Variables
- Simple Linear Regression (SLR)
- Intercept ($\beta_{0}$) and Slope ($\beta_{1}$)
- Multivariate Linear Regression (MLR)
- Parameter estimation
- Least Square Estimator (LSE)
- Regression --> Supervised Learning
- Hypothesis ($h$)
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Residual Sum of Squares (RSS/SSE)
- R2-Score
- Cost Function $J(\theta)$
- Analytic vs Iterative Solution


# What
A way to predict output based on inputs. Assumes that the input and output has a **linear relationship**:
- Dependent ($y$) - output
- Independent ($x$) - input

**SLR**
Only one $x$ (input).

**MLR**
Multiple inputs ($x$)

# Least Square Estimator
Minimize SSE
$$SSE=\sum_{i=1}^ne_{i}^2$$
$$SSE=\sum_{i=1}^n(y_{i}-\hat{y}_{i})^2$$
$$SSE=\sum_{i=1}^n(y_{i}-b_{0}-b_{1}x_{i})^2$$
