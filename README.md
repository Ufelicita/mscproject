# Stock Price Prediction

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

def historical_data(tickers, start_date, end_date, output_dir='historical_data'):
    """
    Downloads historical stock data for multiple ticker symbols and saves to CSV files.

    Parameters:
    - tickers (list): Ticker symbols to download.
    - start_date (str): Start date for data in 'YYYY-MM-DD' format.
    - end_date (str): End date for data in 'YYYY-MM-DD' format.
    - output_dir (str): Directory to save CSV files.

    Returns:
    - None. Saves CSV files in the specified directory.
    """
    os.makedirs(output_dir, exist_ok=True)

    for ticker in tickers:
        print(f'Downloading data for {ticker}...')
        data = yf.download(ticker, start=start_date, end=end_date)
        if not data.empty:
            file_path = os.path.join(output_dir, f'{ticker}_historical_data.csv')
            data.to_csv(file_path)
            print(f'Data for {ticker} saved to {file_path}')
        else:
            print(f'No data found for {ticker}')

# List tickers to download data
tickers = ['BATS.L', 'LAND.L', 'SVT.L', 'GLEN.L', 'RR.L', 'RTO.L', 'SGE.L', 'CCH.L', 'PHNX.L', 'SN.L']

# Set start and end dates for historical data
start_date = '2013-01-01'
end_date = '2023-12-31'

# Set directory to save CSV files
output_dir = 'FTSE100_historical_data'

# Print current working directory
print("Current Working Directory:", os.getcwd())

# Call the function to download data
historical_data(tickers, start_date, end_date, output_dir)


