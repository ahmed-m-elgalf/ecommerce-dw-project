# Ecommerce Data Warehousing Project 


### Overview

You are a data engineer at an e-commerce company. Your company needs you to design a data platform that uses MySQL as an OLTP database. You will be using MySQL to store the OLTP data.




### Design the OLTP Database

Create a database named sales.

![Screenshot: ](img/1-1.png )

Design a table named sales_data based on the sample data given.

![Screenshot: ](img/1-2.png )

Import the data from oltpdata.csv into sales_data table using phpMyAdmin.

![Screenshot: ](img/1-3.png )

List the tables in the database

![Screenshot: ](img/1-4.png )

Write a query to find out the count of records in the tables sales_data

![Screenshot: ](img/1-5.png )

Create an index named ts on the timestamp field.

![Screenshot: ](img/1-6.png )

List all indexes created on this table 

![Screenshot: ](img/1-7.png )

Write a bash script named datadump.sh that exports all the rows in the sales_data table to a file named sales_data.sql

![Screenshot: ](img/1-8.PNG )


### Design a Data Warehouse

You are a data engineer hired by an ecommerce company named SoftCart.com . The company retails download only items like E-Books, Movies, Songs etc. The company has international presence and customers from all over the world. The company would like to create a data warehouse so that it can create reports like
- total sales per year per country
- total sales per month per category
- total sales per quarter per country
- total sales per category per country
You will use your data warehousing skills to design and implement a data warehouse for the company.


Design a Data Warehouse using the pgAdmin ERD design tool in Postgres

Using the ERD design tool design the table softcartDimDate. The company is looking at a granularity of a day. Which means they would like to have the ability to generate the report on yearly, monthly, daily, and weekday basis.

![Screenshot: ](img/2-1.png )

Using the ERD design tool design the table softcartDimCategory.

![Screenshot: ](img/2-2.png )

Using the ERD design tool design the table softcartDimItem.

![Screenshot: ](img/2-3.png )

Using the ERD design tool design the table softcartDimCountry.

![Screenshot: ](img/2-4.png )

Using the ERD design tool design the table softcartFactSales.

![Screenshot: ](img/2-5.png )

Using the ERD design tool design the required relationships(one-to-one, one-to-many etc) amongst the tables.

![Screenshot: ](img/2-6.png )

Download the schema sql from ERD tool and create the schema in a database named staging.

![Screenshot: ](img/2-7.png )

### Report Data Warehouse

Create an instance of IBM DB2 database on cloud

Load this data into DimDate table.

![Screenshot: ](img/2-8.png )

Load this data into DimCategory table.

![Screenshot: ](img/2-9.png )

Load this data into DimCountry table.

![Screenshot: ](img/2-10.png )

Load this data into FactSales table.

![Screenshot: ](img/2-11.png )



Create a grouping sets query using the columns country, category, totalsales.

![Screenshot: ](img/2-12.PNG )

Create a rollup query using the columns year, country, and totalsales.

![Screenshot: ](img/2-13.PNG )

Create a cube query using the columns year, country, and average sales.

![Screenshot: ](img/2-14.PNG )

Create an MQT named total_sales_per_country that has the columns country and total_sales.

![Screenshot: ](img/2-15.PNG )


Load sales data history into DB2 database 

![Screenshot: ](img/2-16.png )

Create a line chart of month wise total sales for the year 2020.

![Screenshot: ](img/2-17.png )

Create a pie chart of category wise total sales.

![Screenshot: ](img/2-18.png )

Create a bar chart of Quarterly sales of mobile phones

![Screenshot: ](img/2-19.png )


### ETL – Data Pipeline 
You need to keep data synchronized between different databases/data warehouses as a part of your daily routine. One task that is routinely performed is the sync up of the transactional database and staging data warehouse. Automating this sync-up will save you time and standardize your process.
Create a shell script to 


Extract the data using increamental load from the MySQL database to extract data added in the last 4 hours and then load it into the PostgreSQL Staging warehouse 

Transform the data into staging database and create DimDate 

![Screenshot: ](img/3-1.png )

Transform the data into staging database and create  FactSales table

![Screenshot: ](img/3-2.png )

Export the tables as CSV files for loading into the production warehouse.

![Screenshot: ](img/3-3.PNG )

Schedule a cron job to automate these tasks

![Screenshot: ](img/3-4.png )





