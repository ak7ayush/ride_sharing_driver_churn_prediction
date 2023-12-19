# Insights

## Insights from Model 1- Decision Tree Classifier:
* Best Hyperparameters are max_depth=5, max_leaf_nodes=15
* The f1 score for predicting leaving the company is 0.96
* The recall score for predicting leaving the company is 0.97
* The precision score for predicting leaving the company is 0.95
* The AUC score for predicting leaving the company is 0.96
* Model Sensitivity:0.97
* Model Specificity:0.89
* The most important features according to model 1:
    * Month of Reporting
    * Year of joining
    * Total Business Value
    * Q_Rating_Inc_Flag
    * Income

## Insights from Model 2- Random Forest Classifier (RF):
* Best parameters are : {'max_depth': 5, 'n_estimators': 50}, score is : 0.97
* Test Accuracy : 0.95
* f1_score : 0.96
* The recall score for predicting leaving the company is 0.95
* The precision score for predicting leaving the company is 0.97
* The AUC score for predicting leaving the company is 0.97
* Model Sensitivity:0.95
* Model Specificity:0.95
* Most important features(highest to lowest): -Month Of Reporting -Total Business Value. -Year of Joining -Quarterly performance increase -Income

## Insights from Model 3-Gradient Boosted Decision Tree (GBDT) Classifier:
* Best hyperparameters:{'subsample': 0.8, 'n_estimators': 250, 'max_depth': 3, 'learning_rate': 0.1}
* The AUC score is 0.97.
* Test Accuracy : 0.96
* f1_score : 0.96
* The recall score for predicting leaving the company is 0.97 versus 0.96 for RF model.
* The precision score for predicting leaving the company is 0.96.
Model Sensitivity:0.97
* Model Specificity:0.91
Top most important features (Highest to lowest):
Month Of Reporting
Year of Joining (driver tenure)
Total Business Value
Income
Quarter Rating Increase



Summary:
Model 3 with the GBDT classifier has better sensitivity but less specificity compared to Model 2 Random Forest Classifier. Slightly different order of feature importances is observed with GBDT.

## Insights from Model 4-XGBoost Classifier:
* XGBoost Best hyperparameters:{'subsample': 0.8, 'n_estimators': 50, 'max_depth': 5, 'learning_rate': 0.1, 'colsample_bytree': 1.0}
* The AUC score for predicting leaving the company is 0.98, an improvement over the previous GBDT model with 0.97.
* Test Accuracy : 0.95
* recall_score :0.96
* precision_score : 0.96
* f1_score : 0.96
* The recall score for predicting leaving the company is 0.97
* The precision score for predicting leaving the company is 0.97
* Model Sensitivity:0.97
* Model Specificity:0.93
* Top most important features:
* Month Of Reporting
* Year of Joining
* Quarterly performance increase
* Total Business Value
* Joining designation
* We obtained the best AUC score of 0.98 with the XGBoost model.


# Conclusion

* It is a no-brainer that the cost of acquiring new drivers is at least 5X the cost of retention. In our analysis we evaluated four tree-based models and can rank them as follows based on their prediction performance metrics:


* Model4 (XGBoost) > Model3 (GBDT) > Model2 (Random Forest) > Model1 (Decision Trees)


* Using the feature importance insights generated from the models, some important predictors of driver attrition are -


* Month and Year of Reporting: Drivers who actively reported into the system every month were less likely to leave. Recommendation: Company should reward such drivers with points. Company can leverage gamification based motivation strategy where drivers rank up through different levels and accumulate points for continued consistency on the system.


* Quarterly Performance Rating Increase: Drivers with an increase in their quarterly rating were more likely to stay with the company. Recommendation: Company should identify the driver profile with low/high quarterly rating and extend loyalty programs that incentivizes performance improvements. Quarterly performance reviews and additional training could be imparted to the drivers whose rating has not increased over the last quarter so that issues can be identified with concerned drivers and attrition can be prevented.


* Total Business Value: This is an important feature in predicting if a driver is going to leave the company or not. Recommendation: The total business value is the total business that a driver generates, the company should set small financial milestones for the drivers to work through. The company should roll out a reward and recognition program for the drivers who meet their milestones.


* Income/Grade: Income plays an important role in predicting the driver attrition. Recommendation: Company should ensure that the drivers have enough opportunities and motivation to increase their monthly average income above a certain threshold. Another option to ease the financial burden on the drivers and increase their morale is to provide vehicle maintenance offers, insurance policies, health checkups, and special education programs etc.