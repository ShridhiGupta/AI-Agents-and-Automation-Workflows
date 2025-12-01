# Automated Daily Stock Data Fetcher & Email Reporter

A scheduled n8n workflow that fetches daily stock data from multiple sources, processes it, stores it in Google Sheets, and sends a summarized email report automatically.

## Features
- Scheduled daily stock price fetching  
- Multiple stock symbols (NIFTY50, TCS, INFY, RELIANCE, etc.)  
- Data merging and transformation  
- Automatic sheet update in Google Sheets  
- Daily summary generation  
- Email notification with clean summary  

## How It Works
1. Daily Schedule triggers the workflow  
2. Stock symbols are prepared and fetched via API  
3. All responses are merged and cleaned  
4. Data is appended to Google Sheets  
5. A daily summary is created  
6. Email report is sent  

## Setup
Import workflow → Add API keys (if required) → Connect Google Sheets & Email → Configure schedule → Activate.


