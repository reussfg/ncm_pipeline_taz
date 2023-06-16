# Data Engineering Pipeline

This repository contains a data engineering pipeline that extracts, transforms, and loads data into an Azure SQL database. The pipeline is written in Python and utilizes various libraries and Azure services.

## Prerequisites

Before running the pipeline, ensure that you have the following:

- Python installed on your machine
- Azure Blob Storage account and connection string
- Azure SQL Server and database details
- Required Python libraries installed (pandas, requests, pyodbc, sqlalchemy)

## Pipeline Steps

The pipeline consists of the following steps:

1. Data Extraction: The pipeline connects to the data source and retrieves the required data. It uses the `requests` library to download data from external URLs.

2. Data Transformation: The extracted data is transformed using pandas and various data cleaning operations. Columns are selected, data types are converted, and additional columns are created based on calculations and mappings.

3. Data Storage: The transformed data is stored in a CSV file named `dados.csv`. This file serves as an intermediate storage before uploading the data to Azure SQL.

4. Data Loading: The pipeline establishes a connection to the Azure SQL database using the provided credentials. It creates an SQLAlchemy engine and uses it to upload the CSV data to the specified table in the database.

## Usage

To run the pipeline, follow these steps:

1. Set the necessary configurations in the script:
   - Set the `server`, `database`, `username`, and `password` variables with your Azure SQL Server details.
   - Update the `table_name` variable with the desired table name in the Azure SQL database.
   - Ensure you have the required Python libraries installed.

2. Execute the script: Run the script in a Python environment. Make sure you have an internet connection and the necessary access rights to download data and connect to Azure SQL.

3. Monitor the execution: The script will display logs and progress messages in the console. Ensure that there are no errors during data extraction, transformation, and loading.

4. Verify the results: Once the script completes successfully, check the Azure SQL database to ensure that the transformed data has been loaded into the specified table.

## Note

For security purposes, sensitive information such as connection strings and credentials has been omitted from this public script. Make sure to replace the placeholders in the script (`your_server_name`, `your_database_name`, `your_username`, `your_password`, `your_table_name`) with your actual Azure SQL Server details.

## License

This project is licensed under the [MIT License](LICENSE).

Feel free to customize and extend the pipeline to suit your specific requirements.
