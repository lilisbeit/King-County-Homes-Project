# King-County-Homes-Project



## Overview
A large real estate firm in the Seattle area is seeking to maximize prices for home sellers. My task is to use data from previous home sales to predict future prices.

## Business Problem
The real estate firm operates throughout King County, which includes the metropolis of Seattle, as well as suburban and rural areas. Home prices vary greatly between these diverse landscapes, as well as between neighborhoods in Seattle. The firm needs to accurately price a home based on data such as its size, location, and number of bedrooms, in order to get the best sale price for its clients. It needs a model that can generate a good estimate of value for any home in the county.

## Data Understanding
To build a model to predict prices, I used data from the King County House Sales dataset, which can be found here:

(https://www.kaggle.com/harlfoxem/housesalesprediction)

This dataset contains information on over 21,000 houses sold in King County between May, 2014 and May, 2015. Although the median sale price is $450,000, the dataset also includes multi-million dollar homes. At the top of the market are about 1,000 properties which sold between $1.2 million and $7.7 million, so the price data are right-skewed with a few very high outliers.

In addition to sale price, the dataset includes details about the homes, including square footage, lot square footage, number of bedrooms, zip code, and the dates when the houses were built, renovated, and sold. Although the data seem mostly accurate, some values are missing, and many columns have outliers on the high side.

## Analysis



## Conclusions

To accurately price homes in King County, the real estate firm should use a model that segments zip codes into price-based categories, such as Model 8. This model combines data about house features that are highly correlated with price, such as square footage, with knowledge of the mean house prices of each zip code, to produce predictions that explain 83% of the variance from the mean price. Model 8 is a significant improvement over the baseline regression model, which only explains 63% of the variance. In addition, while the baseline model's predictions were an average of $136K off from the actual prices of the test data, Model 8's Mean Absolute Error was only $87K for the test data.

Square footage and grade have the strongest positive correlation with price, but the model vastly improved after zip code classifications were included. Unsurprisingly, location seems extremely important to home buyers in the Seattle area, which is a diverse landscape that includes, urban, suburban, and rural neighborhoods.

Much work remains to investigate potential improvements to this model. In particular, including interactions among X variables may increase the model's accuracy. Since square footage and zip code are such powerful predictors of price, perhaps an interaction between these variables would enhance the model. Also, since zip code classification was so effective in improving the model, perhaps including a few more zip classes would help by segmenting the market even further.

In addition, the month when the house was sold may affect price, and was not tested in these models. Also not tested was a feature that would indicate whether the house was recently renovated, for example in the past 20 years. It may also help to programmatically iterate through the X-variables to select the best features for inclusion in the model.