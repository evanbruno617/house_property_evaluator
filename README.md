# House Property Evaluator
---
# Purpose
---
The purpose of this project is to analyze how gdp of each county can affect certain aspects such as time it takes to sell, percent change in sales, median price of home sales, and amount of unsold inventory of houses.

# Gathering Data
---
I first obtained the gdp of each county by scraping data from https://california.reaproject.org/data-tables/gsp-a200n/tools/60001/ in [Scrape](https://github.com/evanbruno617/house_property_evaluator/blob/main/scraper.ipynb). I obtained the Median Sales, Median time it takes for houses to sell, Percent change in sales, and amount of unsold inventory of houses by downloaded excel files providing this data on a monthly basis

# Cleaning Data
---

In order to provide analysis on this data I had to clean the excel files to get rid of unecessary data and obtain only annual data since the gdp data is given on an annual basis.

# Analysis
---

After cleaning the data analysis for linearity between industries and housing data was done. The first step was finding the correlation between each industry and the housing data. For example, for Median Sales the table depicts the coefficient of correlation and the R-sqaured value beside it.

![Sales[](medianprices.png](https://github.com/evanbruno617/house_property_evaluator/blob/main/Resources/medianprices.png)

Given this data, a multiple linear regression model was constructed to predict Median sales using the variables that had the highest R-squared values. 

Out of these values above, Finance and insurance, Construction, Retail trade, [Finance, insurance, real estate, rental, and leasing], and Construction was chosen for the multiple linear regression. They were chose because they are the top 5 variables with the highest R^2 values. When peforming the multiple linear regression with these variables this model is obtained. 

![Sales[](medianprices.png](https://github.com/evanbruno617/house_property_evaluator/blob/main/Resources/price_lin.png)

A coefficient of 0.998668 is obtained with a R^2 values of 0.592084 which is good values to obtain for this analysis. This data is using the sales data from December of every year from 2001 - 2022. It finds the relationship between the change in these variables variables year over year and the change in the median price of houses year over year in Decemeber. 

## Using Sum
---
The above data is only using the data from Decemeber of each month. Another hypothesis to be tested if there is a better correlation when taking the same of the total prices of each year. By performing the same analysis as before, it was found that Information and Construction have the highest R^2 values so this was used in the multiple linear regression. After performing the multiple linear regression this was the results.

![pic](https://github.com/evanbruno617/house_property_evaluator/blob/main/Resources/Sum_price.png)

This therefore shows that there is a high correlation between change in total prices for a year and the change in the performance  of Information and Constructing sectors of each county. This model has 68% of its variation explained by these variables.

Another Data to note is that on its own, construction has a coefficent of 0.94 with an R^2 value of 0.65 therefore acting as a great linear relationship with Median House prices.

# Conclusion
---

By peforming Linear regression analysis throughout these counties it is discovered that there is a high correlation between certain sectors and the change in median prices of houses in each county. This new found discovery can be used in the future to help predict prices of houses by predicting and forecasting the change in these sectors contributing to gdp in each county. 










