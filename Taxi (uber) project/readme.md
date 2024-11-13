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
- etl, orchestration - mage: [transform](https://github.com/AdesinaA/data-engineering/blob/main/Taxi%20(uber)%20project/MageAI/uber_transformation_code.py), [load](https://github.com/AdesinaA/data-engineering/blob/main/Taxi%20(uber)%20project/MageAI/uber_load_data.py)
- analytics: [uber.sql](https://github.com/AdesinaA/data-engineering/blob/main/Taxi%20(uber)%20project/uber.sql)
- dashboard: 

### Data Modelling
The datasets was designed using [lucid chart](https://www.lucidchart.com/) adopting the principles of fact and dim data modelling concepts.
![Screenshot 2024-11-13 at 14 48 18](https://github.com/user-attachments/assets/e0b1f04c-5e9a-411c-9b0f-3e7e7a583401)

### stage 1: Cleaning and Transformation
Link to the script: https://github.com/AdesinaA/data-engineering/blob/main/Taxi%20(uber)%20project/uber_data.ipynb

### stage 2: storage
![Screenshot 2024-11-13 at 10 48 54](https://github.com/user-attachments/assets/1aaabf36-1c6d-48ea-9bd5-7941e3840f66)

### stage 3: etl / orchestration
![Screenshot 2024-11-13 at 10 49 38](https://github.com/user-attachments/assets/df3675ac-0c15-4f30-86ac-e7b51237bfd8)

#### Note: Choose Ubuntu, download your PEM key. In your terminal, install these dependencies and SSH. 

```# Install Python and pip
sudo apt-get install update -y
sudo apt-get update -y

# install python on our machine.
sudo apt-get install python3-distutils
sudo apt-get install python3-apt

# install wget to enable us to Download file from the internet.
sudo apt-get install wget
wget https://bootstrap.pypa.io/get-pip.py

sudo python3 get-pip.py

# Install Mage
sudo pip3 install mage-ai

# Install Pandas
sudo pip3 install pandas

# install AWS library
sudo pip3 install awscli

#install AWS Simple Storage Service (s3) Datalake
sudo pip3 install s3

#install Python library to programmatically access and manage various AWS services
sudo pip3 install boto3

# install AWS Redshift
 sudo pip3 install redshift
```
#### performed orchestration in mage ai by accessing the external internet protocol address. It is always in this format: <external  IP address>:<port number> . Afterwards, i created a new pipeline in two stages:
- transform: [uber_transformation_code.py](https://github.com/AdesinaA/data-engineering/blob/main/Taxi%20(uber)%20project/MageAI/uber_transformation_code.py)
- load: [uber_load_data.py](https://github.com/AdesinaA/data-engineering/blob/main/Taxi%20(uber)%20project/MageAI/uber_transformation_code.py)

#### Note: Before loading executing the load pipeline, create access keyand secret key and grant it permission to have access to s3 and redshift privilege and then add it to your ```io_config.yaml```. 
