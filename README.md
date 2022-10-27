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

