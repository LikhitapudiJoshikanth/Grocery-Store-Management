🛒 Grocery Store Management System (SQL Project)
📘 Project Overview

The Grocery Store Management System is a database-driven project designed to efficiently manage the daily operations of a grocery store.
It provides structured data storage for products, customers, suppliers, employees, billing, and inventory, enabling smooth data retrieval and analysis through SQL queries.

🎯 Objectives

To store and manage grocery store data in a relational database.

To perform SQL operations like CRUD (Create, Read, Update, Delete) efficiently.

To analyze sales, stock, and customer data using aggregate and join queries.

To ensure data integrity using primary keys, foreign keys, and constraints.

🗂️ Database Structure
1. Tables Used
Table Name	Description
Products	Stores details of grocery items such as name, category, price, and stock quantity.
Customers	Contains customer information like name, contact, and address.
Suppliers	Holds supplier details and the products they supply.
Employees	Includes store employee data like name, role, and contact.
Orders	Stores information about customer orders.
Order_Details	Contains detailed items within each order.
Payments	Tracks payment methods and transaction details.
🧩 Key SQL Concepts Used

DDL (Data Definition Language):
CREATE, ALTER, DROP, TRUNCATE

DML (Data Manipulation Language):
INSERT, UPDATE, DELETE

DQL (Data Query Language):
SELECT, WHERE, GROUP BY, ORDER BY

Constraints:
PRIMARY KEY, FOREIGN KEY, UNIQUE, NOT NULL, CHECK

Joins:
INNER JOIN, LEFT JOIN, RIGHT JOIN

Functions:
SUM(), AVG(), COUNT(), MAX(), MIN()

Subqueries and Views

Triggers and Stored Procedures (optional)

🧠 Sample Queries

Retrieve all products below minimum stock:

SELECT Product_Name, Quantity 
FROM Products 
WHERE Quantity < 10;


Display total sales by each employee:

SELECT e.Employee_Name, SUM(p.Total_Amount) AS Total_Sales
FROM Payments p
JOIN Employees e ON p.Employee_ID = e.Employee_ID
GROUP BY e.Employee_Name;


List top 5 most sold products:

SELECT Product_ID, SUM(Quantity) AS Total_Sold
FROM Order_Details
GROUP BY Product_ID
ORDER BY Total_Sold DESC
LIMIT 5;

⚙️ Tools & Technologies

Database: MySQL / PostgreSQL / SQL Server

Frontend (optional): Power BI or Excel (for visualization)

Backend (optional): Python or Java (for connectivity demo)

📊 ER Diagram (Entity-Relationship Model)

Main Entities:

Products

Customers

Suppliers

Orders

Employees

Payments

Relationships:

A Customer can place many Orders.

An Order can have multiple Products (via Order_Details).

A Supplier provides many Products.

An Employee handles many Orders.

📈 Use Cases

Store managers can check daily sales reports.

Employees can generate bills for customers.

Suppliers and stock levels can be monitored.

Business analysts can analyze profit and customer trends.

🚀 Future Enhancements

Add triggers for automatic stock updates.

Integrate data visualization dashboards.

Implement role-based access control.

Add expiry tracking for perishable products.

👨‍💻 Author

Name: Likhitapudi Joshikanth
Course: Data Science with Generative AI (Innomatics Research Labs)
Project Type: SQL Database Project
