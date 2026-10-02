# FIN 239 - Coding Assignment #2

**Course**: FIN 239 - Financial Data Analytics  
**Semester**: Fall 2026  
**Due Date**: Tuesday, September 29, 2026 at 11:59 PM  
## Assignment Overview

This assignment tests your ability to work with financial data from various sources and platforms. You will familiarize yourself with Bloomberg Terminal and Capital IQ, and use Python to retrieve data from multiple remote sources including Ken French Data Library, FRED, Nasdaq Data Link, and WRDS.


## Learning Objectives

By completing this assignment, you will:

- Gain proficiency with professional financial data platforms (Bloomberg Terminal and Capital IQ)
- Master Excel add-in functionality for dynamic financial dashboards
- Develop skills in retrieving financial data programmatically from multiple sources
- Understand differences between data platforms and their respective strengths
- Apply best practices for reproducible data workflows

## Prerequisites

- Python 3.8 or higher
- Jupyter Notebook
- pandas library
- Access to Bloomberg Terminal (student account)
- Access to Capital IQ (student account)
- Access to WRDS (student account)
- nasdaqdatalink, pandas_datareader, or fred libraries

## Part 1: Bloomberg Terminal (20%)

Familiarize yourself with the Bloomberg Terminal and its data analysis capabilities.

### 1. Create Bloomberg Account (0%)
Set up your Bloomberg Terminal student account.

**Instructions:**
1. Create an account on the Bloomberg Terminal using your student email address
2. Join our class group (Use the Class Code on Canvas)

### 2. Build Financial Metrics Dashboard with Bloomberg Excel Add-in (20%)
Create a comprehensive Excel workbook with live Bloomberg data functions.

**Instructions:**
1. Create a comprehensive Excel workbook replicating the structure and data from resources/sample_financial_metrics.md
2. Use Bloomberg Excel functions (BDH, BDP, etc.) to populate all available metrics with live data
3. Design the workbook to allow easy ticker changes through a single input cell
4. Implement best practices: named ranges for the ticker symbol, dynamic formulas that update when ticker changes, proper data validation and error handling, professional formatting and layout matching the sample structure
5. Include a documentation sheet explaining any notes to help explain your work
6. Test your workbook with at least 3 different stock tickers to demonstrate functionality
7. Save as bloomberg_dashboard.xlsx


## Part 2: Capital IQ (15%)

Familiarize yourself with the Capital IQ platform for financial data and analysis.

### 1. Create Capital IQ Account (0%)
Set up your Capital IQ student account.

**Instructions:**
1. Create an account on Capital IQ using your student email address

### 2. Install the Capital IQ Excel Add In (5%)
Install and configure the Capital IQ Excel Add-in for data access.

**Instructions:**
1. Log into Capital IQ
2. Under the 'My Profile' → 'Downloads' section, download the Capital IQ Excel Add In
3. Install the Capital IQ Excel Add In

### 3. Build Financial Metrics Dashboard with Capital IQ Excel Add-in (10%)
Create a comprehensive Excel workbook with live Capital IQ data functions and compare with Bloomberg approach.

**Instructions:**
1. Create a comprehensive Excel workbook replicating the structure and data from resources/sample_financial_metrics.md
2. Use Capital IQ Excel functions to populate all available metrics with live data
3. Design the workbook to allow easy ticker changes through a single input cell
4. Implement best practices: named ranges for the ticker symbol, dynamic formulas that update when ticker changes, proper data validation and error handling, professional formatting and layout matching the sample structure
5. Include a documentation sheet explaining your Capital IQ functions and methodology
6. Test your workbook with at least 3 different stock tickers to demonstrate functionality
7. Compare and contrast the data availability and functionality differences between Capital IQ and Bloomberg approaches
8. Save as capitaliq_dashboard.xlsx


## Part 3: Python Data Retrieval (65%)

Use Python to gather data from remote sources. Each of these requirements must be completed using Python code.

### 1. Ken French Data Library (15%)
Retrieve and process Fama-French factor data from Ken French's Data Library.

**Instructions:**
1. Review Ken French's Data Library: https://mba.tuck.dartmouth.edu/pages/faculty/ken.french/data_library.html
2. Create a Pandas data frame from the 'Fama/French 3 Factors' weekly data using the 'TXT' file format
3. Create a Pandas data frame from the 'Fama/French 3 Factors' daily data using the 'CSV' file format
4. These two files should be accessed directly from French's website
5. Save the results of each query to a CSV file in the data/ folder: ff3_factors_weekly.csv and ff3_factors_daily.csv

### 2. FRED (15%)
Retrieve economic data from the Federal Reserve Economic Data (FRED) database.

**Instructions:**
1. Create a Pandas data frame with historical consumer price index (CPI) data
2. Create a Pandas data frame with historical producer price index (PPI) data
3. Create a Pandas data frame with historical real gross domestic product (GDP) data
4. This data may be accessed remotely using the 'fred' or 'pandas_datareader' modules we covered in class
5. Reference the St. Louis Fed's FRED website (https://fred.stlouisfed.org) to locate the appropriate data series
6. Save the results of each query to CSV files in the data/ folder: fred_cpi_data.csv, fred_ppi_data.csv, fred_gdp_data.csv

### 3. Nasdaq Data Link (15%)
Access and retrieve stock and fundamental data from Nasdaq Data Link.

**Instructions:**
1. Print a list of all the tickers that are included in the free sample of the Sharadar Equity Prices data
2. Create a Pandas data frame using the Sharadar Equity Prices data with historical stock data for ticker 'NKE'
3. Create a Pandas data frame using the Core US Fundamentals Data with historical financial results for ticker 'NKE'
4. This data should be accessed remotely using the 'nasdaqdatalink' module we covered in class
5. Reference the Nasdaq Data website (https://data.nasdaq.com/search) to locate the appropriate data series
6. Save the results of each query to CSV files in the data/ folder: nasdaq_nke_prices.csv and nasdaq_nke_fundamentals.csv

### 4. WRDS (20%)
Access CRSP and Compustat data from WRDS using both get_table and raw_sql methods.

**Instructions:**
1. Using the get_table method, download the 'CRSP Monthly Stock' data from WRDS, retrieving the following columns: permno, date, ret, vol, prc, and shrout while restricting the data to 5,000 rows
2. Using the get_table method, download the 'Compustat Fundamentals Quarterly' data from WRDS, retrieving the following columns: gvkey, datadate, at, lt, revt, and ni
3. Using the raw_sql method, download the 'CRSP Monthly Stock' data from WRDS for the year 2022 for the following tickers: 'AAPL', 'MSFT', 'AMZN', 'GOOGL', 'TSLA'
4. Using the raw_sql method, download the 'Compustat Fundamentals Quarterly' data from WRDS for the year 2022 for the following tickers: 'AAPL', 'MSFT', 'AMZN', 'GOOGL', 'TSLA'
5. Save the results of each of these queries to CSV files in the data/ folder: wrds_crsp_monthly_sample.csv, wrds_compustat_quarterly_sample.csv, wrds_crsp_2022_stocks.csv, wrds_compustat_2022_stocks.csv
6. Note: you may need to perform intermediate steps to accomplish the raw_sql queries



## Project Structure

```
Assignment-2/
├── README.md                 # This file - assignment instructions
├── assignment2_student.ipynb # Your completed assignment notebook
├── bloomberg_dashboard.xlsx  # Bloomberg Excel dashboard (Part 1)
├── capitaliq_dashboard.xlsx  # Capital IQ Excel dashboard (Part 2)
├── data/                     # Folder for CSV files from Python data retrieval
│   ├── ff3_factors_weekly.csv
│   ├── ff3_factors_daily.csv
│   ├── fred_cpi_data.csv
│   ├── fred_ppi_data.csv
│   ├── fred_gdp_data.csv
│   ├── nasdaq_nke_prices.csv
│   ├── nasdaq_nke_fundamentals.csv
│   ├── wrds_crsp_monthly_sample.csv
│   ├── wrds_compustat_quarterly_sample.csv
│   ├── wrds_crsp_2022_stocks.csv
│   └── wrds_compustat_2022_stocks.csv
└── resources/
    └── sample_financial_metrics.md

```

## Submission Requirements

- Complete the assignment in the provided Jupyter notebook template
- Ensure all code runs without errors from start to finish
- Include clear comments and explanations for your code
- For Part 1, submit your Bloomberg Excel dashboard file (bloomberg_dashboard.xlsx) with live Bloomberg functions, documentation sheet, and evidence of testing with multiple tickers
- For Part 2, submit your Capital IQ Excel dashboard file (capitaliq_dashboard.xlsx) with live Capital IQ functions, documentation sheet, evidence of testing, and comparison analysis with Bloomberg
- For Part 3, demonstrate successful data retrieval from each source

## Other Assignment Requirements

### References (-35% penalty)
You must cite any external references you use to help produce your code. These citations can be simple and need not follow any formal citation pattern. It is best to place the references as comments near the places in your code that were most influenced by them. The key tasks in this assignment should not be copied verbatim from any outside source. If you did not use any outside resource then cite your own knowledge or experience. **Failure to cite will add up to a 35% penalty to the assignment.**

### Readability (-20% penalty)
Your code must be readable and easy to follow, using comments when necessary. **Failure to produce readable code will add up to a 20% penalty to the assignment.**


## Suggested Resources

- Module 2 lecture notebooks and materials
- Bloomberg Terminal documentation
- Capital IQ platform help resources
- Python documentation: https://docs.python.org/3/
- Course materials on Canvas

## Academic Integrity

This is an individual assignment. While you may discuss general concepts with classmates, all code and analysis must be your own work.

