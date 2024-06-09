# Automated-ETL-Pipeline-for-Banking-Data-Analysis

This Python script implements an automated Extract, Transform, Load (ETL) pipeline for analyzing banking data. The pipeline consists of the following steps:

## 1. Data Extraction:
Utilizes web scraping techniques to extract information from a specific Wikipedia page (url) that lists the largest banks.
The extract function retrieves the table under the heading "By market capitalization" from the Wikipedia page and converts it into a Pandas DataFrame.

## 2. Data Transformation:
The extracted data contains market capitalization values in USD.
The transform function converts the market capitalization values from USD to GBP, EUR, and INR based on predefined exchange rates obtained from a CSV file (exchange_rate_csv_path).
The transformed data is added to the DataFrame as new columns representing market capitalization in GBP, EUR, and INR.

## 3. Data Loading:
The transformed data is saved into a CSV file (csv_output_path) for further analysis and visualization.
Additionally, the data is loaded into a SQLite database (db_name) and stored as a table (table_name) using the load_to_db function.
The SQLite database provides a structured storage format for the data, enabling efficient querying and analysis.

## 4. SQL Query Execution:
After loading the data into the SQLite database, predefined SQL queries are executed to perform analysis tasks.
The run_query function runs SQL queries on the loaded database and prints the results.
Example queries include retrieving all records from the table, calculating the average market capitalization in GBP, and selecting a subset of records for further examination.

## 5. Logging:
Throughout the ETL process, progress updates, including timestamps, are logged to a log file (log_file).
Logging facilitates monitoring, debugging, and auditing of the ETL pipeline, providing insights into the execution flow and potential issues.

## Usage:
Clone the repository or download the script.
Ensure that Python and necessary libraries (requests, BeautifulSoup, pandas, numpy, sqlite3) are installed.
Update the url, exchange_rate_csv_path, csv_output_path, db_name, table_name, and log_file variables as needed.
Run the script etl_pipeline_banking.py.
Monitor the progress and review the output CSV file and SQLite database for the transformed data.
Analyze the data using SQL queries or other tools as needed.

## Dependencies:
requests,
BeautifulSoup,
pandas,
numpy,
sqlite3.


## Author:
Manideep Elasagaram






