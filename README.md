# Financial Ratio Scanner Using Python & FMP API

## Overview
Financial Ratio Scanner is a Python-based financial analytics project that automates the extraction, filtering, and analysis of financial metrics for publicly listed companies using the Financial Modeling Prep (FMP) API.

The project retrieves stock listings, filters companies across major exchanges, extracts annual financial metrics, and generates Excel-based reports for ratio-driven financial analysis and stock screening.

---

## Features
- Retrieve stock market data using FMP API
- Filter companies listed on NASDAQ, NYSE, AMEX, and BATS
- Extract annual financial metrics
- Analyze debt-to-equity ratios
- Generate Excel reports automatically
- Perform ratio-based stock screening

---

## Technologies Used
- Python
- Pandas
- Requests
- Financial Modeling Prep API
- Excel Reporting

---

## Project Workflow
1. Fetch stock listings from FMP API
2. Filter stock-type securities and supported exchanges
3. Retrieve financial statement-supported companies
4. Extract annual key metrics
5. Analyze and sort financial ratios
6. Export results into Excel files

---

## Project Structure

```bash
financial-ratio-scanner/
│
├── fmp_key.py
├── ratio_scanner.py
├── fs_metrics.xlsx
├── sorted_ratio.xlsx
├── requirements.txt
└── README.md
