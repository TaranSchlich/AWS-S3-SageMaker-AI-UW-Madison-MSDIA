# Getting Started with AWS  

**By: Taran Schlichtmann**

**Date: 11/15/2025**

S3 Data Storage, SageMaker Notebook Setup, and Exploratory Data Analysis

Focused on using **Amazon Web Services (AWS)** to store data in S3, access it through SageMaker, and perform exploratory data analysis using Python. The assignment simulates an HR analytics scenario where employee feedback survey data is analyzed to uncover insights about training, compensation, benefits, and management support.

---

## AWS Services Used

### **Amazon S3**
- Created a new S3 bucket (`aws-assignment-###`)
- Uploaded the *employee_attitudes.csv* dataset
- Managed bucket configuration and file storage

### **Amazon SageMaker AI**
- Created a notebook instance (`SageMaker-Assignment`)
- Selected instance type: `ml.t3.medium`
- Used the `LabRole` IAM role for permissions
- Opened a Jupyter notebook using the `conda_python3` kernel
- Connected to S3 and loaded the dataset using Python

---

## Exploratory Data Analysis (EDA)

Within the SageMaker notebook, I performed the following:

### **Imported Required Libraries**
- `boto3` for S3 communication  
- `pandas` for data manipulation  
- `get_execution_role` for AWS permissions  

### **Loaded the CSV File**
```python
role = get_execution_role()
data_location = 's3://aws-assignment-###/employee_attitudes.csv'
df_ratings = pd.read_csv(data_location)
```

### **Calculated Key Metrics**
Number of rows: 30

Previewed first 5 records

rating_raises in first row: 61

Generated descriptive statistics

Standard deviation of rating_overall: 12.17

Average of rating_management: 66.6

Correlation matrix

Correlation between rating_raises and rating_benefits: 0.45

These steps demonstrate the ability to load, inspect, and analyze data directly within AWS SageMaker.

### **Insights from the Employee Feedback Data**
Employees rated management support relatively high on average

Training and benefits had more variability across responses

Strong correlations were observed between:

Overall satisfaction and management ratings

Training and raises

These insights can help HR identify areas for improvement in employee experience

### **Tools & Technologies**
Amazon S3 (cloud storage)

Amazon SageMaker AI (notebook environment)

Python (pandas, boto3)

Jupyter Notebook

AWS IAM (permissions & roles)

### **Skills Demonstrated**
Cloud data storage and retrieval

SageMaker notebook setup and configuration

Python-based data analysis

Descriptive statistics and correlation analysis

HR analytics and interpretation of survey data

AWS resource management (creating, stopping, deleting instances and buckets)
