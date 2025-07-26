# 📈 PSX Historical Data Scraper

This project is a simple and beginner-friendly **Python script** that scrapes historical stock market data from the **Pakistan Stock Exchange (PSX)** and saves it to a **CSV file**.

> Getting PSX data in CSV format can be frustrating — this script automates the process so you can download clean, structured data with just a few lines of code.

---

## What This Project Does

- Scrapes **daily trading data** for multiple days using a **date range**
- Extracts:
  - Symbol
  - LDCP (Last Day Closing Price)
  - Open, High, Low, Close
  - Change & Change %
  - Volume
- Adds:
  - The date of the data
  - The timestamp when it was scraped
- Saves the final result to a **CSV file (`psx_data.csv`)**

---

## Who Should Use This?

This project is perfect for:
- Finance students or researchers
- Data analysts
- Python beginners
- Anyone who needs easy access to PSX market data without copy-pasting manually

---

## How to Use This in Google Colab

> You don’t need to install anything locally — it runs 100% online!

### Step 1: Open the Notebook
Open the Google Colab notebook (or copy this script into a new notebook).

### Step 2: Set Your Date Range
At the top of the code, adjust:
python <br>
- start_date = datetime.strptime('2025-07-20', '%Y-%m-%d')
- end_date = datetime.strptime('2025-07-25', '%Y-%m-%d') 
Set any range of dates you want to scrape. <br>

### Step 3: Run All Cells
Click Runtime > Run All or run cells one by one. The script will:<br>
- Scrape each date (excluding weekends)
- Log which days were scraped
- Skip days with no data (like holidays)
- Save the full data to psx_data.csv

Step 4: Download CSV
After scraping is complete, download the psx_data.csv file from the Colab file browser on the left panel.

### Features
- Fully automated scraping 
- Supports scraping for any valid date range
- Skips weekends and market-closed days
- Saves data in clean tabular format
- Beginner-friendly and well-commented code

### Technologies Used
- Python
- requests – for HTTP requests
- BeautifulSoup – for parsing HTML
- datetime – for date range logic
- csv – for exporting data

### Limitations
- The PSX website may change its structure in the future. This script is based on its current HTML layout.
- This script does not use Selenium, so it might not work if the site becomes fully JavaScript-based.
- Data may not be available for weekends or public holidays — those days are automatically skipped.
<br>
