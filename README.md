# Financial Ratio Scanner Using Python & Financial Modeling Prep API

## Overview

This project is a Python-based Financial Ratio Scanner that uses the Financial Modeling Prep (FMP) API to retrieve financial data for publicly listed companies and perform ratio-based analysis.

The script automates the process of:

- Retrieving stock listings from Financial Modeling Prep
- Filtering companies listed on major U.S. exchanges
- Identifying companies with available financial statement data
- Extracting annual key financial metrics
- Ranking companies based on the Debt-to-Equity ratio
- Exporting results to Excel for further analysis

---

## Technologies Used

- Python
- Pandas
- Requests
- Financial Modeling Prep (FMP) API
- Excel

---

## Repository Structure

```text
FMP-ratio-scanner/
│
├── fmp_key.py
└── fmp_ratio_scanner.py
```

---

## Files

### fmp_key.py

Stores the Financial Modeling Prep API key.

```python
#!/usr/bin/env python3
# -*- coding: utf-8 -*-

# FMP API key
fmp_key = ''
```

Replace the empty string with your FMP API key before running the project.

### fmp_ratio_scanner.py

Main script responsible for:

- Connecting to the Financial Modeling Prep API
- Retrieving stock listings
- Filtering companies by exchange and asset type
- Retrieving key financial metrics
- Extracting Debt-to-Equity ratios
- Exporting results to Excel files

---

## Workflow

### 1. Retrieve Stock Listings

The script requests stock listing data from the FMP API and loads it into a Pandas DataFrame.

### 2. Retrieve Financial Statement Symbols

The script retrieves a list of companies that have financial statement data available through the API.

### 3. Filter Companies

**Asset Type**
- Stock

**Supported Exchanges**
- NASDAQ
- Nasdaq
- NASDAQ Capital Market
- NASDAQ Global Market
- NASDAQ Global Select
- New York Stock Exchange
- New York Stock Exchange Arca
- American Stock Exchange
- NASDAQ Stock Exchange
- NASDAQ Stock Market
- BATS

### 4. Match Available Financial Statement Companies

The script identifies companies that appear in both:

- Stock listings
- Financial statement symbol lists

Symbols containing "-" are excluded.

### 5. Retrieve Key Metrics

For each selected company, the script retrieves annual key metrics from the Financial Modeling Prep API.

Current filters:

- Calendar Year: 2023
- Period: FY (Full Year)

### 6. Create Financial Dataset

The collected financial metrics are stored in a Pandas DataFrame and exported to:

```text
fs_metrics.xlsx
```

### 7. Debt-to-Equity Analysis

The script extracts:

```text
debtToEquity
```

and sorts companies in descending order.

Results are exported to:

```text
sorted_ratio.xlsx
```

---

## Installation

Install the required packages:

```bash
pip install pandas requests openpyxl
```

---

## Configuration

Add your Financial Modeling Prep API key in `fmp_key.py`:

```python
fmp_key = 'YOUR_API_KEY'
```

---

## Running the Project

```bash
python fmp_ratio_scanner.py
```

---

## Output

The script generates two Excel files:

### fs_metrics.xlsx

Contains the retrieved financial metrics for the selected companies.

### sorted_ratio.xlsx

Contains companies ranked by Debt-to-Equity ratio.

---

## Project Purpose

This project demonstrates:

- API Integration
- Financial Data Processing
- Data Filtering with Pandas
- Financial Ratio Analysis
- Automated Reporting
- Python-Based Financial Analytics

---

## Author

**Rasheeda Sultana**

````

