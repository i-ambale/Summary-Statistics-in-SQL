# Summary Statistics Report in SQL
© ExploreAI Academy

Project Overview
This repository contains SQL scripts and a Jupyter Notebook demonstrating how to create a summary statistics report using numeric functions and aggregations in SQL.

⚠️ Note: This notebook will not run on Google Colab because it requires a connection to a local MySQL database (united_nations). Ensure that your MySQL Workbench and database are set up on your local machine.

Learning Objectives
By the end of this project, you will:
✅ Learn how to use SQL aggregate functions (e.g., MIN(), MAX(), AVG()).
✅ Understand how to apply the GROUP BY clause for analyzing datasets at different levels.
✅ Perform summary statistics analysis on the Access_to_Basic_Services table.

---

## Setup Instructions
1. Clone the Repository
```sql
git clone https://github.com/i-ambale/Summary-Statistics-SQL.git
cd Summary-Statistics-SQL
```
2. Install Dependencies
Ensure you have the following installed:

- MySQL Server & Workbench

- Python 3.x

- Required Python libraries:
```sql
pip install pymysql sqlalchemy jupyterlab
```
3. Database Connection
```sql
Modify your database connection string in the Jupyter Notebook:
```
```sql
mysql+pymysql://root:your_password@localhost:3306/united_nations
```
4. Run the Notebook
Start Jupyter Notebook and execute the queries:
```sql
jupyter notebook
```
---

## SQL Queries Used
Basic Summary Statistics
```sql
SELECT 
    MIN(Pct_managed_drinking_water_services) AS Min_pct_water,
    MAX(Pct_managed_drinking_water_services) AS Max_pct_water,
    AVG(Pct_managed_drinking_water_services) AS Avg_pct_water
FROM access_to_basic_services;
```
```sql
SELECT 
    Region,
    Sub_region,
    MIN(Pct_managed_drinking_water_services) AS Min_pct_water,
    MAX(Pct_managed_drinking_water_services) AS Max_pct_water,
    AVG(Pct_managed_drinking_water_services) AS Avg_pct_water
FROM access_to_basic_services
GROUP BY Region, Sub_region;
```
---
## Contributors
📌 Ibrahim Ambale – GitHub

## License
This project is released under the MIT License.
