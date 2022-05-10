# Data 602 Final Project:

## Dataset:
   Dataset is referenced from Chicago data portal "https://data.cityofchicago.org/Transportation/Traffic-Crashes-Crashes/85ca-t3if" for the year 2022 with 9568 rows and 49 columns.
   
## Project Proposal / Business outcome:
  Traffic accidents are responsible for most of the deaths. Especially, in USA there are millions of deaths reported every year. Injuries during the accident depends on the several aspects like road conditions, weather conditions, road defects, speed limit, device conditions and light conditions in particular street. So, I am working on the dataset of Chicago for prediction of injuries and no injuries during traffic accidents due to various conditions in the year 2022. 

## Exploratory Data Analysis:
  EDA is used for analyse and take insights from the data. Imported libraries for loaded dataset using pandas library. Shape of the dataset is observed with columns information to analyse the data types, standardization of column names, analysed duplicate rows in the dataset, Later analysed missing values in the columns in which more than 90% of the null values in the columns are detected and removed.Correlation for the dataset is observed.
  ![image](https://user-images.githubusercontent.com/95875120/163471568-d0099b7e-dc4d-41ab-85ba-0e126e3b66fd.png)
 Columns with high correlated data are removed. then outliers for the columns in data are detected using Inter quartile range, which is handled in modeling.
 #### Visualization:
 The severity of crashes is visualized with pie chart 
 ![image](https://user-images.githubusercontent.com/95875120/163472010-72ae9026-4b04-4e45-b75b-0978104152de.png)
 
Later, observed several conditions for the injuries and no injuries during the crashes.
![image](https://user-images.githubusercontent.com/95875120/163472130-bc87f370-08af-4256-b30b-c2b8a92309a1.png)

During my analysis, I observed that most of the crashes happened in febrauary and on saturdays of the year, especially on the weather conditions of clear weather followed by snow, most of the crashes reported based on the primary and secondary resons are unknown. The crashes happened on the dry road with no control on the device especially on the West part of the Chicago city. The most of the crashes reported are when the speed condition is 30 and in the streets of western Ave.


   
## Modeling:
The process of modeling started from cleaning the data with unwanted columns that includes columns with missing values of more than 90%, columns providing the correlation of greater than or equal to 70%, outliers numerical columns that affecting the dataset and the skewness in the dataset by calculating the upper limit and lower limit and comparing with Interquartile range. Later in the feature processing, the steps followed by me is initially dividing the cleaned and dropped dataset into numerical and categorical columns. Then, splitting the datasets into train and test samples with a split of 20%, imputing the numerical columns with 'median' after analysing from the EDA and standard scaling the data instead of minmaxscaler because standard scaler provides better performance and then impting the categorical data with most frequent values and encoding the data with binary 0 and 1. Finally transforming the data through column transformer for modeling. As my target variable is binary class which is imbalanced and categorical type. 

![image](https://user-images.githubusercontent.com/95875120/167613722-5fb24e5a-ee84-4945-a5ea-265c3f9fc2c2.png)


So, choosing logistic regression instead of linear regression because linear regression cannot perform regression on categorical variable and with decision trees classification for fitting the model, analysing the overfit in the model with accuracy scores and loss function.

#### Logistic regression:

![image](https://user-images.githubusercontent.com/95875120/167613930-5bbc4038-08ab-4047-8d2b-7e6daed45b4a.png)

#### Decision trees:

![image](https://user-images.githubusercontent.com/95875120/167613981-d50dd196-f913-4208-a66c-6285f31e0805.png)

Among them, the overfitting and impurity issues are found to be higher in the case of decision trees as compared with the logistic regression.

Then the number of components for dimension reduction with PCA of threshold greater than 95% is found with components as 27, then with k means clustering 13 optimal clusters are found with elbow method.

![image](https://user-images.githubusercontent.com/95875120/167614911-a17a32ec-8e00-429f-ad66-cdf5e60ed4f1.png)

Due to the overfitting issues, best components for logistic regression and decision trees with several combinations including pca and kmeans found that the logistic regression performing better than the decision trees.

## Conclusion:
   In conclusion, from both EDA and modeling, the severity of injuries are more in case of "No Injury" and models are % accurate in predicting the severity of injuries and the reasons for the severity during crashes can be reduced by the analysis of weather, device condition, lightning, particular street, road condition. In future, the precautions in driving during several external factors helps in mitigating the severity of injuries during the vehicle crashes.
