**Question 1**
--
Create a table named Products with the following constraints:
ProductID as INTEGER should be the primary key.
ProductName as TEXT should be unique and not NULL.
Price as REAL should be greater than 0.
StockQuantity as INTEGER should be non-negative.

![Screenshot 2025-04-30 220124](https://github.com/user-attachments/assets/690a314c-8a58-4971-9513-6ba79f75978b)


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

![Screenshot 2025-04-30 220510](https://github.com/user-attachments/assets/55246a78-9c52-4ed7-a7b7-ec1addcbf07a)


**Question 2**
---
Write a SQL query to Add a new column named "discount" with the data type DECIMAL(5,2) to the "customer" table.

![Screenshot 2025-04-30 220522](https://github.com/user-attachments/assets/68479e39-c908-472b-aa8a-f0d7d801e508)


**Query:**

```sql

ALTER TABLE customer
ADD COLUMN discount DECIMAL(5,2)

```

**Output:**

![Screenshot 2025-04-30 220535](https://github.com/user-attachments/assets/bc416f42-3a2c-47fb-8de5-c21ce6895407)


**Question 3**
---
Create a new table named contacts with the following specifications:
contact_id as INTEGER and primary key.
first_name as TEXT and not NULL.
last_name as TEXT and not NULL.
email as TEXT.
phone as TEXT and not NULL with a check constraint to ensure the length of phone is at least 10 characters.

![Screenshot 2025-04-30 220547](https://github.com/user-attachments/assets/c0b8305e-734c-42b6-8d17-ab724e65f2db)


**Query:**

```sql

Create a new table named contacts with the following specifications:
contact_id as INTEGER and primary key.
first_name as TEXT and not NULL.
last_name as TEXT and not NULL.
email as TEXT.
phone as TEXT and not NULL with a check constraint to ensure the length of phone is at least 10 characters.

```

**Output:**

![Screenshot 2025-04-30 220601](https://github.com/user-attachments/assets/6540f06d-27f6-484a-a8b2-3ce46f098abd)


**Question 4**
---
Create a table named ProjectAssignments with the following constraints:
AssignmentID as INTEGER should be the primary key.
EmployeeID as INTEGER should be a foreign key referencing Employees(EmployeeID).
ProjectID as INTEGER should be a foreign key referencing Projects(ProjectID).
AssignmentDate as DATE should be NOT NULL.

![Screenshot 2025-04-30 220612](https://github.com/user-attachments/assets/c4b7db4b-c2f7-4f52-8f9e-b8fa3791e430)


**Query:**

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

![Screenshot 2025-04-30 220620](https://github.com/user-attachments/assets/85332812-a85b-4c27-bc01-53dbb8b51363)


**Question 5**
---
Create a table named Events with the following columns:

EventID as INTEGER
EventName as TEXT
EventDate as DATE

![Screenshot 2025-04-30 220626](https://github.com/user-attachments/assets/3c88bf66-a401-4afd-bd8d-df974e06bc75)

**Query:**

```sql

create table Events(
EventID INTEGER,
EventName TEXT,
EventDate DATE
);

```

**Output:**

![Screenshot 2025-04-30 220634](https://github.com/user-attachments/assets/2bf9f615-be51-4152-92fd-3f4dc647fc1d)


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

**Query:**

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

**Query:**

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

**Query:**

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

**Query:**

```sql

INSERT INTO Products(ProductID,ProductName,Price,Stock)
SELECT ProductID, ProductName, Price, Stock FROM Discontinued_products;

```

**Output:**

![Output9](output.png)

**Question 10**
---
In the Products table, insert a record where some fields are NULL, another record where all fields are filled without any NULL values, and a third record where some fields are filled, and others are left as NULL.

**Query:**

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

