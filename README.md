### Data Mining Project
# Dry Beans Classification
![alt text](https://food.unl.edu/newsletters/images/assorted-dry-beans.png)

Click [here](https://github.com/Ashleshk/Dry-Beans-Classification-Prediction/blob/main/Project_Report_final.pdf) for report.

In this project different machine learning algorithms were used to classify the most well-known 7 types of beans in Turkey; Barbunya, Bombay, Cali, Dermason, Horoz, Seker and Sira, depending **ONLY** on dimension and shape features of bean varieties with no external discriminatory features.

Logistic Regression, Decision Tree, Random Forest, MLP, Xgboost classifiers were trained and a final Neural Network is used resulting Accuracy 94.21% on the training data, 94.91%  on validation set and 0.938 on the final testing set.  

## Table of contents:
### 1-Dataset
### 2-EDA
### 3-Preprocessing
### 4-Model Training
### 5-Result
## Dataset

The dataset provided in this project is obtained from [UC Irvine Machine Learning Repository - Dry Bean Dataset.](https://archive.ics.uci.edu/ml/datasets/Dry+Bean+Dataset)
- **Note**: The data is already splitted with 80% - 20% ratio to training and testing sets respectively, so a part of the data is already separated for final testing and will use the training set for train and validation.

## EDA
- Exploring the dataset, getting summary statistics and checking for null values and duplicates and there weren't any.
- Graphical representations:\
1- Count plot the labels column show the distribution of all classes that showed a slight imbalance but it doesn't affect and no need to handle.\
2- Histogram of numerical features, some distributions have long tails, skewed and most are bi-modal which means that some classes are quite distinct from others.
\
3- Boxplot shows that the "Bombay" & "Horoz" classes are distinct from other classes and that there are some minimal outliers in some features.\
4- The Pearson linear correlation shows that there are lots of highly correlated features.

## Preprocessing
1- Label Encoding the categorical target labels with values from 0 to 6.\
2- Train-Validation split the training dataset with 95% - 5% ratio.\
Now, we have the training set:\
3- Remove outliers from some features with certain threshold.\
4- Feature scaling using StadardScalar()

## Model Training
Logistic Regression, Decision Tree, Random Forest, MLP, Xgboost classifiers were trained on the dataset separately.
- RandomizedSearchCV was used previously in hyperparameter optimization for the models and the best parameters are used directly in this code.
- F1-score and Confusion Matrix  are used to evaluate each model's performance.\

## Result 
On analysing the results from each model, following are some inferences:
- There was no overfitting observed in any of the three techniques used as the accuracy values for training and validation confusion matrices were close to each other.
- All accuracies achieved for the developed classification model were **greater than 85%**.
- It is worthwhile to note that the Accuracy value for the validation partition of **Boosted Tree model was 92.16%** and only marginally lower than the Accuracy value of Neural Network model. 
- Thus, Boosted Tree model may be recommended for classification as an alternative to the Neural Network model


