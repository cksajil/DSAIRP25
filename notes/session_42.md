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

## Performance metric on Train and Test Data

| **Train** | **Test** | **Remarks**             |
|-----------|----------|-------------------------|
| Low       | Low      | Biased Model            |
| High      | Low      | Overfit Model           |
| High      | High     | Correct Model           |
| Low       | High     | Ruled out/Doesn't occur |