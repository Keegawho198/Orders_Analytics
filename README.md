# Orders_Analytics

## Overview


This is an end-to-end data analytics project that utilizes Python and SQL to analyze and process sales data from a Kaggle dataset. The project involves cleaning and transforming data using pandas, loading the data into MySQL, and answering various business-related questions using SQL.

Technologies Used:


Python: Data cleaning and processing using pandas.

SQL: Data analysis and querying in MySQL.

MySQL Server: Database for storing and managing the dataset.


## Project Steps

## ETL Process (Extract, Transform, Load)

a. Extract
Data was extracted from a Kaggle dataset, which contains sales data.

b. Transform
Data Cleaning:
Identified and replaced missing or unknown values with NULL.

Standardized column names by converting them to lowercase and replacing spaces with underscores for consistency.


Column Adjustments:
Created new columns based on existing data, including discount, sale_price, and profit.

Removed unnecessary columns such as discount_percent, list_price, and cost_price since they were not needed for the analysis.

Data Type Adjustments:
Converted order_date column to datetime format for better querying and analysis.

c. Load
Connected to MySQL and initially allowed the code to create a table. However, due to incorrect data types being used, the table was dropped and a new table was created with the correct data types.

Adjusted the code to append data to the new table, ensuring data integrity and correctness.


## Database Connection & Configuration
The project securely connects to the MySQL database by using a db_config file (which should be excluded from the repository for security purposes).

The db_config file should look like this:
python
Copy

Edit below
{

    "host": "localhost",

    "port": 3306,

    "user": "YOUR USER NAME",

    "password": "YOUR PASSWORD HERE",

    "database": "DATABASE TABLE NAME"

}

Note: The db_config file should be added to .gitignore to avoid sharing sensitive credentials in version control.


## SQL Analysis

Once the data was loaded into the MySQL database, several key business questions were answered using SQL queries. Some examples of the analyses performed include:

Top Selling Products by Region: Identified the top 10 products with the highest sales for each region.

Month-over-Month Growth: Compared sales growth between January 2022 and January 2023, and across other months.

Highest Growth by Profit: Identified which subcategory had the highest profit growth between 2022 and 2023.



## Project Structure

Analysis.py: Python script for data cleaning, transformation, and loading into MySQL.

sql_exploration.sql: SQL file containing the queries used to analyze the data.

create_sql_table: SQL for creating the table with correct datatypes

db_config.py: Contains the database connection details (not included in the repo for security reasons).

.gitignore: Ensures that sensitive files like db_config.py are not shared.




## Future Improvements

Data Visualization: Create visualizations to complement the SQL analysis using libraries like matplotlib or seaborn.

Automated Data Pipeline: Set up an automated pipeline for recurring data updates and analysis.

Advanced SQL Analytics: Explore more advanced SQL techniques such as window functions and subqueries to gain deeper insights.

End to end data analytics project using python and SQL. We will use a Kaggle dataset, while doing data processing and cleaning using pandas and load the data into sql server. We will answer some questions using SQL.
