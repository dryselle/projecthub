## Title
Department-Level Engagement Analysis
## Problem Statement
The company’s overall engagement index is 2.99, falling below the acceptable benchmark range of 3.4–4.1. All departments also score below benchmark, indicating organization-wide disengagement and increased people risk.
## Data
The data was obtained from kaggle.com with records from 2018-2023.
## Methodology
For Data Cleaning and Data Manipulation, MS Excel and MySQL Workbench were used. 

MS Excel Data Manipulation:
- Standardized the data format for the 'DATE' columns to dd-mmm-yyyy.
- Remove unnecessary columns.

Once the dataset was cleaned, it was imported to MySQL Workbench with the database name 'project'.
- All columns were uploaded as a 'TEXT' datatype.
- In order to transform the DATE columns to its correcr data type, the following queries were made;
  Because MySQL only recognizes the date format yyyy-mm-dd, the format was converted using the string to date function. Once it has been updated, the tables were altered and columns modified.
  For the Exit Date column, because there were blank fields, it had to be filled in as NULL in order for the column to be modified as DATE.

For Exploratory Data Analysis, a combination of MS Excel and SQL for advance querying were utilized.
- Went through the KPIs that are commonly used in Human Resource environment.
- Did a business logic check, that is, validating that the relationships between fields in a dataset make sense according to domain knowledge or real-world expectations.
- After the initial analysis, it was decided to focus on the Engagement Index KPI.

Employee Engagement Diagnostic Analysis
1. Survey Period Identification and Year Classification
Employee engagement surveys were conducted across two time periods:
- August–December 2022
- January–August 2023
To ensure accurate year-over-year comparison, survey responses were classified by survey year based on the collection period. This step was necessary to prevent overlap and to ensure that engagement scores were correctly attributed to the appropriate year.

2. Engagement Index Construction
An Engagement Index was created to serve as a consolidated measure of employee commitment and experience.
The Engagement Index was calculated as the average of three survey dimensions:
- Engagement Score
- Satisfaction Score
- Work-Life Balance Score
This composite index allowed for a more holistic assessment of engagement rather than relying on a single metric.

3. Department-Level Engagement Analysis
Once the Engagement Index was calculated for each survey year, the analysis was conducted at the department level.
Key findings included:
- In 2022, the Admin Office recorded the lowest Engagement Index (2.51).
- In 2023, the Production department recorded the lowest Engagement Index (2.95).
This step helped identify which departments were experiencing the most significant engagement challenges in each year.

4. Driver Analysis of Engagement Index Components
To understand why engagement scores were low, the analysis focused on the underlying drivers of the Engagement Index—specifically Satisfaction and Work-Life Balance.
a. Satisfaction Analysis (Salary Range)
Satisfaction was further examined by analyzing employees’ salary range:
- Employees were categorized based on salary range levels.
- For each department and survey year, the number of employees in lower salary ranges was counted.
This count was divided by the total department headcount for the corresponding year to calculate the percentage of employees potentially impacted by compensation concerns.

b. Work-Life Balance Analysis (Workload)
Work-Life Balance was analyzed by examining excessive workload:
- Employees reporting being overloaded with work were identified.
- The number of affected employees per department and survey year was divided by the total department headcount.
Results were expressed as percentages to allow comparison across departments of different sizes.

5. Analytical Approach and Tools
The analysis was conducted using Excel’s Data Model, leveraging:
- Filtering by department and survey year
- Aggregation of employee counts
- Percentage calculations to normalize results across departments
This approach enabled consistent, comparable insights while maintaining transparency in the calculation logic.

Root Cause Analysis Tool: 5 Whys

## Results
Further analysis indicates that salary range and workload distribution were not primary contributors to the low Engagement Index observed in this case. Departments with lower engagement did not exhibit disproportionately higher concentrations of employees in lower salary ranges nor higher levels of excessive workload compared to other departments.

This result suggests that the engagement challenge is not driven by compensation or workload factors, but rather points toward non-financial and cultural drivers of engagement.

Based on this shift in findings, the following potential root causes were identified:
- Leadership style and communication
  - Possible gaps in recognition, clarity of direction, and the effectiveness of feedback mechanisms may be influencing employee engagement.
- Career development and progression
  - Limited growth opportunities or unclear career pathways may be reducing long-term motivation and commitment.
- Work environment and team dynamics
  - Perceptions related to fairness, inclusion, and team cohesion may be weaker, particularly within administrative functions.
- Organizational alignment
  - Employees may feel disconnected from the organization’s mission or perceive their contributions as less valued compared to other departments.
  
## Recommendation
- Conduct targeted focus groups
  - Gather qualitative feedback from Admin Offices employees to uncover specific pain points (e.g., leadership, recognition, career growth).
- Enhance recognition & communication
  - Implement regular check-ins, transparent communication, and recognition programs tailored to Admin Offices.
- Career development pathways
  - Offer training, mentorship, or rotational opportunities to increase engagement through growth.
- Culture & inclusion initiatives
  - Strengthen team-building and inclusion practices to improve belonging and morale.
- Monitor with pulse surveys
  - Track engagement quarterly to see if interventions are improving scores.

