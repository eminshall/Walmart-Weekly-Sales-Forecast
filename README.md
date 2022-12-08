# Walmart Weekly Sales Forcast
Creating a model to predict weekly sales at Walmart locations.

The goal of this project is to create a model capable of predicting weekly sales throughout the year across multiple retail locations. Having a model such as this can provide decision support regarding future plans related to stock planning, investments, operations, and accounting.

## Data
This data was sourced from Kaggle and can be found [here](https://www.kaggle.com/datasets/aslanahmedov/walmart-sales-forecast). Although it isn't clear if this data came from Walmart itself, the data reasonably represents any retail company with multiple locations. This data set has 421,570 rows and 16 columns.

## Data Cleaning
Very little cleaning was neccessary. The data and features came split in a few different csv files which were merged. Some of the features included Markdowns which represented discounts at those stores for a certain weeks. For the weeks when there were no Markdowns offered, instead of having a null value I replaced it with 0.

## EDA
From exploring the data we discovered the following insights:

* Weekly Sales are higher on weeks with a holiday. This is noteworthy because in the data the only holidays included were Super Bowl, Labor Day, Thanksgiving/Black Friday, and Christmas. To reiterate, four weeks out of the year generate more sales then the rest of the weeks.
* Most stores follow a pattern of where sales shoot up in the final weeks of the year. The exception are smaller 'Type C' stores which see a downturn and don't see the benefits of holiday sales surges.
* Fuel Price, Temperature, CPI, and Unemployment didn't seem to have much correlation to weekly sales throughout the year. 

## Models
I chose to use regression models for predicting sales in this instance. In the notebook you'll find I used RandomForest Regression, Random Forest Regression with Gridsearch CV, and XGBoost. The winner being Random Forest Regression with Gridsearch CV, having an accuracy score of 99%.

## Future Improvements
In the future I plan on making a predictive model using timeseries techniques by spliting the data by date.
