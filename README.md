# A Data Science Approach to Technical Analysis: Revolutionising Stock Price Prediction with Machine Learning

## Project Overview

This notebook provides a comprehensive program designed to predict stock prices using historical data. By employing advanced machine learning techniques, the program analyzes historical stock price trends and forecasts future stock prices based on past performance.

### Expected Input Files
The program requires historical stock price data in CSV format. Yahoo Finance can automatically download this data. The format of the expected input files should adhere to the standard structure provided by Yahoo Finance, which includes columns such as Date, Open, High, Low, Close, Adj Close, and Volume.

### Automatic Download
The notebook includes functionality to automatically download historical stock data. The tickers and date ranges for the data can be specified directly in the code. The function download_and_process_data(tickers, start_date, end_date, output_dir) is responsible for handling the download and processing of the data:

### 
#### Tickers: List of stock symbols to download data for.
#### Start Date: The start date for the data retrieval period.
#### End Date: The end date for the data retrieval period.
#### Output Directory: Directory where the downloaded data will be saved (train_data, test_data, extra_data)
### Input During Program Run
During the execution of the program, users may need to provide specific inputs, such as:

### Stock Symbol: 
The symbol of the stock for which the prediction is to be made.
### Date Range: 
The date range for the historical data to be considered in the prediction model.
These inputs are typically entered within the code cells of the notebook, where users can modify the parameters as needed.

### Output of the Program
The program produces the following outputs:

### Predicted Stock Prices: 
These predictions are saved in a CSV file. The CSV file will contain the date and the corresponding predicted stock price.
### Graphical Plots:
Visual representations of the data 

### How to Run the Program
### Install Dependencies: 
Ensure all required libraries are installed. You can install the necessary libraries. 

### Configure Parameters:
Modify the tickers and date ranges in the code as per your requirements.

### Execute Notebook Cells:
Run the cells in the notebook sequentially to download the data, train the models, and generate predictions.

### Review Outputs:
Examine the output CSV files and plots to analyze the predicted stock prices.

This README is designed to help users grasp and run the stock price prediction program efficiently. If you have any questions or need information feel free to check out the code and comments, in the notebook. 
