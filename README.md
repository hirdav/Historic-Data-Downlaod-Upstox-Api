

# Historic Data Download with Upstox API

Here I am able to download Historic Data  using Upstox API. This repository will help you get historical market data for analysis. 


# 📊 Option Chain Data Extraction using Upstox API

This project uses the **Upstox API** to extract  option chain data, retrieve historical data (1 day/30 minute/1 minute intervals), and analyze specific contracts based on exchange, lot size, and expiry dates. The project includes functionality for token-based authentication and handling large data for trading purposes.

## 🚀 Features

- **Access Token Generation**: Authorize the app using the Upstox API for secure data access.
- **Real-time Instrument Filtering**: Select specific instruments and their contracts (e.g., `NSE_FO`, `OPTIDX`) based on lot size and expiry dates.
- **Historical Data Extraction**: Fetch OHLC data (1 day, 1 minute intervals) for selected instruments .
- **Data Saving**: Extracted data can be saved locally in a structured format (CSV).

## 💡 Use Cases

- **Trading Algorithms**: Ideal for integrating real-time and historical data into trading strategies.
- **Market Analysis**: Perform in-depth analysis using real-time and historical option chain data to improve trading decisions.
- **Custom Data Filtering**: Filter based on lot size, expiry date, and price range to analyze specific instruments.

## 🔧 Technologies Used

- **Python**
- **Pandas** for data manipulation
- **Requests** for API calls
- **Upstox API** for data extraction
- **WebSocket** for real-time streaming

## 🛠 How It Works

### 1. Authorization and Token Generation

Authenticate using the Upstox API by generating an access token: go to the file Access token generation

# Go to the python file Access token Generation 

After generating the token, use it for authorized API requests to access option chain data.

### 2. Extracting Instrument Data

Retrieve real-time contract data from `NSE_FO` or `MCX_FO` or NSE Equity , exchanges based on specific parameters such as `lot_size` and `expiry`.

```python
df[(df['exchange'] == 'NSE_FO') & (df['instrument_type'] == 'OPTIDX') & (df['lot_size']==25)&(df['expiry']=='2024-09-19')]
```

### 3. Historical Data (OHLC)

Fetch 1-day or 1-minute OHLC data for the selected instruments:

```python
url = 'https://api.upstox.com/v2/market-quote/ohlc'
```

Use the Upstox API to retrieve historical data for further analysis and storage.

### 4. Save Data Locally

Save the extracted data to a CSV file for future analysis:


## 📚 Documentation
- [Upstox API Documentation](https://upstox.com/developer/api/v2/) - Detailed documentation for API usage.
  
## 🔧 Setup and Usage

### 1. Install Dependencies

```bash
pip install -r requirements.txt
```

### 2. Set Up API Credentials

Add your Upstox `apiKey`, `secretKey`, and `redirectUrl` in the code to authenticate.

### 3. Run the Script

## 🤝 Contributions

Any Contributions are welcome! Fork the repository, submit issues, or create pull requests to add more features or optimize the existing ones.

Thanks.

