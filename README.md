
# Panic Attack Data Analysis

This project focuses on analyzing panic attack patterns using Power BI to uncover meaningful insights related to frequency, triggers, and demographic trends. The goal is to transform raw data into actionable insights that can help in better understanding mental health patterns


# Objectives
* Analyze frequency and distribution of panic attacks
* Identify key triggers and contributing factors
* Understand demographic patterns (age, gender, etc.)
* Build an interactive dashboard for data exploration
## Project Workflow
1. Snowflake Setup
- Created an account in Snowflake Cloud Data Platform
Configured warehouse, database, and schema

2. Data Upload
- Created a new database and required tables
Imported CSV dataset into Snowflake tables


3. Data Exploration in Snowflake
- Queried data using SQL to understand structure and relationships
- Performed initial data validation and checks
Analyzed key fields and data distribution

![Snap_1](https://github.com/user-attachments/assets/26607104-70d0-467e-9a42-26c75f547210)

4. Power BI Integration
- Connected Power BI to Snowflake as a data source
Imported data into Power BI for further analysis

![Snap_2](https://github.com/user-attachments/assets/ce04fbc6-f5d0-4690-b3f0-ca185e63305e)

5. Data Understanding & Preparation
- Explored dataset inside Power BI
- Identified data quality issues and required transformations
6. Data Transformation (Power Query)
- Cleaned and transformed data using Power Query Editor
- Handled missing/null values
- Changed data types
- Filtered and reshaped data
- Created derived columns

![Snap_3](https://github.com/user-attachments/assets/48b8aa1d-2dc8-44b8-a2bb-0638f40e06a9)


7. Data Modeling & Visualization
- Built relationships between tables (if applicable)
- Created calculated columns and measures using DAX

% Patient with Dizziness = DIVIDE(COUNTROWS(FILTER(PANIC_ATTACK_DATA, PANIC_ATTACK_DATA[DIZZINESS] = True())), COUNTROWS('PANIC_ATTACK_DATA'),0)*100

Age Group  = SWITCH(True(), PANIC_ATTACK_DATA[AGE]<=17, "Child", PANIC_ATTACK_DATA[AGE]<=24, "Adolesent", PANIC_ATTACK_DATA[AGE]<=64,"Adult","Senior")

- Designed interactive dashboards and reports

![Snap_4](https://github.com/user-attachments/assets/968cca78-b89f-47b8-bc8d-53176b2fb90e)

![Snap_5](https://github.com/user-attachments/assets/a0c69102-264c-4327-840f-0e16226691bd)

![Snap_6](https://github.com/user-attachments/assets/883f90ce-a42c-4742-918b-719afa8a7e7e)

8. Insights Generation
- Identified trends, patterns, and key insights
Enabled interactive filtering and drill-down analysis

## Key Findings & Insights
- Sweating (~836 cases) and shortness of breath (~746 cases) are the most common symptoms, making them strong indicators of panic attacks
- Dizziness and trembling are moderately distributed, indicating they are secondary but frequent symptoms
- Most panic attacks last between 20-30 minutes, suggesting short-duration but high-intensity episodes
- Sleep analysis shows majority of individuals sleep 5-7 hours, indicating suboptimal sleep may contribute to panic conditions
- Drinking habits show no extreme concentration, suggesting alcohol is not a primary standalone trigger but may have indirect impact
- Common triggers include caffeine, phobias, and PTSD, with noticeable influence on panic score levels
- Individuals with medical history of anxiety and depression show higher likelihood of panic attacks
- Adult population shows slightly lower sleep levels and more lifestyle-related triggers compared to adolescents
- Interactive dashboard enables identification of high-risk groups based on symptoms, triggers, and demographic filters
