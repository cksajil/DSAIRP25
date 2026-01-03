# Logistic Regression
# Naive Bayes
# KNN

[![KNN from scratch](https://img.youtube.com/vi/8cHGBZ_3K-8/0.jpg)](https://www.youtube.com/watch?v=8cHGBZ_3K-8)

# Hyperparameters

# Models and Tasks
| **Model**           	| **Task**       	| **Import**                                                                                                	|
|---------------------	|----------------	|-----------------------------------------------------------------------------------------------------------	|
| Linear Regression   	| Regression     	| from sklearn.linear_model import LinearRegression                                                         	|
| Logistic Regression 	| Classification 	| from sklearn.linear_model import LogisticRegression                                                       	|
| KNN                 	| Both           	| from sklearn.neighbors import KNeighborsClassifier<br>from sklearn.neighbors import KNeighborsRegressor   	|
| Naive Bayes         	| Classification 	| from sklearn.naive_bayes import GaussianNB                                                                	|
| SVM                 	| Both           	| from sklearn.svm import SVC<br>from sklearn.svm import SVR                                                	|
| Decision Tree       	| Both           	| from sklearn.tree import DecisionTreeClassifier<br>from sklearn.tree import DecisionTreeRegressor         	|
| Random Forest       	| Both           	| from sklearn.ensemble import RandomForestClassifier<br>from sklearn.ensemble import RandomForestRegressor 	|


# Performance Metrics

- Classifcation
    - TP, TN, FP, FN
    - Accuracy = (TP + TN) / (Total)
    - Precision = TP / (TP + FP)
    - Recall = TP / (TP + FN)
    - F1-Score = 2 * (Precision * Recall) / (Precision + Recall)

- Regression
    - Mean Absolute Error (MAE): Average absolute difference between actual and predicted values.
    - Mean Squared Error (MSE): Average squared difference.
    - Root Mean Squared Error (RMSE): Square root of MSE.
    - R-squared (Δ²): Proportion of variance explained by the model.
    - Mean Absolute Percentage Error (MAPE): Percentage-based error.
