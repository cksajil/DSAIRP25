# Types of Algorithms
- Supervised Learning
	- Classification
	- Regression
- Unsupervised Learning
	- Clustering
- Reinforcement Learning


# Introduction to Classification, Regression and Clustering
- What is classification and regression
- What is regression
- Performance metrics for regression
- Linear Regression
- Scikit-Learning API usage
- Implementation from scratch
- Polynomial regression

```python
from sklearn.preprocessing import PolynomialFeatures
from sklearn.linear_model import LinearRegression

poly = PolynomialFeatures(degree=3, include_bias=False)
X_poly = poly.fit_transform(X_train)

model = LinearRegression()
model.fit(X_poly, y_train)

X_test_poly = poly.transform(X_test)
y_test_pred = model.predict(X_test_poly)

mse = mean_squared_error(y_test, y_test_pred)
r2 = r2_score(y_test, y_test_pred)
print(f"Mean Squared Error: {mse:.2f}")
print(f"R-squared: {r2:.2f}")
```



- Regularization


## Regression Performance Metrics
- Regression
    - Mean Absolute Error (MAE): Average absolute difference between actual and predicted values.
    - Mean Squared Error (MSE): Average squared difference.
    - Root Mean Squared Error (RMSE): Square root of MSE.
    - R-squared (Δ²): Proportion of variance explained by the model.
    - Mean Absolute Percentage Error (MAPE): Percentage-based error.

[![Classification, Regression, Clustering](https://img.youtube.com/vi/T4Ha6U0PJ7s/0.jpg)](https://youtu.be/v=T4Ha6U0PJ7s)

# Linear Regression & Regularization

[![Linear Regression Intuition](https://img.youtube.com/vi/XnaJ04s6DTs/0.jpg)](https://www.youtube.com/watch?v=XnaJ04s6DTs)

[![Linear Regression from Scratch](https://img.youtube.com/vi/_yiTZQ0vR60/0.jpg)](https://www.youtube.com/watch?v=_yiTZQ0vR60)


## Quick Introduction to Bias and Variance

[![Intro 2 Bias and Variance ](https://img.youtube.com/vi/vEKaehF3d9U/0.jpg)](https://www.youtube.com/watch?v=vEKaehF3d9U)


## Performance metric on Train and Test Data

| **Train** | **Test** | **Remarks**             |
|-----------|----------|-------------------------|
| Low       | Low      | Biased Model            |
| High      | Low      | Overfit Model           |
| High      | High     | Correct Model           |
| Low       | High     | Ruled out/Doesn't occur |