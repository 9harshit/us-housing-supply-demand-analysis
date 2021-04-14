# US Housing Supply Demand Analysis 

 - Clean and preprocessed data used in this EDA is present in repo ***dataset.csv***
 - Details of preprocessing present in eda2.ipynb file

## Data

 - Data is considered only for period between 2000 and 2018.
 - Features : House Price Index, Mortgage Index, Rental Price, Housing Units in Nation, Unemployment Rate, Average Family Income. All these factors affect the supply and demand of the House price in nation.
 - House price index is from 2000 to 2018 provided by S&P/Case-Shiller U.S. National Home Price Index.

 ***Assumptions***
 - Main objective of this EDA is to find relation between house price index and other factors hence some assumptions are made by taking yearly average and considering monthly values to constant for a year.


 - More information for the data can be found on US goverment official websites.
   

## Data Analysis

   ### House price index in US over 20 years

   ![Screenshot](https://github.com/9harshit/us-housing-supply-demand-analysis/blob/main/2.png)
   ![Screenshot](https://github.com/9harshit/us-housing-supply-demand-analysis/blob/main/1.png)

   
   - Average hosue price in the country increased steadily after 2011, after reducing steeply because of 2008 housing crisis.
   - Prices started stablising in 2011 and after that kept increasing year by year.
   - Increase in Unemployment and reduction in average family income led to decrease in house price
   - No. of house built between 2008-2012 are low in comparision to no. house built before and after this time period.
   - Rental price of house was not affected by factor and kept increasing year by year, with only slight reduction during 2009-2010 period.

   ### Average Rent in US over 10 years

   
   - Trends of the rental price has been same in 2010 to 2017.
   - Rent increased in mid-year and decreased towards the end of the year.
   - This trend can be the result of end of summer break, starting of college sem and students moving. Families tend to shift during this time of year

   ### Co relation between features

   ![Screenshot](https://github.com/9harshit/us-housing-supply-demand-analysis/blob/main/co.png)

    The correlation between a house price index and the Mortgage Rate Index rating is: -0.49503029190690134
    The correlation between a house price index and the Average Family Income is: 0.4189612042909276
    The correlation between a house price index and the Average Rent Index is: 0.7450782835496872
    The correlation between a house price index and the Average Unemployment Rate is: -0.29934893638623483
    The correlation between a house price index and the No of Housing Units is: 0.7576064599077678

  - House price index has highest positive corelation with units of houses in nation, with increase in houses on market prices increase, indicating with that even though there was dip in house price after 2008 crisis people felt housing market was still a good investemnt choice
  - House price index have negative corelation with Mortgage rate, with increase in Mortgage rate, demand reducese hence house price reduces.
  - Increase in House price index also lead to increase in rent prices. 
  - House price index has negative corelation with unemployment rate. Since people have no jobs, demand reduces hence price of houses reduces.


## Model Building

  - The data is split into train and tests sets with a test size of 20%.
  - Models performance is measured using R2 score.

  - Model used :
     - Linear Regression
     - Random Forest Regressor
     - Xgboost

 - Model performance :

    - Linear Regression: R2 Score = 0.61
    - Random Forest Regressor: R2 Score = 0.85
    - Xgboost: R2 Score = 0.60

 - Random Forest is the best model for this dataset because few values are index (trend based movement and not actual values)  while others are actual values, because random forest creates mutplie trees to create a yes no structure based on probability, it must be able to deduce the connection in more deeper manner.

## Notes 
 - Deeper analysis can be done by income of households, type of families and their background, other factors like type of schools (public or private) etc.
 - Study can be done from city based on aggregate to county and aggregating to analysis state wise trends.
 - Tracking future or current developments in an area can also help in predicting future house price treds.

***Raw Dataset present in the repo. Only housing unit dataset was created manaully because the file was getting corrupted when imported using pandas***
***ALL dataset are downloaded from official USA government sites
