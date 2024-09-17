# AWS-Portfolio
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

### 2. Data Cleansing and Structuring
- AWS Glue was used for data cleaning: removing duplicates, handling missing values, and correcting data types.
- Derived metrics such as `PropertyValueChange` and `TaxRateChange` were created for further analysis.

### 3. Data Pipeline Implementation
- ETL pipeline implemented using AWS Glue's Visual ETL. The pipeline runs monthly to process and analyze updated data.

### 4. Data Analysis
- Amazon Athena was used to run SQL queries on the dataset.
- Data trends for property values and tax rates were analyzed, identifying key property zones and tax changes across the city.

### 5. Data Visualization
- Bar charts and line graphs were used to visualize the correlation between land values and tax rates across different streets.

### 6. Data Publishing
- The final dataset and visualizations were published using Amazon EC2 instances, providing web-based access to stakeholders.

## Key Visuals
- Average Land Value and Tax Rate by Street (Bar Chart with Line Graph)
  - Displays average land value on the y-axis, streets on the x-axis, and the correlation with tax rates.

## Estimated Cost
The estimated cost for AWS services used in this project (S3, Glue, Redshift, EC2) was calculated using the AWS pricing calculator and is provided in the attached cost analysis document.

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



