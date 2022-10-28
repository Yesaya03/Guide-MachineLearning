# Machine Learning

## Feature Engineering

In feature engineering, we can perform a transformation for machine learning modelling needs. Machine learning only accepts numeric data. All data types are converted into numeric form to enter machine learning modelling. The process of converting data types into numeric formats is called feature engineering.

There are several ways to convert type data non-numeric into type data numeric:

1. Converts categorical data to numeric data

This way, it is often referred to as **_One Hot Encoding_**. We can use syntax `get_dummies()` with parameters: data, prefix and drop_first\
Note:
* **prefix** : String to append DataFrame column names. Pass a list with length equal to the number of columns when calling get_dummies on a DataFrame. Alternatively, prefix can be a dictionary mapping column names to prefixes.\
* **drop_first** : Whether to get k-1 dummies out of k categorical levels by removing the first level.

2. Converts ordinal data to numeric data

This way,  We can use syntax `map()` 

3. Standardize or equalize the value of an integer.

To normalize the value of a variable in data to be balanced, we can use `StandardScaler`. Keep in mind, that `StandardScaler` does not change values or data, only normalizes data.

## Pre-Processing

In Pre-Processing has several stages:

1. Feature Selection

At this stage, we determine which columns will include in the modelling.\
Use`drop()` function to delete a column in a data

2. Feature Importance

At this stage, we distinguish the data we want to include in the x variable (training data) and the y variable (test data).\
Next stage, we use scikit learn with the `ExtraTreesClassifier()` module. This module can tell which features most influence on the data tested.

3. Train Test Split

Train Test Split is the process of dividing the percentage between the data training and the data testing.\
For example:\
`X_train, X_test, y_train, y_test = train_test_split(X, y, train_size = 0.8, random_state = 48)`

## Machine Learning Modelling

In Pre-Processing has several stages:

1. Feature Selection

At this stage, we determine which columns will include in the modelling.\
Use`drop()` function to delete a column in a data

2. Feature Importance

At this stage, we distinguish the data we want to include in the x variable (training data) and the y variable (test data).\
Next stage, we use scikit learn with the `ExtraTreesClassifier()` module. This module can tell which features most influence on the data tested.

3. Train Test Split

Train Test Split is the process of dividing the percentage between the data training and the data testing.\
For example:\
`X_train, X_test, y_train, y_test = train_test_split(X, y, train_size = 0.8, random_state = 48)`
