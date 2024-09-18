# Project 1 UCW Scholarly Activity Data Analysis Project

## Project Overview
This project focuses on analyzing the trends and impacts of faculty scholarly activities at UCW. The analysis was conducted using a variety of AWS cloud-based services for data querying, visualization, and reporting. The project is divided into several key phases: Exploratory Data Analysis, Diagnostic Analysis, Data Wrangling and Integration, and Data Security & Compliance.

## Table of Contents
- [Project Overview](#project-overview)
- [Objectives](#objectives)
- [Technologies Used](#technologies-used)
- [Datasets](#datasets)
- [Methodologies](#methodologies)
- [Deliverables](#deliverables)
- [How to Run the Project](#how-to-run-the-project)
- [File Structure](#file-structure)
- [Contact Information](#contact-information)

---

## Objectives

1. **Exploratory Data Analysis (EDA)**
   - **Project Title**: Trends in Faculty Scholarly Activities
   - **Objective**: Analyze trends and participation rates in different categories of scholarly activities as defined by UCW.
   
2. **Diagnostic Analysis**
   - **Project Title**: Impact Analysis of Scholarly Activities on Academic Output
   - **Objective**: Assess the impact of various scholarly activities on academic output and faculty engagement.
   
3. **Data Wrangling and Integration**
   - **Project Title**: Data Preparation and Integration for Scholarly Activity Analysis
   - **Objective**: Clean, transform, and integrate data from various sources to prepare a unified dataset for analysis.
   
4. **Data Security and Compliance**
   - **Project Title**: Ensuring Data Security and Compliance in Scholarly Activity Analysis
   - **Objective**: Implement security measures and ensure compliance with UCW’s research ethics policy.

---

## Technologies Used
- **AWS Athena**: For querying data from AWS S3.
- **AWS S3**: For data storage and access.
- **Amazon QuickSight**: For creating data visualizations.
- **AWS SageMaker**: For running regression analysis and machine learning models.
- **AWS Glue**: For data cleaning and transformation.
- **AWS Lambda**: For automating data integration tasks.
- **AWS KMS (Key Management Service)**: For ensuring data security and compliance.

---

## Datasets
The project uses various datasets stored in **AWS S3**, including:
- Faculty publication records
- Grant and presentation data
- Scholarly activity participation records
- Corresponding academic output data

---

## Methodologies

1. **Exploratory Data Analysis (EDA)**
   - Utilized **AWS Athena** to query data on scholarly activities and generate trends.
   - **AWS QuickSight** was used to visualize the results.

2. **Diagnostic Analysis**
   - Conducted regression analysis using **AWS SageMaker** to assess the impact of scholarly activities on academic output.

3. **Data Wrangling and Integration**
   - Cleaned and transformed raw datasets using **AWS Glue** and automated integration with **AWS Lambda**.

4. **Data Security and Compliance**
   - Implemented encryption and access control measures using **AWS KMS** to ensure secure handling of sensitive data.

---

## Deliverables

1. **Exploratory Data Analysis**
   - Visual reports and dashboards highlighting trends in scholarly activities.
   
2. **Diagnostic Analysis**
   - A report detailing the impact of scholarly activities on academic output.
   
3. **Data Wrangling and Integration**
   - A cleaned and integrated dataset ready for analysis.

4. **Data Security and Compliance**
   - Secure storage solutions and compliance documentation.

---

## How to Run the Project

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/UCW-Scholarly-Activity-Data-Analysis.git
    cd UCW-Scholarly-Activity-Data-Analysis
    ```

2. Set up AWS credentials in your environment to access **AWS S3**, **Athena**, **QuickSight**, **SageMaker**, **Glue**, and **Lambda** services.

3. Install the necessary Python packages if applicable:
    ```bash
    pip install boto3 pandas matplotlib seaborn
    ```

4. Run the analysis scripts and visualization notebooks:
    ```bash
    python exploratory_analysis.py
    python diagnostic_analysis.py
    ```

5. Ensure that AWS services like **Athena** and **QuickSight** are properly configured for data access and visualization.

---

## File Structure

```bash
.
├── data                    # Raw and processed data files
├── scripts                  # Python scripts for data analysis and visualization
│   ├── exploratory_analysis.py
│   ├── diagnostic_analysis.py
├── notebooks                # Jupyter notebooks for data wrangling and EDA
├── reports                  # Final reports and dashboards
├── README.md                # Project overview and instructions
└── requirements.txt         # List of dependencies

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



