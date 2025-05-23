# Big Data Final

## Model 1: Random Forest
- The random forest model utilizes PySpark and its random forest, labeled point, multiclass metrics, vectors, and when libraries
- The code starts off by initalizing the spark session and reading the data
- Since its in a csv format, the data is initially taken in as a dataframe
- Using the when library, we encode the M and Bs in the target column into 1 and 0 into a new 'label' column
- Then we gather the feature columns (every column that isn't the id, label, or diagnosis column)
- Using the vectors library, we create labeled points consisting of the label and a vector of all the feature columns
- The data is split into 70% training and 30% testing set
- A random forest classifier is built and trained on the data
- Using the test set, we gather predictions and zip with the labels
- Multiclass metrics allows us to calculate the accuracy, precision, recall and f1 score as well as a confusion matrix
