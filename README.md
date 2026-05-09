# AdventureWorks-2022
Step 1: Data Cleaning & ETL Process
Raw data was stored in a denormalized format with inconsistent data types (e.g., currency symbols and string-based numbers) that prevented mathematical analysis.

Action: Executed SQL scripts to sanitize the dataset by removing non-numeric characters (e.g., $, ,) and casting fields into appropriate Decimal and Integer types.

Key File: cleaning.sql
Step 2: Data Engineering & Star Schema Modeling
To optimize query performance and reporting scalability, the flat data was restructured into a relational Star Schema.

Action: Engineered a robust model by separating data into Fact Tables (Sales, Targets) and Dimension Tables (Products, SalesPersons, Resellers, Date, Territory). Established Primary/Foreign key relationships to ensure data integrity.

Key File: Create Tables.sql

Step 3: Advanced SQL Analytics (Business Insights)
Leveraging advanced SQL techniques to solve complex business questions that simple aggregations cannot answer.

Action: Developed SQL Views using CTEs and Window Functions (SUM() OVER) to calculate:

Sales Gap Analysis: Identifying employees achieving <50% of their quarterly targets.

Pareto Analysis (80/20 Rule): Calculating cumulative profit percentages to isolate the vital few products driving the business.

Churn Analysis: Detecting resellers who purchased in H1 (First Half) but had zero activity in H2, including calculating the "Lost Sales Value."

Key File: Business Questions.sql
Technical Stack & Skills Demonstrated:
SQL: Data Cleaning (ETL), Schema Design, CTEs, Window Functions, DDL/DML.

Power BI: Advanced DAX, Data Modeling, Tooltip/Drill-through Logic.

Business Analysis: Pareto Optimization, Churn Rate Tracking, Gap Analysis.

How to Use this Repository:
Run cleaning.sql to prepare the raw environment.

Execute Create Tables.sql to build the Star Schema.

Use Business Questions.sql to generate the analytical views for reporting.
