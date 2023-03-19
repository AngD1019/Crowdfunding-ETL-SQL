# Crowdfunding-ETL

## Project Overview 

Independent Funding is a crowdfunding platform for funding independent projects or ventures. This company has been growing, so now it needs to move all their accessible data from one large Excel file onto a PostgreSQL database. This way, the analytics team will be able to perform analysis and create reports for company stakeholders as well as individuals who donate to projects.

In preparation for this project, I was tasked with the following: 
* Extracting and transforming the data from the large Excel file into four separate CSV files
* Creating a PostgreSQL database and tables by using an ERD
* Loading the CSV files into the database
* Performing SQL queries to generate reports for stakeholders

Using the analysis performed with the Crowdfunding ETL project and SQL data analysis, the purpose of this project is to perform both an ETL process and a data analysis by using SQL queries on the crowdfunding dataset. This dataset holds information showing the backers who have pledged to the live projects.

Python, Pandas, and Jupyter notebooks were used to extract and transform the backers’ contact information from a CSV file to create a DataFrame that will be exported as a CSV file. In the load phase, the dataset was used to create an ERD and a table schema to create a new table in the crowdfunding_db database. The CSV file that contains the backers’ information into this table was uploaded into this table. And finally, data analysis was performed on the crowdfunding_db database by using SQL queries.

## Deliverables

### Deliverable 1: Extract Data (35 pts)
* The alphanumeric "backer_id" string identification number is extracted without extra characters.
* The numeric "cf_id" string identification number is extracted without extra characters. 
* The "name" string value is extracted without extra characters. 
* The "email" string value is extracted without extra characters. 
* A DataFrame is created with the following columns: "backer_id", "cf_id", "name", and "email" and each column in the DataFrame contains the appropriate data. 

<img width="500" alt="Deliv1DF" src="https://user-images.githubusercontent.com/114960958/226147647-3f71c32a-9d63-4a8d-becb-2a0af9c1678c.png">


### Deliverable 2: Transform and Clean Data
* The "cf_id" column is converted to int64.
* The "name" column is split into "first_name" and "last_name" columns that are added to the DataFrame. 
* The "name" column is dropped from the DataFrame. 
* The columns are reordered. 
* The DataFrame is exported as backers.csv. 

### Deliverable 3: Create an ERD and a Table Schema and Load the Data
* The crowdfunding_db relationship diagram has five tables, and the diagram is saved as crowdfunding_db_relationships.png.
* The crowdfunding_db_schema.sql file contains the table schema and the ALTER TABLE statement for each of the five tables. 
* The backers.csv file is imported into the backers table without any errors. 

![crowdfunding_db_relationships](https://user-images.githubusercontent.com/114960958/226147573-f4f77736-facd-405a-b835-9bf491ad59e8.png)

![crowdfunding_db_schema](https://user-images.githubusercontent.com/114960958/226147605-17ee6921-1ce4-4062-b62c-2e3790f8a733.png)

### Deliverable 4: SQL Analysis (15 pts)
* A SQL query is written and successfully executed that retrieves the number of backer_counts in descending order for each cf_id and for all the live campaigns. 
* A SQL query is written and successfully executed that retrieves the number of backers in descending order for each cf_id from the backers table. 
* A SQL query is written and successfully executed to create the email_contacts_remaining_goal_amount table, and the table is exported as email_contacts_remaining_goal_amount.csv. 
* A SQL query is written and successfully executed to create the email_backers_remaining_goal_amount table, and the table is exported as email_contacts_remaining_goal_amount.csv. 
