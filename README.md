# Getting Started with AWS  

**By: Taran Schlichtmann**

**Date: 11/15/2025**

S3 Data Storage, SageMaker Notebook Setup, and Exploratory Data Analysis

A hands‑on introduction to Amazon Web Services (AWS) using S3 for cloud storage and SageMaker for Python‑based data analysis. This project focuses on analyzing employee feedback survey data to uncover insights related to training, compensation, benefits, and management support.

🚀 Overview
This assignment demonstrates the ability to:

Upload and manage data in Amazon S3

Configure and run a SageMaker AI notebook instance

Use Python (pandas, boto3) to load and analyze cloud‑stored data

Perform exploratory data analysis (EDA) including descriptive statistics and correlations

Interpret HR‑related survey data to support business decisions

☁️ AWS Services Used
Amazon S3
Created a new S3 bucket (aws-assignment-###)

Uploaded the employee_attitudes.csv dataset

Managed bucket configuration and storage settings

Amazon SageMaker AI
Created a notebook instance named SageMaker-Assignment

Selected instance type: ml.t3.medium

Used the LabRole IAM role for permissions

Opened a Jupyter notebook using the conda_python3 kernel

Connected to S3 and loaded the dataset using Python

📊 Exploratory Data Analysis (EDA)
Imported Required Libraries
boto3 for S3 communication

pandas for data manipulation

get_execution_role for AWS permissions

Loaded the CSV File
Code
role = get_execution_role()
data_location = 's3://aws-assignment-###/employee_attitudes.csv'
df_ratings = pd.read_csv(data_location)
Calculated Key Metrics
Number of rows: 30

First row rating_raises: 61

Standard deviation of rating_overall: 12.17

Average of rating_management: 66.6

Correlation between rating_raises and rating_benefits: 0.45

These steps confirm successful data ingestion and analysis within SageMaker.

💡 Insights from the Employee Feedback Data
Employees rated management support relatively high on average

Training and benefits showed greater variability across responses

Strong correlations were observed between:

Overall satisfaction and management ratings

Training and raises

These insights help HR identify areas for improvement in employee experience and engagement.

🛠️ Tools & Technologies
Amazon S3 (cloud storage)

Amazon SageMaker AI (notebook environment)

Python (pandas, boto3)

Jupyter Notebook

AWS IAM (permissions & roles)

🎯 Skills Demonstrated
Cloud data storage and retrieval

SageMaker notebook setup and configuration

Python‑based data analysis

Descriptive statistics and correlation analysis

HR analytics interpretation

AWS resource management (creating, stopping, deleting instances and buckets)
