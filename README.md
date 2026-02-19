
# E-Commerce Data Loading (CSV to PostgreSQL)

This project demonstrates a Python-based process to create relational tables and load structured E-Commerce CSV data into a PostgreSQL database.

## Project Objective

- Create relational tables in PostgreSQL  
- Apply primary key and foreign key constraints  
- Load structured CSV data into the database  
- Maintain referential integrity across tables  

## Process Overview

1. Read CSV files using **pandas**
   - orders (sampled 10,000 rows)
   - order_products (sampled 10,000 rows)
   - products
   - aisles
   - departments

2. Connect to PostgreSQL using:
   - `psycopg2` for executing table creation statements  
   - `SQLAlchemy` for inserting data  

3. Create relational tables:
   - `aisles`
   - `departments`
   - `products` (with foreign keys)
   - `orders`
   - `order_products` (composite primary key)

4. Drop the `eval_set` column from the orders dataset before loading.

5. Insert data into PostgreSQL using `DataFrame.to_sql()`.

## Database Details

- Database Name: `ecom_analysis`
- Port: `5432`
- PostgreSQL

## Technologies Used

- Python  
- pandas  
- psycopg2  
- SQLAlchemy  
- PostgreSQL  

This project demonstrates connecting Python to PostgreSQL, creating relational tables with constraints, and loading structured CSV data into a database.
