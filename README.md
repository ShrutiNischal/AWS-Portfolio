# Project 1 UCW Scholarly Activity Data Analysis Project

## Project Overview
This project aims to analyze faculty scholarly activities at UCW using various AWS cloud technologies. It involves several stages of data analysis, from exploratory and diagnostic phases to data wrangling and ensuring data security compliance. The ultimate goal is to provide insights into trends in faculty activities and their impact on academic output while adhering to data security measures.

---

## 1. Exploratory Data Analysis
**Project Title**: Trends in Faculty Scholarly Activities  
- **Objective**: Analyze trends and participation rates in different categories of scholarly activities as defined by UCW.
- **Dataset**: Data on faculty scholarly activities collected from AWS S3.
- **Methodology**: AWS Athena is utilized to query the dataset for trends, and AWS QuickSight is used for generating visual analytics and dashboards.
- **Tools & Technologies**: 
  - AWS Athena
  - AWS S3
  - Amazon QuickSight
- **Deliverables**: 
  - Visual reports
  - Dashboards highlighting trends in faculty scholarly activities.

---

## 2. Diagnostic Analysis
**Project Title**: Impact Analysis of Scholarly Activities on Academic Output  
- **Objective**: Assess the impact of various scholarly activities on academic output and faculty engagement.
- **Dataset**: Records of scholarly activities and their corresponding academic outputs.
- **Methodology**: Conducting regression analysis using AWS SageMaker to evaluate the relationship between scholarly activities and academic output.
- **Tools & Technologies**:
  - AWS SageMaker
  - AWS Athena
- **Deliverables**: 
  - A report detailing the impact of scholarly activities on academic output and faculty engagement.

---

## 3. Data Wrangling and Integration
**Project Title**: Data Preparation and Integration for Scholarly Activity Analysis  
- **Objective**: Clean, transform, and integrate data from various sources to prepare a unified dataset for further analysis.
- **Dataset**: Raw data from AWS S3, which includes faculty publications, grants, and presentations.
- **Methodology**: Data cleaning and transformation processes are executed using AWS Glue, and integration with other academic data sources is automated with AWS Lambda.
- **Tools & Technologies**:
  - AWS Glue
  - AWS Lambda
  - AWS S3
- **Deliverables**: 
  - A cleaned and integrated dataset ready for analysis.

---

## 4. Data Security and Compliance
**Project Title**: Ensuring Data Security and Compliance in Scholarly Activity Analysis  
- **Objective**: Implement security measures and ensure that the analysis complies with UCW's research ethics policies.
- **Dataset**: Sensitive data involved in faculty scholarly activities.
- **Methodology**: Encryption and access control measures are applied in AWS S3, along with compliance checks to ensure secure handling of the data.
- **Tools & Technologies**:
  - AWS S3
  - AWS KMS (Key Management Service)
- **Deliverables**:
  - Secure storage solutions for scholarly activity data.
  - Compliance documentation outlining security measures.
    
--

# Project 2 # AWS-Portfolio
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



