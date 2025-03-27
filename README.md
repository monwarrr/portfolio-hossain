# Portfolio - Monwar Hossain (2302437)

Descriptive Analysis

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

  3. Data Aggression: Used AWS Athena to run SQL queries aggregating animal counts by age category.
     
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

Deliverable: 

  1. Interactive dashboards showing intake trends.
  2. Shelter utilization reports for city planners.
