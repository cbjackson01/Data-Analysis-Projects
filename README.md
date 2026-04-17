# Chicago Transit Aurhority Time Prediction Accuracy


## Objective

This project utilized the Chicago Transit Authority's open data API resources to harvest live data using an API and analyze how accurte bus arrival times are throughout the city. This project was done using python and the corresponding data and code can be found in the CTA-Analysis branch of this repository.

To Meet this Objective, I designed and implemented an end-to-end data pipeline that consists of several stages:
1. Extracted data from the CTA Real Time Train Tracker  and loaded into Jupyter Notebook for further processing.
2. Collected data on whether or not the bus came at the time predicted.
3. Transformed and modeled the data using fact and dimensional data modeling concepts using Python on Jupyter Notebook.
4. Using ETL concept, I orchestrated the data pipeline for analysis
5. on Mage AI and loaded the transformed data into Google BigQuery.
6. Developed a dashboard on Looker Studio.

As this is a data engineering project, my emphasis is primarily on the engineering aspect with a lesser emphasis on analytics and dashboard development.

The sections below will explain additional details on the technologies and files utilized.

## Table of Content

- [Dataset Used](#dataset-used)
- [Technologies](technologies)
- [Data Pipeline Architecture](#data-pipeline-architecture)
- [Date Modeling](#data-modeling)
- [Step 1: Cleaning and Transformation](#step-1-cleaning-and-transformation)
- [Step 2: Storage](#step-2-storage)
- [Step 3: ETL / Orchestration](#step-3-etl--orchestration)
- [Step 4: Analytics](#step-4-analytics)
- [Step 5: Dashboard](#step-5-dashboard)

## Dataset Used

This project uses the TLC Trip Record Data which include fields capturing pick-up and drop-off dates/times, pick-up and drop-off locations, trip distances, itemized fares, rate types, payment types, and driver-reported passenger counts.

More info about dataset can be found in the following links:
- Website: [CTA Real-Time Bus Tracker](https://www.transitchicago.com/developers/bustracker/)
- [Data Dictionary](https://www.transitchicago.com/assets/1/6/cta_Bus_Tracker_API_Developer_Guide_and_Documentation_2025-04-21.pdf)


## Technologies

The following technologies are used to build this project:
- Language: Python, SQL
- Extraction and transformation: Jupyter Notebook, PostGRE SQL
- Storage: PySpark

## Data Pipeline Architecture


<img width="897" alt="Screenshot 2023-05-08 at 11 49 09 AM" src="https://user-images.githubusercontent.com/81607668/236729698-65e193bc-75ee-4ea6-9040-f33f5f2958cb.png">

Files in the following stages:
- Step 1: Cleaning and transformation - [Uber Data Engineering.ipynb](https://github.com/katiehuangx/data-engineering/blob/main/Uber%20Project/Uber%20Data%20Engineering.ipynb)
- Step 2: Storage
- Step 3: ETL, Orchestration - Mage: [Extract](https://github.com/katiehuangx/data-engineering/blob/main/Uber%20Project/Mage/uber_load_data.py), [Transform](https://github.com/katiehuangx/data-engineering/blob/main/Uber%20Project/Mage/uber_transformation.py), [Load](https://github.com/katiehuangx/data-engineering/blob/main/Uber%20Project/Mage/uber_gbq_load.py)
- Step 4: Analytics - [SQL script](https://github.com/katiehuangx/data-engineering/blob/main/Uber%20Project/sql_script.sql)
- Step 5: [Dashboard](https://github.com/katiehuangx/data-engineering/blob/main/Uber%20Project/Uber_Dashboard.pdf)

## Data Modeling

The datasets are designed using the principles of fact and dim data modeling concepts. 
