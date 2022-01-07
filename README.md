# Credit-Card-Default-Prediction
NAME - ANMOL SALUJA
COLLEGE - IIT (BHU) , Varanasi

Project - Amex CodeLab : Credit Card Fraud Detection

Max Score Achieved - 92.59291/100

WORK DONE ON JUPYTER NOTEBOOK USING PYTHON 3.8.

LIBRARIES USED - pandas,numpy,imbalance, XGBoost

APPROACH AND TECHNIQUES USED - 

1. The data was passed through Exploratory Data Analysis Techniques and Preprocessing techniques, such as mean imputation and max value count imputation for missing data.Furthermore,
   categorical data was converted to encoded data via two methods (Label Encoding and One-hot-encoding). Label Encoding provided better accuracy on test set (92.59 vs 92.22).

2. Redundant features were removed and the variance explained by the features was analysed using PCA. Features were then transformed with a 13-component PCA model.

3. Since the labels were highly imbalanced, SMOTE and RandomUnderSampling was attempted to rectify the balance of the dataset. However, it resulted in a highly 
   reduced test accuracy.

4. The features and labels were then passed into a GridSearch model for XGBoost Classifier. Following features were tweeked for optimizing the F1 score -
    'max_depth':range(3,7,2),
    'gamma':[i/10 for i in range(0,4)],
    'reg_alpha':[1e-5, 1e-2, 0.1, 1, 100],
    'eta': [i/100 for i in range(0,100)]
        
5. Following the GridSearch model results and several randomized trials, a test accuracy of 92.59291 was achieved on a XGBoost model using the following 
   parameters - 
     max_depth = 6
     reg_alpha = 100
     gamma = 0.3
     eta = 0.204 

6. Finally, the result was exported to a csv file.
