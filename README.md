# cloud-computing-sahithi
# README: Exploratory Analysis of Vancouver’s 2025 Capital Budget Allocation

## Project Description
Exploratory Analysis of the 2025 Multi-Year Capital Project Budget

## Project Title
Exploring Vancouver’s 2025 Capital Budget Allocation

## Objective
The objective of this project is to perform exploratory data analysis (EDA) to identify trends and patterns in the City of Vancouver’s 2025 capital project budget, focusing on service categories such as water, parks, streets, community facilities, and public safety.

## Dataset
The dataset was sourced from the City of Vancouver open data portal. It includes:
- Budget requests for 2025
- Historical capital expenditures
- Service categories like "One Water," "Parks and Public Open Spaces," and "Public Safety"

## Methodology
### 1. Data Ingestion
- Raw data was stored in an AWS S3 bucket (`ceb-raw-sah`).
- A structured data-cleaning and profiling architecture was set up in a second S3 bucket (`ceb-trf-sah`), organized into folders for data-cleaning and profiling tasks.

### 2. Data Profiling and Cleaning
- The dataset was linked to AWS Glue DataBrew for profiling.
- Issues identified included missing values and inconsistent formats.
- Cleaning involved:
  - Imputing missing values
  - Removing duplicates
  - Standardizing formats (e.g., dates and numerical fields)
- A reusable recipe was created in DataBrew to automate the cleaning process.

### 3. ETL Pipeline Design
- Designed and executed an ETL pipeline in AWS Glue:
  - Dropped irrelevant columns
  - Aggregated data by service categories to calculate metrics (e.g., total budget requests and expenditures)
  - Standardized schema for consistency
- Merged datasets for deeper insights, comparing 2025 budgets with historical plans.

  ![image](https://github.com/user-attachments/assets/9f9c907b-cc3d-4124-bb4f-92c4682d1f1c)


## Tools and Technologies
- **AWS Services:** S3, Glue DataBrew, and Glue ETL.
- **Data Storage:** Organized bucket structure for raw and transformed data.
- **Profiling and Cleaning:** AWS Glue DataBrew for profiling, cleaning, and recipe creation.
- **ETL Automation:** AWS Glue Visual ETL for pipeline design and execution.

## Deliverables
- A cleaned and transformed dataset stored in AWS S3.
- Key insights derived from the ETL pipeline:
  - Total and category-wise budget allocations
  - Comparative analysis with historical expenditures
- Organized data outputs for system and user purposes:
  - Internal (system integration)
  - External (analysis and reporting)


    



## Conclusion
The exploratory analysis provided a structured and efficient approach to understanding the City of Vancouver’s 2025 capital project budgets. By leveraging AWS services for data profiling, cleaning, and transformation, the analysis highlighted significant budget trends and variances across service categories. The insights derived from this analysis can assist in strategic decision-making and resource allocation, ensuring a balanced approach to financial planning. Additionally, the reusable ETL pipelines and recipes ensure scalability for future analyses, enhancing operational efficiency for budgetary evaluations.
