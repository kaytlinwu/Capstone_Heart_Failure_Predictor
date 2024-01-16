# Capstone_Heart_Failure_Predictor

# Introduction
Cardiovascular disease is the leading cause of death worldwide.  

The purpose of this project was to create a model to predict for heart disease using 11 clinical features: Age, Sex, Chest Pain Type, Resting BP, Cholesterol, Fasting Blood Sugar, Resting ECG, Max Heart Rate, Exercise Angina, Old Peak, and ST Slope. The data for this project was provided from https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction

# EDA/Feature Engineering
- Relatively clean dataset. 
- Cholesterol values of 0 were found within the dataset. Because this is not a physiologically permissible value, median imputation was performed.
- Variables were not strongly correlated to each other
- Standard scalar was applied and categorical variables were converted to numeric values

# Modelling
- 3 models were applied to the dataset which include SVM, Logistic Regression and XGBoost Classification. All models were hypertuned to try to optimize parameters.
- Model evaluation included accuracy, precision and recall score along with model specific evaluation such as AUC-ROC curve and confusion matrix for logistic regression and plotting the hyperplane for SVM. 

# Model Comparison Results
## SVM
    - Accuracy: 0.8391304347826087
    - Precision: 0.8560606060606061
    - Recall: 0.8625954198473282

## Hyperparameter-tuned SVM
    - Accuracy: 0.8478260869565217
    - Precision: 0.8582089552238806
    - Recall: 0.8778625954198473

- Hyperparameter-tuned SVM using a linear kernel had better accuracy, precision, and recall score compared to the default model.

## Logistic
    - Accuracy: 0.8521739130434782
    - Precision: 0.8592592592592593
    - Recall: 0.8854961832061069
The ROC AUC curve shows that the model has a 85% of correctly distinguishing between patients with heart disease vs. patients without heart disease.
The Confusion Matrix demonstrated the number of correct predictions with 80 true positives (TP), 19 false positives (FP), 116 true negatives (TN), and 15 false negatives (FN). 
    
## Hyperparameter-tuned Logistic
    - Accuracy: 0.8521739130434782
    - Precision: 0.8592592592592593
    - Recall: 0.8854961832061069
- The tuned and non-tuned models yielded the same result. The parameter that differs from the tuned and non-tuned model is the addition of L2 penalty to the hyperparameter tuned model. Though a penalty is added, the model performance does not improve. 

## XGBoost Classifcation 
    - Accuracy: 0.8434782608695652
    - Precision: 0.8571428571428571
    - Recall: 0.8702290076335878

# Conclusion and Further Directions
3 ML models were investigated to predict for heart disease using 11 clinical features. Of the models tested, Logistic Regression had the best overall performance with an accuracy score of 85.22%, precision score of 85.93%, and recall score of 88.55%. 

Further direction includes expanding the dataset since the used for this project is quite small to perform ML modelling. All ML model analyzed are limited by the total number of samples, so acquiring more data is critical to tuning the models. For the scope of this project, only 3 ML models were used. As a result, additional ML models could be used to investigate whether there are more applicable models that are of better performance including ensemble models. Finally, further feature engineering could be used to leverage medical knowledge to connect parameters for more in-depth analysis. 

