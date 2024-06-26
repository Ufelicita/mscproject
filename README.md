# Stock Price Prediction_v2

This repository contains a script to download historical stock data for multiple ticker symbols and save the data to CSV files. The script is designed to be run in Google Colab.

## Libraries Used

- `yfinance`: For downloading historical stock data.
- `pandas`: For data manipulation.
- `os`: For file and directory operations.

## Setup and Usage

### Script to Download Historical Stock Data

The following script downloads historical stock data for specified ticker symbols and saves the data to CSV files in a specified directory. This script includes all the necessary steps, including mounting Google Drive and installing required libraries.

```python
from google.colab import drive
import os
import yfinance as yf

# Mount Google Drive
drive.mount('/content/drive')

# Install yfinance
!pip install yfinance

# FTSE100 Stock Price Prediction

This project downloads, processes, and merges historical stock data for selected FTSE100 companies, preparing it for future stock price prediction analysis.

## Features

- Downloads historical stock data for multiple FTSE100 companies using yfinance
- Processes and cleans the data, keeping only relevant columns
- Merges data from different stocks into a single DataFrame
- Handles errors and missing data gracefully
- Compatible with Google Colab for easy cloud-based execution

## Dependencies

- yfinance
- pandas
- os
- datetime

## Usage

1. Mount Google Drive (if using Google Colab):

from google.colab import drive
drive.mount('/content/drive')

2. Install required libraries:

!pip install yfinance

3. Import necessary libraries:

import yfinance as yf
import pandas as pd
import os
from datetime import datetime, timedelta

4. Use the `download_and_process_data` function to download, process, and merge stock data:

def download_and_process_data(tickers, start_date, end_date, output_dir):
    # Function implementation...

# Example usage:
tickers = ['BATS.L', 'CCH.L', 'LAND.L', 'SVT.L', 'GLEN.L', 'RR.L', 'RTO.L', 'SGE.L', 'LGEN.L', 'SN.L']
start_date = '2014-01-01'
end_date = '2023-12-31'
output_dir = 'historical_data'

merged_df = download_and_process_data(tickers, start_date, end_date, output_dir)

## Data Processing

The `download_and_process_data` function:
- Creates a directory to store the CSV files
- Downloads data for each ticker symbol
- Processes each dataset, keeping only the 'Date' and 'Adj Close' columns
- Renames the 'Adj Close' column to the stock ticker name
- Merges all processed datasets into a single DataFrame

## Output

The function returns a merged DataFrame containing:
- Date
- Adjusted closing prices for all specified stocks

Individual CSV files for each stock are also saved in the specified output directory.

