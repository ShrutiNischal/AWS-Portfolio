UCW Scholarly Activities Analysis
Project Overview
This repository contains several data analysis projects focused on faculty scholarly activities at UCW. The projects aim to explore trends, assess impact, and ensure data security in scholarly activities through various AWS-based tools and technologies.

Projects
1. Exploratory Data Analysis
Title: Trends in Faculty Scholarly Activities
Objective: Analyze trends and participation rates in various categories of scholarly activities (e.g., publications, presentations, grants).
Dataset: Data on faculty scholarly activities collected from AWS S3.
Methodology:
AWS Athena is used to query and filter data for exploratory purposes.
AWS QuickSight is utilized for visualizing trends.
Tools & Technologies:
AWS Athena
AWS S3
AWS QuickSight
Deliverables: Visual reports and interactive dashboards showcasing the trends.
2. Diagnostic Analysis
Title: Impact Analysis of Scholarly Activities on Academic Output
Objective: Assess how various scholarly activities contribute to academic output and faculty engagement.
Dataset: Scholarly activity records and corresponding academic outputs.
Methodology: Regression analysis using AWS SageMaker to evaluate relationships between activities and academic output.
Tools & Technologies:
AWS SageMaker
AWS Athena
Deliverables: A report detailing the correlation between scholarly activities and academic outcomes.
3. Data Wrangling and Integration
Title: Data Preparation and Integration for Scholarly Activity Analysis
Objective: Clean, transform, and integrate multiple datasets to create a unified and comprehensive dataset for analysis.
Dataset: Raw data from AWS S3, including faculty publications, grants, and presentation records.
Methodology: AWS Glue is used for data cleaning and transformation, while AWS Lambda facilitates data integration.
Tools & Technologies:
AWS Glue
AWS Lambda
AWS S3
Deliverables: A clean and integrated dataset, ready for analysis.
4. Data Security and Compliance
Title: Ensuring Data Security and Compliance in Scholarly Activity Analysis
Objective: Implement encryption, access control, and ensure compliance with UCW's research ethics policies.
Dataset: Sensitive data related to faculty scholarly activities.
Methodology: Use AWS KMS (Key Management Service) to encrypt data and enforce access control measures on AWS S3. Regular compliance checks are conducted.
Tools & Technologies:
AWS S3
AWS KMS (Key Management Service)
Deliverables: Secure data storage and compliance documentation.
How to Run the Projects
To replicate or further develop these analyses, follow these steps:

Set up AWS services:

Ensure you have access to AWS services such as S3, Athena, QuickSight, Glue, Lambda, and SageMaker.
Configure your AWS credentials using the AWS CLI.
Accessing Data:

The data is stored in AWS S3. Use AWS Athena to query the data or AWS Glue to clean and transform the raw datasets.
Running Visualizations:

Use AWS QuickSight to visualize the results. If you have access to the AWS dashboard, you can import the visualizations into your workspace.
Conducting Analysis:

For regression and other analytical techniques, use AWS SageMaker or integrate the dataset into your own machine learning environment.
Ensuring Data Security:

Implement security best practices by enabling AWS KMS for encryption and setting up proper access control policies for AWS S3.
Contributing
Feel free to open issues or submit pull requests if you'd like to contribute to this project. Ensure your code is well-documented and follows the guidelines for secure and compliant data handling.
Project 2 # AWS-Portfolio
# AWS Data Analytic Platform for The City of Vancouver

## Abstract
This project implements the AWS Data Analytic Platform (DAP) for the City of Vancouver, focusing on property tax data from 2023 and 2024. The platform is built using Amazon Web Services (AWS) technologies to streamline data management, analysis, and decision-making for the city's Government and Finance department. The goal of this project is to enhance operational efficiency and improve data-driven decision-making.

## Project Features
- **Data Ingestion**: Utilized Amazon S3 for storing property tax data for the years 2023 and 2024. Data was structured into folders for better organization.
- **Data Cleansing and Structuring**: AWS Glue was used for cleaning, transforming, and structuring raw datasets into a usable format.
- **Data Analysis**: Data was ingested into Amazon Redshift, enabling complex queries and deep analysis on property tax reports.
- **Data Visualization**: Created visual reports with bar charts and line graphs to analyze property value trends and tax rate changes.
- **Data Publishing**: Hosted the processed property tax data on Amazon EC2 for secure and easy access to stakeholders, including policymakers.

## Technologies Used
- **AWS Glue**: For ETL (Extract, Transform, Load) operations
- **Amazon S3**: For data storage
- **Amazon Redshift**: For structured data storage and querying
- **Amazon Athena**: For SQL-based data analysis
- **Amazon EC2**: For publishing and web access

## Project Breakdown

### 1. Data Ingestion
- Data was ingested from CSV files stored in Amazon S3 into the AWS ecosystem.
- Files were stored in a structured manner within the `PropertyTax` folder, with subfolders named `2023` and `2024`.
- <img width="625" alt="Screenshot 2024-09-17 at 5 02 07 PM" src="https://github.com/user-attachments/assets/053adabd-5e72-4d64-8c87-4387ea1c2311">

### 2. Data Cleansing and Structuring
- AWS Glue was used for data cleaning: removing duplicates, handling missing values, and correcting data types.
- Derived metrics such as `PropertyValueChange` and `TaxRateChange` were created for further analysis.
- <img width="508" alt="Screenshot 2024-09-17 at 5 02 51 PM" src="https://github.com/user-attachments/assets/115ef107-903f-4085-953e-c26e5db1b47c">
<img width="465" alt="Screenshot 2024-09-17 at 5 02 59 PM" src="https://github.com/user-attachments/assets/d966803b-e2b4-45f7-a843-2bb3ed3da27f">

### 3. Data Pipeline Implementation
- ETL pipeline implemented using AWS Glue's Visual ETL. The pipeline runs monthly to process and analyze updated data.
- <img width="588" alt="Screenshot 2024-09-17 at 5 02 39 PM" src="https://github.com/user-attachments/assets/9ab07a0e-7635-4ebc-aa05-b4c30b703fa5">
<img width="422" alt="Screenshot 2024-09-17 at 5 03 14 PM" src="https://github.com/user-attachments/assets/2b68e04a-4e2a-4a87-9697-fd63333084a1">
<img width="562" alt="Screenshot 2024-09-17 at 5 03 32 PM" src="https://github.com/user-attachments/assets/f1cb4624-f676-49f2-8bf0-0f04c1622df5">

### 4. Data Analysis
- Amazon Athena was used to run SQL queries on the dataset.
- Data trends for property values and tax rates were analyzed, identifying key property zones and tax changes across the city.

### 5. Data Visualization
- Bar charts and line graphs were used to visualize the correlation between land values and tax rates across different streets.
- <img width="431" alt="Screenshot 2024-09-17 at 5 03 40 PM" src="https://github.com/user-attachments/assets/a46f1d64-2612-4fa4-b97d-f9fa3a0dcf04">

### 6. Data Publishing
- The final dataset and visualizations were published using Amazon EC2 instances, providing web-based access to stakeholders.
- <img width="594" alt="Screenshot 2024-09-17 at 5 03 49 PM" src="https://github.com/user-attachments/assets/c175e6c8-2a72-4a9b-a54b-572f9c704f5d">

## Key Visuals
- Average Land Value and Tax Rate by Street (Bar Chart with Line Graph)
  - Displays average land value on the y-axis, streets on the x-axis, and the correlation with tax rates.
    

## Estimated Cost
The estimated cost for AWS services used in this project (S3, Glue, Redshift, EC2) was calculated using the AWS pricing calculator and is provided in the attached cost analysis document.
<img width="529" alt="Screenshot 2024-09-17 at 5 03 57 PM" src="https://github.com/user-attachments/assets/2c125c3e-c4d8-4c94-af4a-f5ebddc7b50a">
<img width="552" alt="Screenshot 2024-09-17 at 5 04 03 PM" src="https://github.com/user-attachments/assets/4bc26d08-0150-4496-a6f8-6c6adc90d952">

---

## How to Run the Project
1. **Data Storage**: Ensure that the raw datasets are uploaded to an Amazon S3 bucket.
2. **ETL Process**: Use AWS Glue to clean and transform the data. The ETL job can be scheduled to run monthly.
3. **Data Querying**: Utilize Amazon Redshift and Athena to query the cleaned datasets.
4. **Visualization**: Use your preferred data visualization tool or AWS QuickSight to visualize key insights.
5. **Data Publishing**: Host the results on an Amazon EC2 instance for easy access.

---

## Future Work
- Expand the platform to handle data for other city departments.
- Automate reporting and visualization processes for real-time insights.
- Integrate with other AWS services for enhanced data analysis, such as AWS Lambda for automated task execution.



