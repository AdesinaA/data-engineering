# 🚕 Taxi (uber) Data Engineering End to End Project

## Objective
In this project, I designed and implemented an end-to-end data pipeline that consists different processes:

- extracted data from New York City trip record data website and loaded it into AWS S3 storage for further processing.
- transformed and modeled the dataset using fact and dim data modelling tactics using python in jupyter notebook.
- created an AWS bucket, allowed public access and also set up an EC2 instance for our project.
- adopting ETL process, i orchestrated the data pipeline in MAGE AI and loaded the transformed data into AWS Redshift.
- developed a dashboard in Power BI.

This project is basically emphasizing on data engineering with lesser emphasis on analytics and dashboard aesthetics. 

## Table of Content
- Dataset Used
- Technologies
- Data Pipeline Architecture
- Data Modelling
- Cleaning and Transformation
- Storage
- ETL/Orchestration
- Dashboard

### Dataset Used
This project uses the tlc trip record dataset which include trip distances, rate types, payment types, pickup and dropoff dates and time, pickup and dropoff location & driver-passenger counts. 

Attached is the overview and links to the dataset details:

- website: https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page
- data dic: https://www.nyc.gov/assets/tlc/downloads/pdf/data_dictionary_trip_records_yellow.pdf
- raw data (csv format): https://github.com/AdesinaA/data-engineering/blob/main/Taxi%20(uber)%20project/uber_data.csv

### Technologies
These tools were used for the development of this project: 
- programming language: python & sql
- extraction & transformation: jupyter notebook, AWS redshift, AWS EC2 instance
- storage: AWS S3
- orchestration: [Mage AI](https://www.mage.ai/)
- dashboard: Power BI

### Data Pipeline Architecture
![dataarchitecture](https://github.com/user-attachments/assets/13c301e1-4fbe-4de0-975f-62e69a0aa524)

#### Files in the following stages:
- cleaning and transformation: https://github.com/AdesinaA/data-engineering/blob/main/Taxi%20(uber)%20project/uber_data.ipynb
- storage:
- etl, orchestration - mage: [transform](https://github.com/AdesinaA/data-engineering/blob/main/Taxi%20(uber)%20project/MageAI/uber_transformation_code.py ), [load]( https://github.com/AdesinaA/data-engineering/blob/main/Taxi%20(uber)%20project/MageAI/uber_load_data.py)
- analytics: [uber.sql]( )
- dashboard: 
