# Sales Analysis Using SQL JOINs and Window Functions

**Student Name:** SUGIRA Kevine  
**Student ID:** 29725  
**Course:** Database Development with PL/SQL  
**Instructor:** Eric Maniraguha  
**Academic Year:** 2025 – 2026  

---

## 1. Business Problem
A retail company stores its sales data across multiple relational tables.  
Management requires advanced SQL analysis to:

- Track customer purchases
- Identify customers with no transactions
- Detect products that are not selling
- Analyze customer spending behavior
- Compare sales performance over time
- Segment customers based on total spending

The goal of this project is to use **SQL JOINs** and **Window Functions** in PostgreSQL to solve these business questions.

---

## 2. Database Schema
The database consists of four related tables:

### Customers
Stores customer details and regions.

### Products
Stores product details and categories.

### Orders
Represents customer purchases by date.

### Order_Items
Stores individual items per order, including quantity and total amount.

Primary keys and foreign keys are used to enforce data integrity.

---

## 3. Entity Relationship Diagram (ERD)
- One **customer** can place many **orders**
- One **order** can contain many **order_items**
- One **product** can appear in many **order_items**

📸 *ERD diagram screenshots are included in the `screenshots/` folder.*

---

## 4. SQL JOIN Queries (Step 4 – Part A)

### 4.1 INNER JOIN
Retrieves transactions with valid customers and products.

![ER Diagram](/Images/INNERJOIN.png)
### LEFT JOIN
Customers who never made a transaction
![ER Diagram](/Images/LEFTJOIN.png)
### RIGHT JOIN
(or FULL JOIN if RIGHT JOIN is avoided) Detect products with no sales activity
![ER Diagram](/Images/RIGHTJOIN.png)

