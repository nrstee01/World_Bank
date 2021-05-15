# World Bank Exploration
---


## Goal

To see if taxes can be a reliable predictor for GDP growth.
  

## Data Used

- WorldBankData-https://databank.worldbank.org/indicator/NY.GDP.MKTP.KD.ZG/1ff4a498/Popular-Indicators?l=en#


## Gathering & Cleaning Data
    
The data was gathered from the World Bank using their online DataBank. The World bank has over a thousand features to choose from. I selected features that relate to GDP growth, taxes, and other indicators covering a wide range of categories. Some of the categories include health, education, military, and other economic indicators. I chose countries that were considered high income according to the World bank listing. I did this to have a dataset that had countries with stable economic and political systems to help limit noise. I ended up pulling information on 82 different countries.
  
Upon looking at the data it was evident that many of the features I originally obtained had too many data points missing to use. Many other features had many missing null values and so I shrunk the amount of countries I used to 10. These countries were from europe and shrinking the amount of countries allowed me to make sure I could accurately clean the data and fill null values. I was able to look at the data and see that some features only had information reaching so far back in time. I wanted to look into some of the features that had missing data so I made 3 different data frames. Each data frame went back in time either to 2000, 1990, or 1980. This allowed me to look at some features that did not have data going back as far as 1980.     
  
  
## First Regression Model

After cleaning the data I made a regression model to see how taxes can predict GDP growth. Making a model proved if anything that taxes are terrible at predicting GDP growth.
The scores for the train and test were .054 and -0.073 respectively. The model on the test data was performing worse than the baseline model and the train was not performing that much better.

The correlation coefficient of the tax features the average was -0.016 and seeing the model statistics, using taxes to predict GDP growth was not going to yield a much better result. At this point I started looking at the other features in the data set to see if I could discern any pattern from them.

  
## Additional Feature Exploration

I started looking into the features that were part of the dataframe and began with the features relating to the military. The data showed that the military for all countries were shrinking in size and shrinking in the percentage of GDP was used to fund them. 
  
Seeing the data on healthcare the trend showed that countries were spending more on healthcare over time. The percentage of healthcare spending as a percentage of GDP grew year over. This could be that countries have more money to spend on healthcare or healthcare is getting more expensive. The amount of beds in a hospital per 1000 people conversely shrunk  by almost half in the past 40 years for some countries. While all countries saw so decline in the amount of beds per 1000 people. 
  
The last area I looked at with the data was trade. Trade grew rapidly over the last 40 years. The average trade as a percent of GDP was a little over 60% in 1980. By the end of 2017 that number rose to over 85% of GDP. This was facilitated by a decrease in tariffs. The average tariff rate was 4.5% in 1990 and then decreased to 2% by 2017. The increase in trade also ment a growth in imports for exports. The data showed a strong correlation between GDP growth and growth in imports and exports.  

With the findings I made with the European countries I went back to look at all 82 countries I pulled to see if the pattern holds on a global scale. All of the patterns relating to the military, healthcare, and trade were still prevalent in the global data. 

## New Regression Model  

I made a new model that used annual import growth and annual export growth to try and predict GDP growth. The new model performed much better than the first model using taxes. The new train and test scores were .6 and .56 respectfully. Using only 2 features the model was able to account for almost 60% of the variance in the test data. This leads me to believe that a growing global economy has been the dominant factor for a change in GDP.  

## Conclusion

Starting out the goal was to find out if taxes have a measurable impact on GDP growth. This turned out to not be the case. Taxes were a poor predictor of GDP growth. After exploring additional features from the World Bank it became apparent that global trade dominated growth.
This knowledge can help countries make better policy decisions with regards to world trade.

You can look through the data using interactive maps that I made with the World Bank data with the link provided.
https://public.tableau.com/profile/nicholas.r.steele#!/vizhome/WorldBankData_16209578927590/TradeDashboard

