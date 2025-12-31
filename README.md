# Getting Started with AWS  

**By: Taran Schlichtmann**

**Date: 11/15/2025**

S3 Data Storage, SageMaker Notebook Setup, and Exploratory Data Analysis

A hands‑on introduction to Amazon Web Services (AWS) using S3 for cloud storage and SageMaker for Python‑based data analysis. This project focuses on analyzing employee feedback survey data to uncover insights related to training, compensation, benefits, and management support.

## Project Overview

The goal of this assignment was to:

- Upload structured data to Amazon S3  
- Configure and launch a SageMaker notebook instance  
- Use Python to load and analyze cloud‑stored data  
- Generate descriptive statistics and correlations  
- Interpret HR‑related survey results to support business insights  

---

## AWS Services Utilized

### Amazon S3
- Created a new S3 bucket (`aws-assignment-###`)
- Uploaded the `employee_attitudes.csv` dataset
- Managed bucket configuration and file storage

### Amazon SageMaker AI
- Created a notebook instance (`SageMaker-Assignment`)
- Selected instance type: `ml.t3.medium`
- Used the `LabRole` IAM role
- Opened a Jupyter notebook using the `conda_python3` kernel
- Connected to S3 and loaded the dataset with Python

---

## Exploratory Data Analysis (EDA)

### Libraries Imported
- boto3 for S3 communication  
- pandas for data manipulation  
- get_execution_role for AWS permissions  

### Data Loading
```python
role = get_execution_role()
data_location = 's3://aws-assignment-###/employee_attitudes.csv'
df_ratings = pd.read_csv(data_location)
```

### Key Outputs
Total rows: 30
First row rating_raises: 61
Standard deviation (rating_overall): 12.17
Average (rating_management): 66.6
Correlation (rating_raises vs rating_benefits): 0.45

### Insights from the Survey Data
Management support received relatively high ratings
Training and benefits showed greater variability
Strong relationships were observed between:
Overall satisfaction and management ratings
Training and raises
These findings help identify areas where HR can focus to improve employee experience.

### Tools & Technologies
Amazon S3
Amazon SageMaker AI
Python (pandas, boto3)
Jupyter Notebook
AWS IAM

### Skills Demonstrated
Cloud data storage and retrieval
SageMaker notebook configuration
Python‑based data analysis
Descriptive statistics and correlation analysis
HR analytics interpretation
AWS resource management (instances, buckets, permissions)
