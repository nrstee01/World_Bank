# World_Bank
---


## Goal
  To see if taxes can be a reliable predictor for GDP growth.
  

## Data Used
- WorldBankData-https://databank.worldbank.org/indicator/NY.GDP.MKTP.KD.ZG/1ff4a498/Popular-Indicators?l=en#


## Gathering & Cleaning Data
    
  The data was gathered from the from the World Bank using their online databank. The World bank has over a thousand features to chose from. I selected features that relate to GDP growth, taxes, and other indicators covering a wide range of categoryies. Some of the categories include health, education, military, and other economic indicators. I chose countries that were consider high income according to the World bank listing. I did this to have a dataset that had countries with stable economis and political systems to help limit noise. I endend up pulling information on 82 diffrent countries.
  
  Upon looking at the data it was evedint that many of the features I origonalay obtained had too many data points missing to use. The other features had many missing null values and so I shrunk the amount of countries I used to 10. These countiries were from europe and shrinking the amount of countries allowed me to make sure I could more accuratly clean the data and fill null values. I was abled to look at the data and see that some features only had information reaching so far back in time. I wanted to look into some of the features that had missing data so I made 3 diffrent data frames. Each dataframe went back in time either to 2000, 1990, or 1980. this allowed me to look at some feature that did not have data going back as far as 1980.     
  
  
## First Regression Model
  After cleaning the data I made a regresstion model to see how taxes can predict GDP growth. Making a model proved is anything that taxes are terible at predicting GDP growth.
The scores for the train and test were .054 and -0.073 respectivly. The model on the test data was preforming worse than the baseline model and the train was not preforming that much better.

Looking at the correlation coefficient of the taxe features the average was -0.016. Looking at the correlation coefficients and the model statistics using taxes to predict GDP growth was not going to yeild a much better result. AT this point I started looking at the other features in the data set to see if I could decern any pattern from them.

  
## Addtional Feature EDA
  I started looking into the features that were part of the dataframe and began with the features relating to the military. The data showed that the military for all countries were shrinking in size and shrinking in the percentage of GDP was used to fund them. 
  
  Seeing the data on healthcare the trend showed that countries were spending more on healthcare over time. The percentage of healthcare spendening as a percentage of GDP grew year over. This could be that countries have more money to spend on healthcare or healthcare is getting more expensive.
  
  The last area I looked at with the data was trade. Trade grew rapidly over the last 40 years. The average trade as a percent of GDP was a little over 60% in 1980. By the end of 2017 that number rose to over 85%. This was facilitated be a decrease in tariffs. The average tariff rate was 4.5% in 1990 and then decreassed to 2% in in 2017. The increase in trade also ment a growth in imports for exports. The data showed a strong corelation between GDP growth and growth in imports and exports.  

## New Regression Model  
I made a new model that used annual import growth and annual export growth to try and predict GDP growth. The new model preformed much better than the first model using taxes.
## Conclusion
  The model had very few legal terms that were the top influencers on the model. The model was deciding on other factors when determining its prediction. This leads me to believe that how legal problems are solved are very similar. https://public.tableau.com/profile/nicholas.r.steele#!/vizhome/WorldBankData_16209578927590/TradeDashboard

