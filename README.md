# 📈 Stock Market ETL Pipeline

## Overview

This project is an end-to-end Business Intelligence (BI) solution developed for the MADSC301 Business Intelligence Final Assignment at EU Business School Munich.

The project automatically collects Apple (AAPL) stock market data from the Financial Modeling Prep (FMP) API, processes and cleans the data, stores it in PostgreSQL, and visualizes key insights using Power BI.

The ETL pipeline is automated using Windows Task Scheduler to run daily.

---

## Business Case

Investors and analysts need reliable and updated stock market information to monitor price trends and trading activity.

This project demonstrates how a Business Intelligence system can automatically:

- Collect stock market data
- Clean and transform raw information
- Store data in a database
- Generate analytical dashboards
- Automate updates without manual intervention

---

## Architecture

```
FMP API
   ↓
Extract (Python)
   ↓
Raw JSON Data
   ↓
Transform (Pandas)
   ↓
Clean CSV Dataset
   ↓
Load (PostgreSQL)
   ↓
Power BI Dashboard
   ↓
Windows Task Scheduler (Daily Automation)
```

---

## Technologies Used

### Programming
- Python 3

### Libraries
- Pandas
- Requests
- SQLAlchemy
- Psycopg2
- Python-dotenv

### Database
- PostgreSQL

### Visualization
- Power BI

### Automation
- Windows Task Scheduler

### Data Source
- Financial Modeling Prep (FMP) API

---

## Project Structure

```
stock-market-etl/
│
├── scripts/
│   ├── extract.py
│   ├── transform.py
│   └── load.py
│
├── data/
│   ├── raw/
│   └── processed/
│
├── sql/
│
├── dashboard/
│
├── main.py
├── run_etl.bat
├── requirements.txt
├── README.md
└── .gitignore
```

---

## ETL Process

### 1. Extract

Data is collected from the Financial Modeling Prep API.

Collected fields include:

- Symbol
- Date
- Open Price
- High Price
- Low Price
- Closing Price
- Trading Volume

Output:
- Raw JSON file

---

### 2. Transform

Using Pandas:

- Selected required columns
- Converted data types
- Removed inconsistencies
- Structured dataset for analysis

Output:
- Cleaned CSV dataset

---

### 3. Load

The transformed data is loaded into PostgreSQL for storage and future analysis.

Output:
- PostgreSQL database table

---

## Automation

The ETL process is automated using Windows Task Scheduler.

Schedule:
- Daily execution
- Runs `run_etl.bat`
- Automatically updates stock data

This fulfills the workflow orchestration requirement of the assignment.

---

## Dashboard Insights

The Power BI dashboard provides:

### KPIs
- Highest Closing Price
- Lowest Price
- Total Trading Volume

### Visualizations
- Apple Closing Price Trend
- Trading Volume Trend

---

## Sample Dashboard

The dashboard displays:

- Historical stock price movements
- Trading activity over time
- Key performance indicators

---

## Future Improvements

- Multi-stock analysis
- Real-time streaming data
- Predictive analytics using Machine Learning
- Docker containerization
- Email notifications for pipeline failures

---

## Author

**Abin Benno**

Student ID: 25061274

EU Business School Munich

MADSC301 – Business Intelligence

Spring Semester 2026
