# WK8-Data-Pipelines-with-Redis
This repo contains project files for Data Pipelines with Redis imlemented using python, redis and postgresql

## Background Information
As a telecommunications data engineer, you have been tasked with building a pipeline that can
efficiently extract, transform, and load data from CSV files into a Postgres database. The data to
be extracted is related to customer call logs, which contain information about the duration, cost,
and destination of customer calls. The extracted data needs to be transformed to ensure it is in
the correct format and structure for storage in the database. The pipeline should also cache
data using Redis to speed up the data extraction and transformation.

# Customer Call Logs Processing Pipeline
This is a data processing pipeline that reads customer call logs data, cleans and transforms it, and loads it into a Postgres database.

## Pipeline Steps
The pipeline consists of three main steps:

* **extract_data():** This step reads the customer call logs data from a CSV file or Redis cache.

* **transform_data(data):** This step cleans and transforms the data, including converting the call_duration column to minutes, stripping the dollar sign from the call_cost column, and adding new columns for the call start time and day of week.

* **load_data(transformed_data):** This step loads the transformed data into a Postgres database.

## Best Practices
The implementation of this pipeline includes the following best practices:

* Use of a logging system to capture errors and exceptions during the pipeline execution.

* Use of a Redis cache to speed up data retrieval, avoiding unnecessary file reading.

* Use of psycopg2 to handle database connections and operations.

## Deployment and Running the Pipeline
To deploy and run the pipeline with a cloud-based provider, follow these steps:

* Set up a Redis instance and a Postgres database on the cloud platform.

* Update the pipeline script with the connection details for Redis and Postgres.

* Install the required dependencies (e.g. pandas, redis, psycopg2) on the cloud platform.

* Run the pipeline script using a scheduling tool like Cron or Airflow.
