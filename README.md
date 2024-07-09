# A Data Science Approach to Technical Analysis: Revolutionising Stock Price Prediction with Machine Learning

## Project Overview

In this ongoing project, I am exploring how data science and machine learning techniques can enhance traditional technical analysis for stock price prediction. While  focusing on selected FTSE100 companies, I aim  to develop a more accurate and robust prediction model than conventional methods.

## Project Versions

### Version 1: Initial Data Collection

In this version, the following was done :
- Set up the basic structure for data collection
- Implemented a `historical_data` function to download stock data
- Saved data to CSV files in a specified directory
- Implemented error handling and informative output

### Version 2: Data Processing and Merging

Building on the first version, the following modifications were made and further steps were added as shown below  :
- Refined the data collection process
- Implemented a `download_and_process_data` function that:
  - Downloads data for multiple stocks
  - Processes each dataset (keeping only 'Date' and 'Adjusted Close')
  - Merges all processed datasets into a single DataFrame
- Updated the list of FTSE100 companies being analyzed
- Set the date range from 2014-01-01 to 2023-12-31

### Version 3: Exploratory Data Analysis (EDA)

In this version, I added comprehensive EDA capabilities:
- Implemented a `perform_eda` function to analyze the merged dataset
- Added visualizations including:
  - Stock prices over time
  - Correlation heatmap
  - Distribution of daily log returns
  - Cumulative returns
- Calculated key financial metrics such as:
  - Average log returns
  - Cumulative returns
  - Sharpe ratios
  - Skewness and kurtosis of returns
 
## Current Data and Analysis
I am currently analysing the following FTSE companies: 

1. BATS.L (British American Tobacco)
2. CCH.L (Coca-Cola HBC)
3. LAND.L (Land Securities Group)
4. SVT.L (Severn Trent)
5. GLEN.L (Glencore)
6. RR.L (Rolls-Royce Holdings)
7. RTO.L (Rentokil Initial)
8. SGE.L (Sage Group)
9. LGEN.L (Legal & General Group)
10. SN.L (Smith & Nephew)

## In-Depth Analysis of Exploratory Data Analysis (EDA) Results

###  Data Quality and Completeness

The  dataset showed excellent quality:
- No missing values across all stocks
- No duplicate rows

This means our data was complete and clean, providing a solid foundation for  analysis and future modelling.

###  Descriptive Statistics

Looking at the summary statistics:

a) Price Ranges:
   - BATS shows the highest average price (2327.03) with a range from 1509.61 to 3410.24
   - GLEN has the lowest average price (259.22) ranging from 52.58 to 540.28

This wide variation in price ranges suggests a  need to normalize the  data when building predictive models to ensure all stocks are treated equally regardless of their price scale.

b) Volatility (Standard Deviation):
   - SVT shows the highest absolute volatility (std: 456.93)
   - LGEN shows the lowest absolute volatility (std: 37.09)

However, to get a true sense of the relative volatility, further EDA would be conducted to calculate the Coefficient of Variation (CV) for each stock.

### 3. Returns Analysis

a) Average Log Returns:
   - RTO leads with 0.0587% daily return
   - RR is the only stock with a negative average return (-0.0108%)

This however suggests RTO has been the best performer in terms of consistent growth, while RR has struggled.

b) Cumulative Returns:
   - RTO shows an impressive 314.92% return over the period
   - RR has the lowest cumulative return at 25.15%

These figures represent the total return if  the stock was held  for the entire period. RTO investors would have more than quadrupled their money, while RR investors would have gained only a quarter.

### 4. Risk-Adjusted Performance

Sharpe Ratios:
   - RTO leads with 0.580292
   - RR has a negative Sharpe ratio (-0.057185)

The Sharpe ratio measures return per unit of risk. RTO offers the best risk-adjusted returns, while RR's negative ratio suggests it is  not compensating investors for the risk they are taking.

### 5. Return Distribution Characteristics

a) Skewness:
   - Most stocks show negative skewness, with RTO being the most negatively skewed (-1.084099)
   - RR is the only stock with positive skewness (0.891731)

The negative skewness suggests more frequent small gains but occasional large losses. RR's positive skewness indicates the opposite: frequent small losses but occasional large gains.

b) Kurtosis:
   - RTO has the highest kurtosis (21.138360)
   - SVT has the lowest kurtosis (3.973709)

The high  kurtosis observed  indicates more frequent extreme events (both positive and negative). RTO's high kurtosis suggests it is  prone to more dramatic price movements, while SVT appears more stable.

