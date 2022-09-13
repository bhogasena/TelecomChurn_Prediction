# Predict the Churning Customers of Telecom Operator

In the telecom industry, customers are able to choose from multiple service providers and actively switch from one operator to another. In this highly competitive market, the telecommunications industry experiences an average of 15-25% annual churn rate. Given the fact that it costs 5-10 times more to acquire a new customer than to retain an existing one, customer retention has now become even more important than customer acquisition.

For many incumbent operators, retaining high profitable customers is the number one business
goal. To reduce customer churn, telecom companies need to predict which customers are at high risk of churn. In this project, you will analyze customer-level data of a leading telecom firm, build predictive models to identify customers at high risk of churn.

This project is to build a machine learning model that is able to predict churning customers based on the features provided for their usage.
     
## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)

## General Information
Required to create a classification model to predict whether users are going to churn or not based on the dataset provided.

Telecom Users Usage Dataset [here](https://github.com/bhogasena/TelecomChurn_Prediction/blob/main/train (1).zip) and Data dictionary [here](https://github.com/bhogasena/House-Price-Prediction/blob/main/data_dictionary.csv).

## Conclusions
# Final Inferences

- Dataset has total of 170+ features and many of them are highly correlated as per EDA.
- Done the PCA for Dimensionality reduction.
- Tried to create different classiifcation models, Logisitic Regression, Decison Tree, Random Forests and XGBoost.
- Random Forest Classifier(Model 7) is good choice for Predicting Churn customers with more accuracy 91.3% and also less False Negatives and more False Positives.    (i.e. if compnay want to retian more users this would be good choice), as it predicts more customers as churn.
- XGBoost (Model 8) has overall high accuracy of 93.124% and has tarde-off between False Positives and False Negatives, it will not verpredict the users going to churn compared to model 7.
- Logistic Regression (Model 5) has highest recall rate compared to all other models, that means this model can be used to if cusotmer wants to redict as many customers as possible that are going to churn and so they can take actions by giving some offers etc.

#### Below are the few recommendations to Operator as per EDA and Model Feature Importances.

- If User didn't make any calls in continuous months (feature name: inactive derived from NaN of onnet and offet mous), there are very high chances of churning.
- If there are less number of outgoing calls comapred to previous months avearge, then there are high chance of churning.(feature name: total_og_mou)
- Users who are making more onnet calls comparted total calls, there are high chances of churning.(derived feature: onnet_mou_per)
- Users are making less offnet calls compared to total calls, there are less chances of churning. (derived feature: offnet_mou_per)
- Users who have not bought any data packs, night packs, extra data etc, in latest months compared to revious aveerage there are high chances of churning. (derived feature: no_extra_pack_)
                          

## Technologies Used
- numpy - version 1.21.6
- matplotlib - version 3.2.2
- seaborn - version 0.11.2
- plotly - version 5.5.0
- statsmodels - version 0.10.2
- sklearn - version 1.0.2

## Contact
Created by [@bhogasena] - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
