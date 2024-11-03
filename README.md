# BreakoutAi

This project retrieves historical price data for popular cryptocurrencies, calculates metrics, and uses a machine learning model (LSTM) to predict future prices. The data is sourced from the CoinGecko API and is saved in an organized Excel workbook, where each cryptocurrency’s data is stored in a separate sheet.

## loom link : 

```
https://www.loom.com/share/ba9991743efd479982839c5b5b5e6b6a?sid=c49990f0-247b-4cdf-8d0a-93661ba28dee
```



## Project Overview

 This project is designed to:

 1. Fetch daily historical price data for selected cryptocurrencies (e.g., Bitcoin, Ethereum, Dogecoin) using the CoinGecko API.
 2. Calculate metrics like highs and lows over specified timeframes.
 3. Used an LSTM (Long Short-Term Memory) model to predict future prices based on historical trends.
 4. Save each cryptocurrency’s data to a separate sheet in an Excel workbook for easy access and analysis.



## Features

- API Data Retrieval: Fetches up to 365 days of historical data for each selected cryptocurrency.
- Metric Calculations: Calculates important metrics (e.g., rolling highs and lows).
- Price Prediction: Uses an LSTM model to predict future high and low prices based on historical data.
- Excel Export: Organizes data in an Excel workbook with separate sheets for each cryptocurrency.


## Machine Learning Model

The project uses an LSTM (Long Short-Term Memory) neural network model for time-series forecasting. LSTMs are well-suited for time-series data like cryptocurrency prices, as they can capture long-term dependencies and trends in sequential data.


## Model Structure

- Input Layer: Accepts the historical price data with rolling metrics.
- LSTM Layers: Two LSTM layers to capture temporal dependencies, each followed by a Dropout layer to prevent overfitting.
- Dense Layer: Final layer to output the predicted future prices (high and low).

The model is trained on historical data and uses a look-back period (e.g., 30 days) to predict the future high and low prices.


## API Reference

#### Base URL

```http
  https://api.coingecko.com/api/v3
```


#### Endpoint: Get Historical Market Data for a Cryptocurrency

Fetches daily historical price data for a cryptocurrency.

```http
  GET /coins/{id}/market_chart
```

Endpoint: 
```http
  /coins/{id}/market_chart
```

Full URL: 
```http
  https://api.coingecko.com/api/v3/coins/{id}/market_chart
```

Path Parameters



| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `id`      | `string` | **Required**. CoinGecko ID of the cryptocurrency (e.g., bitcoin). |


Query Parameters


| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `days`      | `number 'or '   string ` | **Required**. CoinGecko ID of the cryptocurrency (e.g., bitcoin). |



## Installation


#### Prerequisites

Ensure you have Python installed. Install the required packages by running:

```bash
pip install pandas openpyxl requests tensorflow
```
    
