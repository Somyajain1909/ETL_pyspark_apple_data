## Overview
This project implements an ETL (Extract, Transform, Load) pipeline for processing Apple data using Databricks.

## Project WorkFlow

            csv ------                                       ------datalake
                       \                                    /
        parquet ------------->[Factory ----> Pyspark SQL---
                       /       pattern]                     \
    delta table ------                                       ------ delta table
    
    
                <---extract--->           <---transform--->     <---load---> 

## Key Features:
**Extract:** Fetches raw Apple data from CSV, parquet, or delta table.

**Transform:** Cleans and processes the data.

    Problem Statements:

    1. List the customers who bought airpods after iphone.
    2. List the customers who bought only airpods and iphone.

**Load:** Saves the transformed data into a format like Parquet, or loads it into a delta table.

**Databricks Integration:** Utilizes Databricks and Apache Spark for distributed and scalable data processing.

## Requirements
To run the Apple Data ETL pipeline, you need the following:

**Databricks Workspace:** You need access to a Databricks workspace with a configured cluster.

**Python 3.x:** Required for running PySpark-based scripts and notebooks.
Apache Spark: Pre-installed in Databricks environments for distributed data processing.

**Databricks CLI (Optional):** For interacting with Databricks from the command line.

**CSV/JSON Files:** Raw Apple data files in CSV or other formats for input into the ETL pipeline.

