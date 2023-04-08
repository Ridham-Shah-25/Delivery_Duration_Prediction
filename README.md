I used The Historic Dataset of DoorDash to predict the total time taken from order being placed on DoorDash to the order being delivered to the customer.I Divided the project into 4 parts-
# Data Exploration
I imported the CSV File into Pandas and explored the features in this dataset. I formatted some columns and created some new features,which I felt would be more useful. For variables with lesser unique values,I formed dummy variables.At the end,I removed the rows with Nan values

# Collinearity and Removing Redundancies
I used Heatmap to find collinearity and tried to remove redundant pairs and made sure that no 2 features were highly correlated

# Multicollinearity and Feature Selection
I found out MultiCollinearity from Variance Inflation Factor(VIF) method and removed features with high VIF values. Then,I did Feature Selection by sorting The Features by Gini-importance and selecting the top few features for model building

# Classical Machine Learning
I used 3 different Scalers,3 Feature Sets and 5 different Machine Learning Algorithms for finding the best Model which fits my Dataset. I used RMSE score for evaluating my models

# Results
The Best Models I found used Feature-set of top-15 features(sorted by Gini-Importance) and were scaled by Standard Scaler.The results are-
RMSE of: LinearReg 986.6913337271566
RMSE of: Ridge 986.6913337315796
RMSE of: DecisionTree 1233.5450488189838
RMSE of: RandomForest 1284.0594398152712
RMSE of: XGBoost 1067.5736725258685
RMSE of: LGBM 1032.6011551522938

Clearly,Linear and Ridge Regression Models are the ones which fit our dataset the best.
