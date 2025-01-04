# Real-Time-Cryptocurrency-Data-Analysis
Real-time cryptocurrency data collection and analysis using the CoinMarketCap API. It automates data retrieval, processes the data to compute statistical insights such as average percentage changes, and saves the results in a CSV file stored on Google Drive.
This project highlights API integration, data manipulation using Pandas, and automation in Python.

Explanation of the Code and Steps:
Data Retrieval:

  The api_runner function fetches data from the CoinMarketCap API.
  It uses the requests library to send a GET request and retrieve cryptocurrency data in JSON format.
  The pd.json_normalize function flattens the nested JSON structure into a Pandas DataFrame for analysis.

Data Storage:

  The create_csv_gdrive function saves or appends the DataFrame to a CSV file on Google Drive.
  Google Drive is mounted within the Colab environment for file access.

Data Processing:

  The data is grouped by cryptocurrency name using df.groupby.
  Statistical metrics, such as the mean of percentage changes over various time frames, are calculated.
  The stack method converts wide-format data into a long format for better visualization.

Data Transformation:

The reset_index method is used to convert the multi-index DataFrame back into a regular DataFrame.
Column names are replaced with readable labels for ease of interpretation.
Visualization:

A catplot is created using Seaborn to visualize the average percentage change of cryptocurrencies over time.
The hue parameter differentiates data points by cryptocurrency name.
