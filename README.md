# Orders_Analytics
End to end data analytics project using python and SQL. We will use a Kaggle dataset, while doing data processing and cleaning using pandas and load the data into sql server. We will answer some questions using SQL.


Steps taken in this project,

First part ETL (Extract, Transform, Load)

Cleaning data

First I found any values that were Not available or unknown and chnaged them to NULL.

Then I fixed the column names making each column name lower case and remove the space between words and replacing it with a underscore.

Then I added new columns based on what columns we had, which were NEW COLUMNS discount, sale price and profit.

REMOVED 'discount percent', 'list price' and 'cost price'. These columns were removed as they were not needed for the questions I wanted to answer.

We also changed the datatype for order_date to datetime format.

Then we connected our MySQL database to our code, we originally let our code create a table in the database but that we making the database use the incorrect datatypes. So instead I dropped the table that was intially made then Created a new table in SQL with the correct datatypes. From this I then adjusted the code from replaced the table to append. From the the connection was successful.

In order to not share passwords I used a db_config, which will not be included in this repo using .gitignore.

db_config file should like this:

host "localhost"

port 3306

user "YOUR USER NAME"

password YOUR PASSWORD HERE"

database "DATABASE TABLE NAME"


