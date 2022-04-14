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


   

