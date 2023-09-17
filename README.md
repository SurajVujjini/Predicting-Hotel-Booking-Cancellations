# Prediciton of Hotel Booking Cancellations
## Introduction
Hotels thrive on advance reservation systems. This can both be a good thing and bad thing for the hotels. The good thing is that hotels now get more reservations than normal due to ease of booking. Bad thing is that due to the current completive market, hotels need to have an easy cancellation policy for guests. This makes it hard for hotels to estimate the actual demand and also forecast demand. The average percentage of canceled reservations is 24%. Cancellations effect the revenue of the hotel will lose potential revenue customers who will not cancel.

As a part of the project, I will be  analyzing bookings data from Microtel BWI and will be creating a model to predict if the reservation will cancel or not. This can help the hotel forecast the future revenue and also help price the rooms accordingly. 

## Youtube Link:
Prediction of hotel booking cancellations - https://youtu.be/qN8_ObvJ2Ak

## Aim of the Project
The main aim of this project is to create a model that finds reservations that have a high chance of getting canceled.

## About the dataset
No. of rows – 36,275

No. of columns – 19

Total number of values  - 689,225

This dataset does not have any null values, this is very rare for a dataset to have in the real world. I have requested this dataset from Microtel BWI, the absence of null values could be due to the fact that this dataset was sent over by the data management team from Wyndham. I clearly still do not know why there are no null values in this dataset. 

The absence of null values can be seen in this SNS heatmap.

![image](https://user-images.githubusercontent.com/90857782/167941430-bdfab31b-e561-44d4-8727-d5c16fc994d7.png)

## Data Modification and Analysis
I have used multiple plotting tools like seaborn, matplotlib top plot and analyze the data. Plotting can be a simple but very effective way to get the meaning out of the data.

I have encoded the “booking_status” column so that it is included in the correlation heatmap. This is because correlation function only works on integer data.

I have also created two columns which contain price slabs and lead time slabs. This is done because the values form price and lead time columns are very distinct and high in count. Sorting them into well defined slabs simplifies the process.

## Columns in the dataset after necessary modifications
![image](https://user-images.githubusercontent.com/90857782/167941552-429f55ff-da25-45cb-828b-b6d7f114a1ea.png)

## Classification
I have applied total of 4 classification models on the dataset. These are:
1. Logistic Regression
2. Decision Trees
3. Random Forest
4. Gradient Boosting 

I have chosen Logistic regressor classifier as it is one of the simplest, very fast and effective classification algorithms. Decision trees and random forest are a little complicated but highly effective as well and require comparatively low computational power to run. Gradient boosting is very complicated and also required very high computational power to run. I have tried to apply KNN and SVM on this dataset but was failed as my system was not able to handle them.

Of all the classifiers, I found that Random Forest to have high accuracy and also required less time to run. Here is the classification report from the Random Forest classifier. 

![image](https://user-images.githubusercontent.com/90857782/167941840-f254c17b-676a-46ae-adb6-305c2ca9b5b5.png)

## Conclusion
The main aim of this project was to identify reservations which have a higher chance of getting canceled. Using this random forest model, the hotel can get a pretty good idea of demand and manage rooms accordingly. This model helps to find the reservations which are made by guests who are unsure about thier stay and make resrervation just in case they come. 
