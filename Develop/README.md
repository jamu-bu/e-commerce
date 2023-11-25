# E-commerce Back End using Express.js, Sequelize, and MySQL

## Project Description

This project involves building the back end for an e-commerce site using Express.js, Sequelize as the ORM, and MySQL as the database. The goal is to create a robust API that allows for seamless interactions with the database, enabling the internet retail company to stay competitive in the e-commerce market.

## User Story

AS A manager at an internet retail company
I WANT a back end for my e-commerce website that uses the latest technologies
SO THAT my company can compete with other e-commerce companies

## Usage

Add database name, MySQL username, and MySQL password to an environment variable file.
Connect to the database using Sequelize.
Database Initialization:
Execute schema and seed commands to create a development database.
Seed the database with test data.
Server Initialization:
Start the application.
Ensure Sequelize models are synced with the MySQL database.
API Routes:
Test API GET routes in Insomnia for categories, products, or tags.
Verify that the data for each route is displayed in formatted JSON.
Data Manipulation:
Test API POST, PUT, and DELETE routes in Insomnia.
Successfully create, update, and delete data in the database.

## Database Models
Category

id: Integer, Primary key, Auto increment
category_name: String, Not null
Product

id: Integer, Primary key, Auto increment
product_name: String, Not null
price: Decimal, Not null, Validates as a decimal
stock: Integer, Not null, Default value of 10, Validates as numeric
category_id: Integer, References the category model's id
Tag

id: Integer, Primary key, Auto increment
tag_name: String
ProductTag

id: Integer, Primary key, Auto increment
product_id: Integer, References the product model's id
tag_id: Integer, References the tag model's id
Associations
Product belongs to Category.
Category has many Product models.
Product belongs to many Tag models through ProductTag.
Tag belongs to many Product models.
Instructions to Run the App
Create a .env file in the root of the app.
Add the following details to the .env file:
DB_NAME='ecommerce_db'
DB_USER='root'
DB_PW='xxx'
Run the application using npm start.
Follow these steps to set up, configure, and run the e-commerce back end. Ensure that the application meets all acceptance criteria for a functional and competitive e-commerce API.





