# Crowdfunding_ETL

For the ETL mini project, we worked as a group to build an ETL pipeline using Python, Pandas, and either Python dictionary methods or regular expressions for data extraction and transformation. We created four CSV files and used them to generate an ERD and table schema. Finally, we uploaded the CSV data into a Postgres database. 

##Source Data

Source data can be found in the Resources folder

contacts.xlsx
crowdfunding.xlsx

![QuickDBD-export](https://github.com/AniGEA/Crowdfunding_ETL/assets/158235055/783d49af-89c4-4701-a53a-2dfc37405c8e)

##Instructions

The instructions for this mini project are divided into the following subsections:
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
