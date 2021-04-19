# Cloud-data-warehouses-AWS


## Introduction
A music streaming startup, Sparkify, has grown their user base and song database and want to move their processes and data onto the cloud. Their data resides in S3, in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.

As their data engineer, you are tasked with building an ETL pipeline that extracts their data from S3, stages them in Redshift, and transforms data into a set of dimensional tables for their analytics team to continue finding insights in what songs their users are listening to. You'll be able to test your database and ETL pipeline by running queries given to you by the analytics team from Sparkify and compare your results with their expected results.

## Project Description
In this project, you'll apply what you've learned on data warehouses and AWS to build an ETL pipeline for a database hosted on Redshift. To complete the project, you will need to load data from S3 to staging tables on Redshift and execute SQL statements that create the analytics tables from these staging tables.

## How to Run
Prerequisites: Configuration file with login details for an active AWS Redshift cluster and ARN for an IAM role with S3 read access.

- Run sql_queries.py from terminal or python console to load table create and insert queries.
- Run create_tables.py from terminal or python console to create staging and analytical tables.
- Run etl.py from terminal or python console to process and load data into data warehouse.

## Project structure
This is the project structure, if the bullet contains /
means that the resource is a folder:

- create_tables.py - This script will drop old tables (if exist) ad re-create new tables
- etl.py - This script executes the queries that extract JSON data from the S3 bucket and ingest them to Redshift
- sql_queries.py - This file contains variables with SQL statement in String formats, partitioned by CREATE, DROP, COPY and INSERT statements
- dhw.cfg - Configuration file used that contains info about Redshift, IAM and S3
