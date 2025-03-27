# Portfolio - Monwar Hossain (2302437)

# Descriptive Analysis

Project Description: Analyzing Animal Impoundment Trends in Vancouver (2024)

Objective: Identify trends in animal intake patterns, kennel usage, and naming frequencies across age categories (Puppy, Adult, Senior) to optimize shelter operations.

Dataset: 
  1. Animal_ID
  2. Species
  3. Age_Category
  4. Name
  5. Kennel_Number
  6. Date_Impounded
  7. Status
     
Methodology: 

  1. Data Injection: We uploaded the data in the raw S3 bucket.

<img width="751" alt="Image" src="https://github.com/user-attachments/assets/7e58aceb-0612-4822-979a-f5937d4364dc" />

  2. Data Aggression: Used AWS Athena to run SQL queries aggregating animal counts by age category.
     
<img width="557" alt="Image" src="https://github.com/user-attachments/assets/75b3791c-6f25-428a-bae4-14b7f213d791" />

  3. Visualization: Created summary reports for shelter capacity planning using AWS DataBrew and tracked kennel occupancy rates using AWS DataBrew visualizations.

<img width="751" alt="Image" src="https://github.com/user-attachments/assets/35139fd3-696e-474a-bff4-6261d5a2e669" />

  4. Reporting: The curated dataset is later stored in another S3 bucket (Curated Bucket) 

<img width="751" alt="Image" src="https://github.com/user-attachments/assets/6891fa94-519c-406c-9bd1-e8742686a24b" />

  5. Recommendations:

       a) Use a larger dataset.
       b) Filter out more null columns and remove them.
       c) Fix the headings.

Tools & Technologies: 

  1. AWS: Athena, DataBrew, S3.
     
  2. Languages: SQL, Python (Pandas).

Timeline: 

  1. Phase 1: Data Injection

  2. Phase 2: Data Aggregation

  3. Phase 3: Visualization & Reporting

Deliverables: 

  1. Interactive dashboards showing intake trends.
     
  2. Shelter utilization reports for city planners.


# Data Wrangling

Project Title: ETL Pipeline for Animal Inventory Data

Objective: Clean, standardize, and catalog raw animal impoundment records for analysis.

Dataset: Raw CSV/JSON files from Vancouver Open Data Portal. 

<img width="751" alt="Image" src="https://github.com/user-attachments/assets/ce33072a-b2fe-4ade-b605-24603469c833" />

Methodology: 

  1. Data Cleaning: Removed redundant columns (PitNumber, Code) using AWS Glue.

<img width="834" alt="Image" src="https://github.com/user-attachments/assets/04a75c43-36e3-447d-9d24-70214aa03b6f" />

  2. Transformation: Converted Date_Impounded to ISO format.

<img width="416" alt="Image" src="https://github.com/user-attachments/assets/02d9d148-a8eb-417c-b0a4-b0b309f00bd6" />

  3. Cataloging: Created metadata tables in AWS Glue Data Catalog.

<img width="752" alt="Image" src="https://github.com/user-attachments/assets/c10a561f-80da-453e-b163-0cc50b2543eb" />

Tools & Technologies: 

  1. AWS: Glue S3, Data Catalog.
     
  2. Languages: PySpark, SQL.

Timeline: 

  1. Phase 1: Data Cleaning

  2. Phase 2: Transformation

  3. Phase 3: Cataloging

Deliverables: 

  1. Analysis-ready datasets in S3 (pets-cur-hos).

<img width="752" alt="Image" src="https://github.com/user-attachments/assets/1f8bb7ee-f494-40f2-afd1-dd4f2b867d74" />
     
  2. Automated Glue workflows for future data updates.


# Data Quality Control

Project Title: Data Integrity & Security for Animal Services.

Objective: Implement automated validation and monitoring to ensure compliance and accuracy.

Methodology: 

  1. Validation Rule: Flagged missing columns (e.g. Approximate_Weight) using AWS Glue DataBrew.

<img width="783" alt="Image" src="https://github.com/user-attachments/assets/760b0766-ce2a-4478-b288-3d857ac723f7" />

  2. Security: Encrypted S3 buckets with AWS KMS key ani-con-inv-key-hos.

<img width="755" alt="Image" src="https://github.com/user-attachments/assets/8ed2b51a-5792-4811-b308-be70a4970e5c" />

  3. Monitoring: Tracked anomalies via CloudWatch dashboard ani-con-MCR-hos. Also, used an alarm to get a notification when my threshold is crossed.

<img width="755" alt="Image" src="https://github.com/user-attachments/assets/25115f91-a354-46aa-93f7-9d0daf455e62" />

Tools & Technologies: 

  1. AWS: KMS, CloudWatch, CloudTrail.

Timeline: 

  1. Phase 1: Validating 

  2. Phase 2: Security Setup

  3. Phase 3: Monitoring

Deliverables: 

  1. Real-time data quality dashboards.

  2. Audit logs for compliance reporting.


# Note: The portfolio is simplified and only highlights the key steps within the whole process. 
     

     

