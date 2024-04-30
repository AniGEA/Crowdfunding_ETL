# Crowdfunding_ETL

For the ETL mini project, we worked as a group to build an ETL pipeline using Python, Pandas, and either Python dictionary methods or regular expressions for data extraction and transformation. We created four CSV files and used them to generate an ERD and table schema. Finally, we uploaded the CSV data into a Postgres database. 


## CSV Tables

Created CSV files can be found in CSV folder

- campaign.csv
- category.csv
- subcategory.csv
- contacts.csv

## Source Data

Source data can be found in the Resources folder

- contacts.xlsx
- crowdfunding.xlsx


## ERD (Entity Relationship Diagram)

An Entity Relationship Diagram (ERD) of the 4 tables was generated using QuickDBD https://www.quickdatabasediagrams.com/ to illustrate the database structure visually.

![QuickDBD-export](https://github.com/AniGEA/Crowdfunding_ETL/assets/158235055/783d49af-89c4-4701-a53a-2dfc37405c8e)

## Instructions

The instructions for this mini-project are divided into the following subsections:
Create the Category and Subcategory DataFrames
Create the Campaign DataFrame
Create the Contacts DataFrame
Create the Crowdfunding Database
Create the Category and Subcategory DataFrames

1. Extract and transform the crowdfunding.xlsx Excel data to create a category DataFrame that has the following columns:
- A "category_id" column that has entries going sequentially from "cat1" to "catn", where n is the number of unique categories
- A "category" column that contains only the category titles
- The following image shows this category DataFrame:
<img width="190" alt="category_DataFrame" src="https://github.com/AniGEA/Crowdfunding_ETL/assets/158235055/ba572cd1-6bb6-438a-90b3-1790e1230406">

2. Export the category DataFrame as category.csv and save it to your GitHub repository.
3. Extract and transform the crowdfunding.xlsx Excel data to create a subcategory DataFrame that has the following columns:
- A "subcategory_id" column that has entries going sequentially from "subcat1" to "subcatn", where n is the number of unique subcategories
- A "subcategory" column that contains only the subcategory titles
- The following image shows this subcategory DataFrame:
<img width="250" alt="subcategory_DataFrame" src="https://github.com/AniGEA/Crowdfunding_ETL/assets/158235055/8f11a077-f968-4516-87c3-f56e1ac59c53">

4. Export the subcategory DataFrame as subcategory.csv and save it to your GitHub repository.

## Create the Campaign DataFrame

1. Extract and transform the crowdfunding.xlsx Excel data to create a campaign DataFrame has the following columns:
- The "cf_id" column
- The "contact_id" column
- The "company_name" column
- The "blurb" column, renamed to "description"
- The "goal" column, converted to the float data type
- The "pledged" column, converted to the float data type
- The "outcome" column
- The "backers_count" column
- The "country" column
- The "currency" column
- The "launched_at" column, renamed to "launch_date" and with the UTC times converted to the datetime format
- The "deadline" column, renamed to "end_date" and with the UTC times converted to the datetime format
- The "category_id" column, with unique identification numbers matching those in the "category_id" column of the category DataFrame
- The "subcategory_id" column, with the unique identification numbers matching those in the "subcategory_id" column of the subcategory DataFrame
- The following image shows this campaign DataFrame:

  <img width="1074" alt="campaign_DataFrame" src="https://github.com/AniGEA/Crowdfunding_ETL/assets/158235055/8584c9c6-1f77-497d-887a-e27f1f65982d">

 2. Export the campaign DataFrame as campaign.csv and save it to your GitHub repository.

 ## Create the Contacts DataFrame

1. Choose one of the following two options for extracting and transforming the data from the contacts.xlsx Excel data:
- Option 1: Use Python dictionary methods.
- Option 2: Use regular expressions.
2. If you chose Option 1, complete the following steps:
- Import the contacts.xlsx file into a DataFrame.
- Iterate through the DataFrame, converting each row to a dictionary.
- Iterate through each dictionary, doing the following:
- - Extract the dictionary values from the keys by using a Python list comprehension.
- - Add the values for each row to a new list.
- Create a new DataFrame that contains the extracted data.
- Split each "name" column value into a first and last name, and place each in a new column.
- Clean and export the DataFrame as contacts.csv and save it to your GitHub repository.
3. If you chose Option 2, complete the following steps:
- Import the contacts.xlsx file into a DataFrame.
- Extract the "contact_id", "name", and "email" columns by using regular expressions.
- Create a new DataFrame with the extracted data.
- Convert the "contact_id" column to the integer type.
- Split each "name" column value into a first and a last name, and place each in a new column.
- Clean and then export the DataFrame as contacts.csv and save it to your GitHub repository.
  
4. Check that your final DataFrame resembles the one in the following image:
  
<img width="415" alt="contact_DataFrame_final" src="https://github.com/AniGEA/Crowdfunding_ETL/assets/158235055/809ac322-5ff6-4c96-b271-4cd7ce04ce49">



## Create the Crowdfunding Database

1. Inspect the four CSV files, and then sketch an ERD of the tables by using QuickDBD Links to an external site..
2. Use the information from the ERD to create a table schema for each CSV file.
- Note: Remember to specify the data types, primary keys, foreign keys, and other constraints.
3. Save the database schema as a Postgres file named crowdfunding_db_schema.sql, and save it to your GitHub repository.
4. Create a new Postgres database, named crowdfunding_db.
5. Using the database schema, create the tables in the correct order to handle the foreign keys.
6. Verify the table creation by running a SELECT statement for each table.
7. Import each CSV file into its corresponding SQL table.
8. Verify that each table has the correct data by running a SELECT statement for each.




