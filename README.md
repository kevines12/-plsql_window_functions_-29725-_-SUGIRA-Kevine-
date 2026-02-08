# Sales Analysis Using SQL JOINs and Window Functions

**Student Name:** SUGIRA Kevine  
**Student ID:** 29725  
**Course:** Database Development with PL/SQL  
**Instructor:** Eric Maniraguha  
**Academic Year:** 2025 – 2026  



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



## 3. Entity Relationship Diagram (ERD)
- One **customer** can place many **orders**
- One **order** can contain many **order_items**
- One **product** can appear in many **order_items**


![ER Diagram](/Images/ERD.png)


## 4. SQL JOIN Queries (Step 4 – Part A)

### 4.1 INNER JOIN
Retrieves transactions with valid customers and products.

![ER Diagram](/Images/INNERJOIN.png)
### LEFT JOIN
Customers who never made a transaction
![ER Diagram](/Images/LEFTJOIN.png)
### RIGHT JOIN
(or FULL JOIN if RIGHT JOIN is avoided) Detect products with no sales activity

![ER Diagram](/Images/RIGHTJOINT.png)
### FULL OUTER JOIN 
Compare customers and products including unmatched records

![ER Diagram](/Images/FULLOUTERJOIN.png)

### SELF JOIN 
Compare customers within the same region or transactions within the same time period

![ER Diagram](/Images/SELFJOIN.png)

### Part B — Window Functions Implementation

 ### Ranking Functions
 ROW_NUMBER(), RANK(), DENSE_RANK(), PERCENT_RANK() Use case: Top N
customers or products by revenue

![ER Diagram](/Images/RANKINGFUNCTION.png)

### Aggregate Window Functions 
SUM(), AVG(), MIN(), MAX() Use both ROWS and RANGE frames Use
case: Running totals and trends

![ER Diagram](/Images/AGGREGATEWINDOWFUNCTION.png)

### Navigation Functions 
LAG(), LEAD() Use case: Period-to-period comparison and growth

![ER Diagram](/Images/NAVIGATIONFUNCTION.png)

### Distribution Functions
NTILE(4), CUME_DIST() Use case: Customer segmentation

![ER Diagram](/Images/DISTRIBUTIONFUNCTION.png)


##  Step 7: Results Analysis

### 1️ Descriptive Analysis — What happened?
- Sales transactions were recorded across multiple customers, products, and time periods.
- A small number of customers generated the majority of total revenue.
- Electronics products contributed higher sales values compared to furniture products.
- Sales activity showed an upward trend over time.
- Some registered customers did not make any purchases.

### 2️ Diagnostic Analysis — Why did it happen?
- Electronics products have higher unit prices, leading to higher revenue.
- Customers with multiple orders accumulated higher total spending.
- Inactive customers may be newly registered or not yet engaged.
- Increasing sales over time suggests improved engagement or demand.
- Customers within the same region exhibited similar purchasing patterns.

### 3️ Prescriptive Analysis — What should be done next?
- Focus loyalty programs and promotions on high-value customers.
- Create engagement strategies to activate customers with no purchases.
- Promote low-performing products through discounts or bundles.
- Continuously monitor sales trends to improve forecasting.
- Use customer segmentation results to apply personalized marketing strategies.

---

##  Step 8: References

1. PostgreSQL Global Development Group.  
   *PostgreSQL Official Documentation.*  
   https://www.postgresql.org/docs/

2. Oracle Corporation.  
   *SQL Window Functions Documentation.*  
   https://docs.oracle.com/en/database/

3. Mode Analytics.  
   *SQL Window Functions Tutorial.*  
   https://mode.com/sql-tutorial/sql-window-functions/

4. Kimball, R., & Ross, M.  
   *The Data Warehouse Toolkit.* Wiley Publishing.

---

##  Integrity Statement

“All sources were properly cited. Implementations and analysis represent original work. No AI-generated content was copied without attribution or adaptation.”

