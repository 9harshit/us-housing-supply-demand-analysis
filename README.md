# US Housing Supply Demand Analysis 

 - Clean and preprocessed data used in this EDA is present in repo ***dataset.csv***
 - Details of preprocessing present in eda2.ipynb file

## Data

 - Data is considered only for period between 2000 and 2018.
 - Unemployment rate is calculated by taking average of values from 2000 to 2018.
 - House price index is from 2000 to 2018 provided by S&P/Case-Shiller U.S. National Home Price Index.

 ***Assumptions***
 - Main objective of this EDA is to find relation between house price index and other factors hence some assumptions are made.

 - More information for the data can be found on US goverment official websites.
   

## Data Analysis

   ### House price index in US over 20 years

   ![Screenshot](https://github.com/9harshit/us-housing-supply-demand-analysis/blob/main/2.png)
   ![Screenshot](https://github.com/9harshit/us-housing-supply-demand-analysis/blob/main/1.png)

   
   - Average hosue price in the country increased steadily over the the before 2008 hosuing crisis.
   - During 2009 house price valuation of the house decreased steeply.
   - Prices kept decresing for next 3 years.
   - Prices started stablising in 2012 and after that kept increasing year by year.

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

  - House price has highest corelation with price per sqaure feet naturally and least with hospital rating in the area.
  - House price have good relation with schools displaying hosue buyers tendacy to buy house near schools.

  - Further plotting also shows that large and poplulus state like Texas and California have highest number of hospitals and school. But Median income of Texas is less than California which is why house prices in Texas is less in comparision California, but more in comparision to other state with similar income. (Diagram present in python notebook.)


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

## Notes 
 - Deeper analysis can be done by income of households, type of families and their background, other factors like type of schools (public or private) etc.
 - Study can be done from city based on aggregate to county and aggregating to analysis state wise trends

***Raw Dataset present in the repo. Only housing unit dataset was created manaully because the file was getting corrupted when imported using pandas***
***ALL dataset are downloaded from official USA government sites
