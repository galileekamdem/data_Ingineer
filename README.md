# data_Ingineer
A Data Engineering project built on AWS services

The goal is to design a pipeline that ingests, transforms, catalogs, and queries data in a scalable and serverless way.

    Workflow:
Data Ingestion

CSV files are uploaded into an Amazon S3 bucket (input_data).

Automatic Trigger

Amazon EventBridge detects new files.

An AWS Lambda function is triggered to validate and pre-process the data.

Transformation & Preparation

Processed data is stored back into S3 (output_data).

AWS Glue is used for ETL and to create the data catalog.

Exploration & Analytics

Amazon Athena enables SQL queries directly on S3 data.

    Tech Stack
Amazon S3 – raw & processed data storage

AWS Lambda – serverless compute for automation

Amazon EventBridge – event-driven orchestration

AWS Glue – ETL and data cataloging

Amazon Athena – serverless interactive SQL queries
Getting Started
  
    Prerequisites

Active AWS account

AWS CLI configured

Python 3.x (for Lambda functions)

    Setup

Clone the repo:

git clone https://github.com/<your-username>/data_Ingineer.git
cd data_Ingineer


Deploy the infrastructure (via Terraform/CloudFormation or manually).

Upload CSV files into the S3 bucket (input_data).

Query the transformed data using Amazon Athena.

    Example Athena Query
SELECT country, COUNT(*) AS nb_users
FROM data_ingineer.output_data
GROUP BY country
ORDER BY nb_users DESC;

      Key Achievements

Automated end-to-end data pipeline

Fully serverless architecture

Scalable, flexible, and cost-effective

Centralized catalog for easy data exploration

    Future Improvements

Integration with Amazon Redshift for advanced analytics

Monitoring & alerts with CloudWatch

Unit tests for ETL scripts

    Author

Developed by @galileekamdem
📧 Contact: kkamdem071@gmail.com
