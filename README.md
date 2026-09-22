# Project 1: Exploratory Data Analysis of Historical Stock Market Data

## Overview

This project focuses on the exploratory analysis of historical stock market data. The main purpose of the project was to understand the structure of real-world financial data, check its quality, clean inconsistent records, explore the numerical and categorical variables, and identify patterns and unusual observations.

The analysis was carried out using Python, Pandas, NumPy, Matplotlib and Seaborn.

## Objectives

The main objectives of this project were to:

- Load and understand the historical stock datasets
- Examine the structure and data types of the datasets
- Identify missing values and duplicate records
- Check for duplicate ticker and date combinations
- Convert the date column to datetime format
- Explore categorical variables such as exchange and sector
- Calculate descriptive statistics for numerical variables
- Investigate unusual stock-price observations
- Create visualizations to understand the distributions
- Analyze the closing price of one selected stock
- Develop possible questions and hypotheses for future analysis

## Datasets

Two datasets were used in this project:

### historical_stocks.csv

This dataset contains information about stocks and securities, including:

- ticker
- exchange
- name
- sector
- industry

### historical_stock_prices.csv

This dataset contains daily stock trading information, including:

- ticker
- open
- close
- adj_close
- low
- high
- volume
- date

The two datasets are connected using the `ticker` column.

## Tools and Libraries

The following Python libraries were used:

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## Data Preparation

The datasets were loaded into Pandas DataFrames and examined using functions such as:

- `head()`
- `shape`
- `info()`
- `describe()`
- `isnull()`
- `duplicated()`

The date column was converted to datetime format to make time-based analysis easier.

I also checked for duplicate rows and duplicate ticker-date combinations.

During the data-quality checks, some records contained inconsistent relationships between the open, high, low and close prices. These records were investigated and excluded from the cleaned analysis because they did not satisfy the expected OHLC structure.

Unusually high stock prices were not automatically removed. They were investigated separately because an unusual financial value is not necessarily an error.

## Exploratory Data Analysis

The analysis included both categorical and numerical exploration.

For categorical data, I examined:

- Stock exchanges
- Stock sectors

For numerical data, I examined:

- Open price
- High price
- Low price
- Close price
- Trading volume

Descriptive statistics such as the mean, median, standard deviation, minimum, maximum and quartiles were used to understand the numerical variables.

## Key Findings

The historical stock price dataset contains a very large number of daily observations covering several decades.

The mean closing price was approximately **76.1140**, while the median closing price was approximately **15.45**.

The difference between the mean and median indicates that the closing-price distribution is strongly affected by higher-valued observations.

Trading volume showed a very large amount of variation across the dataset.

The closing-price and volume distributions were both strongly skewed, and the boxplots showed a number of extreme observations.

## Unusual Observations

Several securities produced unusually high closing-price observations, including:

- SCON
- CODA
- TVIX

These observations were investigated rather than automatically deleted.

The adjusted closing price was also examined separately because it can differ from the normal closing price as a result of historical adjustments.

This was important because unusually large financial values should be investigated before deciding whether they represent errors.

## Visualizations

The project includes visualizations for:

- Securities by exchange
- Securities by sector
- Closing-price distribution
- Trading-volume distribution
- Closing-price boxplot
- Trading-volume boxplot
- Average monthly closing price
- AAPL closing price over time

These visualizations helped to confirm the patterns identified through the descriptive statistics.

## Individual Stock Analysis

For the individual-stock analysis, I selected **AAPL (Apple)**.

The closing-price series shows substantial changes over time, including periods of lower and higher prices. There are also gaps between some dates because stock markets do not trade every calendar day.

To explain major movements in the stock price in more detail, additional information such as company announcements, earnings results, economic conditions, market events and corporate actions would be required.

## Future Questions and Hypotheses

Two questions that could be investigated in a future project are:

1. Does trading volume change significantly during periods of large movements in closing prices?

2. Do stocks from different sectors show different levels of price volatility over the same period?

## Conclusion

This project provided practical experience working with a large real-world financial dataset.

The analysis involved loading and understanding the datasets, checking data quality, cleaning inconsistent records, investigating unusual observations, calculating descriptive statistics and creating visualizations.

The results show that historical stock data can contain highly skewed price and volume distributions and extreme observations. These observations should be investigated carefully rather than automatically removed.

The findings from this project provide a foundation for more advanced analysis of stock-market behaviour, including volatility, trading volume, sector differences and relationships between market variables.
