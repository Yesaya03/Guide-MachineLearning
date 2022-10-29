# Machine Learning

Machine learning is the use and development of **computer systems** that are able to **learn and adapt** without following explicit instructions, by using **algorithms and statistical models** to analyze and draw inferences from **patterns in data**. <br>

## Machine Learning Workflow

<img width="558" alt="image" src="https://user-images.githubusercontent.com/96195171/198821925-3c2ed5cb-aed1-4a3a-a793-98c1b62cbe90.png">

## Data Profiling <br>
Data profiling is the process of examining the data available from an existing information source and collecting statistics or informative summaries about that data. <br>

In practice, there are some things that are generally done most often, including: <br>

1. Display Dataset Preview <br>
Data preview can be displayed with `df.head()` to display the first 5 (default) rows and all columns in the source object. We can also see the last 5 rows in the dataset by using `df.tail()`

2. Display Dataset Info <br>
To get info/short description of the data, we can use `df.info()` function. So we can find out the number of columns, the number of rows, the data type of the column, and the number of non-null data. This is very useful when doing exploratory data analysis.

3. Checking Missing Value <br>
In order to check missing values in Pandas DataFrame, we can use a function `isna()`. This function help in checking missing values in dataset.

## Data Cleansing <br>
Data cleansing or data cleaning is the process of detecting and correcting corrupt or inaccurate records from a record set, table, or database and refers to identifying incomplete, incorrect, inaccurate or irrelevant parts of the data and then replacing, modifying, or deleting the dirty or coarse data. <br>

In data cleansing, we can do several things, for example: <br>

1. Handling Missing Values <br>
One way to deal with missing values (NaN – Not numbers) is to fill them with any value using the `fillna()` method.pandas. However, the values ​​that are often used to fill in the blank data are usually the mean, median, or mode of each column.

2. Customize the appropriate data type <br>
We can check the data type of each column, then if there is a column that has a data type that does not match, we can change it.

## Exploratory Data Analysis <br>
Exploratory Data Analysis (EDA) is an approach to analyze the data using visual techniques. It is used to discover trends, patterns, or to check assumptions with the help of statistical summary and graphical representations.

1. Data Description <br>
Before exploring the data, we can see a brief summary of the dataset using the `describe()` method. The `describe()` function applies basic statistical calculations to the dataset so that it can give a good idea of the distribution of the data.

2. Numerical Data Visualization <br>
KDE is used to create probability density visualizations of continuous and non-parametric data variables.

3. Categorical Data Visualization  <br>
A barplot shows the relationship between numeric & categorical variables. In the example, each categorical variable is represented as a bar with its count value representing its numeric value.

4. Heat Map Correlation <br>
Heat Map is graphical representations of data that utilize color-coded systems. The primary purpose of Heat Maps is to better visualize the volume of locations/events within a dataset and assist in directing viewers towards areas on data visualizations that matter most.

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
And Then, we use scikit learn with the `ExtraTreesClassifier()` module. This module can tell which features most influence on the data tested.

3. Train Test Split

Train Test Split is the process of dividing the percentage between the data training and the data testing.\
For example:\
`X_train, X_test, y_train, y_test = train_test_split(X, y, train_size = 0.8, random_state = 48)`

## Machine Learning Linear Regression

Linear regression is an attempt to model the relationship between two variables by fitting a linear equation to observed data, where one variable is considered to be an explanatory variable and the other as a dependent variable.

1. Simple Linear Regression

Simple Linear Regression is a type of Regression algorithms that models the relationship between a dependent variable and a single independent variable.

2. Multiple Linear Regression

Multiple linear regression is a statistical technique that uses multiple linear regression to model more complex relationships between two or more independent variables and one dependent variable

## Time Series Forecasting

The data included in the time series type can then be plotted based on time. Forecasting is implemented to observe patterns from the data and determine the analysis steps.

To do use Time Series Forecating, we can use new library from prophet `from prophet import Prophet`

## Cross Validation

statistical methods that can be used to develop models or algorithms where data is separated into two subsets namely the learning process and data validation/evaluation.

to do cross validation we can use new library from sklearn 
`from sklearn.model_selection import cross_val_score`

## Hyperparameter Tuning and Evaluate Model

hyperparameter ledger is a method to determine the best parameter content in an algorithm in a machine learning. When using an algorithm without entering any parameters, the algorithm will use the default parameters that have been previously used by the program.

for example in Linear Regression Algoritm, in default the parameter will filled with :
- fit_intercept `True`
- normalize `False`
- copy_X `True`
- n_jobs `None`
- positive `False`

but with `GridSearchCV` we can find the best model for the parameters put in the algorithm by adjusting the `x_train` and `y_train`

and result best model for parameter in Linear Regression parameter is :
- fit_intercept `True`
- normalize `True` (values change)
- copy_X `True`
- n_jobs `None`
- positive `True` (Values Change)


and MAPE will decrease from `0.34839227351370355` to `0.3483922735137035`
