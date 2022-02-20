# Risky-Business
Machine-Learning: Unit 11

## Background: 
In this assignment I was tasked to build and evaluate several machine learning models to predict credit risk using data you'd typically see from peer-to-peer lending services.I employed different techniques for training and evaluating models with imbalanced classes. I used the imbalanced-learn and Scikit-learn libraries to build and evaluate models using the two following techniques.

---

*Resampling models used:*

1.Naive Random Oversampling

2.SMOTE Oversampling

3.Undersampling(ClusterCentroid)

4.SMOTEENN 

*Ensemble Methods used:*

1.Balanced Random Forest Classifier

2.Easy Ensemble Classifier

---
## How:
Each model had a very similar set up. I first had to read in the data and make sure every column (besides our target) had numerical values. Thus I used Pandas .get_dummies function to achieve this. This would take columns with categorical data and turn it into dummy variables. This would allow me to scale the data. Scaling basically normalizes the training and testing data so the results aren’t skewed when using the models to predict credit risk. From here all steps were the same with the exception of which model/sampling method I used. First I would create variables for the features (X) and target (y), then split them into training and testing sets using the train_test_split function (from sklearn). I would then scale the data from here. The training sets would be used to train and fit the models and the testing sets would be used to see how accurate the model was. 

For the resampling notebook, I would resample data (using multiple methods) so the training data would be balanced (have no bias), then I would run it through the simple logistic model. 
I would then use the classification report (from imblearn) and balanced accuracy score (from sklearn) to determine which model was the best.

For the ensemble notebook it was even simpler since I didn’t have to resample the data.  
I would simply run the scaled data using a specified ensemble classifier. Then use the same steps as before, by creating a model, fitting and training the training data with the model created, then analyzing it using classification report and accuracy score via the testing data. 

---

## Results:
--- 

# Resampling models:

*Which model had the best balanced accuracy score?*
The SMOTE model and SMOTEENN model have the same scores, but are the highest scores. Both had an accuracy score of 0.9946680739911509

*Which model had the best recall score?*
The Undersampling Cluster Centroids model had the best recall score, which was .9945
(Most models had a very good recall score, over .98)

*Which model had the best geometric mean score?*
Similarly with accuracy score, the SMOTE model and SMOTEEN model have the same and highest geometric mean score. Both had a geeometic score of .9947

# Ensemble models:

*Which model had the best balanced accuracy score?*
Easy Ensemble Classifier had the best balanced accurcy score with a score of .925

*Which model had the best recall score?*
Easy Ensemble Classifier had the best recall score with a score of .943

*Which model had the best geometric mean score?*
Easy Ensemble Classifier had best Geometric mean score with a of .925


