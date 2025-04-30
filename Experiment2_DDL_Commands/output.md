**Question 1**
--
Create a table named Products with the following constraints:
ProductID as INTEGER should be the primary key.
ProductName as TEXT should be unique and not NULL.
Price as REAL should be greater than 0.
StockQuantity as INTEGER should be non-negative.

**Query:**

```sql

CREATE TABLE Products(
ProductID integer primary key,
ProductName varchar(100) unique not null,
Price Real check(price>0),
StockQuantity integer check(StockQuantity>0)
);

```

**Output:**

![Output1](output.png)

**Question 2**
---
Write a SQL query to Add a new column named "discount" with the data type DECIMAL(5,2) to the "customer" table.


```sql

ALTER TABLE customer
ADD COLUMN discount DECIMAL(5,2)

```

**Output:**

![Output2](output.png)

**Question 3**
---
Create a new table named contacts with the following specifications:
contact_id as INTEGER and primary key.
first_name as TEXT and not NULL.
last_name as TEXT and not NULL.
email as TEXT.
phone as TEXT and not NULL with a check constraint to ensure the length of phone is at least 10 characters.



```sql

Create a new table named contacts with the following specifications:
contact_id as INTEGER and primary key.
first_name as TEXT and not NULL.
last_name as TEXT and not NULL.
email as TEXT.
phone as TEXT and not NULL with a check constraint to ensure the length of phone is at least 10 characters.

```

**Output:**

![Output3](output.png)

**Question 4**
---
Create a table named ProjectAssignments with the following constraints:
AssignmentID as INTEGER should be the primary key.
EmployeeID as INTEGER should be a foreign key referencing Employees(EmployeeID).
ProjectID as INTEGER should be a foreign key referencing Projects(ProjectID).
AssignmentDate as DATE should be NOT NULL.



```sql

CREATE TABLE ProjectAssignments(
AssignmentID integer primary key,
EmployeeID integer,
ProjectID integer,
AssignmentDate date not null,
foreign key(EmployeeID) REFERENCES Employees(EmployeeID),
foreign key(ProjectID) REFERENCES Projects(projectID));

```

**Output:**

![Output4](output.png)

**Question 5**
---
Create a table named Events with the following columns:

EventID as INTEGER
EventName as TEXT
EventDate as DATE



```sql

create table Events(
EventID INTEGER,
EventName TEXT,
EventDate DATE
);

```

**Output:**

![Output5](output.png)

**Question 6**
---
Create a new table named item with the following specifications and constraints:
1.item_id as TEXT and as primary key.
2.item_desc as TEXT.
3.rate as INTEGER.
4.icom_id as TEXT with a length of 4.
5.icom_id is a foreign key referencing com_id in the company table.
6.The foreign key should cascade updates and deletes.
7.item_desc and rate should not accept NULL.



```sql

CREATE TABLE item(
item_id text primary key,
item_desc text,
rate integer ,
icom_id text check(length(icom_id=4)),
foreign key(icom_id) references company(com_id)
on update cascade
on delete cascade
);

```

**Output:**

![Output6](output.png)

**Question 7**
---
Write a SQL Query  to add attribute ISBN as varchar(30) and domain_dept as varchar(30) in the table 'books'



```sql

ALTER TABLE books
ADD ISBN varchar(30);
ALTER TABLE books
ADD domain_dept varchar(30);

```

**Output:**

![Output7](output.png)

**Question 8**
---
Insert the below data into the Employee table, allowing the Department and Salary columns to take their default values.



```sql

INSERT INTO Employee (EmployeeID,Name,Position)
VALUES(4, 'Emily White', 'Analyst');

```

**Output:**

![Output8](output.png)

**Question 9**
---
Insert all products from Discontinued_products into Products.

Table attributes are ProductID, ProductName, Price, Stock



```sql

INSERT INTO Products(ProductID,ProductName,Price,Stock)
SELECT ProductID, ProductName, Price, Stock FROM Discontinued_products;

```

**Output:**

![Output9](output.png)

**Question 10**
---
In the Products table, insert a record where some fields are NULL, another record where all fields are filled without any NULL values, and a third record where some fields are filled, and others are left as NULL.


```sql

INSERT INTO Products(ProductID, Name, Category, Price,Stock)
VALUES('106','Fitness Tracker','Wearables',NULL,NULL);
INSERT INTO Products(ProductID, Name, Category, Price,Stock)
VALUES('107','Laptop','Electronic','999.99','50');
INSERT INTO Products(ProductID, Name, Category, Price,Stock)
VALUES('108','Wireless Earbud','Accessorie',NULL,'100');

```

**Output:**

![Output10](output.png)


## RESULT
Thus, the SQL queries to implement different types of constraints and DDL commands have been executed successfully.

