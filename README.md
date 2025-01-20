# luxury_vehicle_data_pipelines

# Manual Data Pipeline with Jupyter Notebook: AWS Datalake to Docker

## Overview

This project is a learning exercise demonstrating a manual data pipeline using a Jupyter Notebook. It focuses on extracting data from an AWS S3 datalake (acting as a simple data source), performing basic transformations, and loading the processed data into a PostgreSQL database running in a Docker container.

**Disclaimer:** This project is intended for educational purposes and provides a simplified example.

## Purpose

The primary goal is to illustrate the fundamental concepts of building a data pipeline manually:

1. **Data Extraction:** Retrieving data from an AWS S3 bucket.
2. **Data Transformation:** Performing basic data cleaning, manipulation, and merging using Pandas.
3. **Data Loading:** Storing the processed data in a PostgreSQL database.

## Workflow

The Jupyter Notebook (`main.ipynb` - you should rename the notebook accordingly) guides you through the following steps:

1. **Installation:** Install necessary libraries like `boto3`, `pandas`, `sqlalchemy`, and `psycopg2-binary`.
2. **AWS S3 Connection:** Establish a connection to your AWS S3 bucket using `boto3`.
3. **Data Retrieval:** Download the car data (two CSV files) from the specified S3 bucket.
4. **Data Processing:**
   - Clean and prepare the data using Pandas.
   - Merge the two datasets for a consolidated view.
   - Filter the data based on specific criteria (year, price, etc.).
5. **Dockerized PostgreSQL:**
   - Ensure you have a Docker container running PostgreSQL and is accessible.
   - Obtain the connection details (host, port, database name, username, password).
6. **Data Loading:**
   - Create a SQLAlchemy engine to connect to the PostgreSQL database.
   - Load the processed DataFrame into a designated table.

## Requirements

- **AWS Account:** With access to an S3 bucket containing the sample data files.
- **Python 3.x:** With the required libraries installed.
- **Docker:** With a running PostgreSQL container.
- **Jupyter Notebook:** For executing the code.

## Usage

1. **Clone the repository.**
2. **Configure AWS Credentials:** Make sure your AWS credentials are configured for `boto3` (environment variables, AWS config files, etc.).
3. **Set up Docker:** Start a PostgreSQL container and note the connection details.
4. **Update Connection Details:** Modify the connection parameters in the Jupyter Notebook to match your PostgreSQL setup.
5. **Run the Notebook:** Execute the cells in the Jupyter Notebook to run the pipeline.

## Learning Outcomes

- Understanding basic data pipeline principles.
- Working with AWS S3 for data extraction.
- Utilizing Pandas for data transformation.
- Connecting to and loading data into a PostgreSQL database.
- Gaining familiarity with Docker for database deployment.
