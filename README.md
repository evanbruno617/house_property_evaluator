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

(photo)

Given this data, a multiple linear regression model was constructed to predict Median sales using the variables that had the highest R-squared values. 






