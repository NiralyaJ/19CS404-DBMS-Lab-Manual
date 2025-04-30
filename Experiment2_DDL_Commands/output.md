
**Question 1**

Create a table named Products with the following constraints:
ProductID as INTEGER should be the primary key.
ProductName as TEXT should be unique and not NULL.
Price as REAL should be greater than 0.
StockQuantity as INTEGER should be non-negative.

![Screenshot 2025-04-30 094406](https://github.com/user-attachments/assets/4e2cc8a7-2cfb-4668-989e-3c04dfe9cad6)

**QUERY**

CREATE TABLE Products(,
ProductID integer primary key,,
ProductName varchar(100) unique not null,,
Price Real check(price>0),,
StockQuantity integer check(StockQuantity>0),
);

**Output:**

![Screenshot 2025-04-30 094456](https://github.com/user-attachments/assets/84a95bad-072c-4c86-9ccb-5a92d14dad42)

**Question 2**
Write a SQL query to Add a new column named "discount" with the data type DECIMAL(5,2) to the "customer" table.

Sample table: customer

 customer_id |   cust_name    |    city    | grade | salesman_id 
-------------+----------------+------------+-------+-------------
        3002 | Nick Rimando   | New York   |   100 |        5001
        3007 | Brad Davis     | New York   |   200 |        5001
        3005 | Graham Zusi    | California |   200 |        5002
        
 ![Screenshot 2025-04-30 094519](https://github.com/user-attachments/assets/4bb0831b-ef40-4ead-ac9c-d905c42ed6a8)

**QUERY**

ALTER TABLE customer
ADD COLUMN discount DECIMAL(5,2)

**Output:**

![Screenshot 2025-04-30 094538](https://github.com/user-attachments/assets/7d21cfbd-114a-4508-8abe-cc7ea7e26578)

**Question 3**

Create a new table named contacts with the following specifications:
1.contact_id as INTEGER and primary key.
2.first_name as TEXT and not NULL.
3.last_name as TEXT and not NULL.
4.email as TEXT.
5.phone as TEXT and not NULL with a check constraint to ensure the length of phone is at least 10 characters.

![Screenshot 2025-04-30 094553](https://github.com/user-attachments/assets/959f4a4d-e5af-420e-bedc-3474bb5fde41)

**QUERY**

CREATE TABLE contacts(
contact_id integer primary key,
first_name text not null,
last_name text not null,
email text,
phone text not null check(length(phone)=10));

**Output:**

![Screenshot 2025-04-30 094627](https://github.com/user-attachments/assets/bc28dfd2-ab99-41ea-aefa-f4b7a5565bd4)

**Question 4**
Create a table named ProjectAssignments with the following constraints:
AssignmentID as INTEGER should be the primary key.
EmployeeID as INTEGER should be a foreign key referencing Employees(EmployeeID).
ProjectID as INTEGER should be a foreign key referencing Projects(ProjectID).
AssignmentDate as DATE should be NOT NULL.

![Screenshot 2025-04-30 094650](https://github.com/user-attachments/assets/f70188b2-c8c8-4f5f-8582-0fd92df50cca)

**QUERY**

CREATE TABLE ProjectAssignments(
AssignmentID integer primary key,
EmployeeID integer,
ProjectID integer,
AssignmentDate date not null,
foreign key(EmployeeID) REFERENCES Employees(EmployeeID),
foreign key(ProjectID) REFERENCES Projects(projectID));

**Output:**

![Screenshot 2025-04-30 094706](https://github.com/user-attachments/assets/0b6a911a-842d-4df0-9aa2-7c06a01f7a20)

**Question 5**
Create a table named Events with the following columns:

EventID as INTEGER
EventName as TEXT
EventDate as DATE

![Screenshot 2025-04-30 094721](https://github.com/user-attachments/assets/86acd69d-76b1-4454-9160-9952e77cca28)

**QUERY**

create table Events(
EventID INTEGER,
EventName TEXT,
EventDate DATE
);

**Output:**

![Screenshot 2025-04-30 094737](https://github.com/user-attachments/assets/3886ccad-0dc6-49d9-94a8-eabe063ea55e)

**Question 6**

Create a new table named item with the following specifications and constraints:
1.item_id as TEXT and as primary key.
2.item_desc as TEXT.
3.rate as INTEGER.
4.icom_id as TEXT with a length of 4.
5.icom_id is a foreign key referencing com_id in the company table.
6.The foreign key should cascade updates and deletes.
7.item_desc and rate should not accept NULL.

![Screenshot 2025-04-30 094751](https://github.com/user-attachments/assets/58f39a50-3612-4299-8939-b0225b0e158c)

**QUERY**

CREATE TABLE item(
item_id text primary key,
item_desc text,
rate integer ,
icom_id text check(length(icom_id=4)),
foreign key(icom_id) references company(com_id)
on update cascade
on delete cascade
);

**Output:**

![Screenshot 2025-04-30 094804](https://github.com/user-attachments/assets/726e6efd-4a18-4821-b1f7-6490fd46474d)


**Question 7**

Write a SQL Query  to add attribute ISBN as varchar(30) and domain_dept as varchar(30) in the table 'books'

 ![Screenshot 2025-04-30 094820](https://github.com/user-attachments/assets/83b3a4ea-5508-4de2-9afe-47aa888153c0)

**QUERY**

ALTER TABLE books
ADD ISBN varchar(30);
ALTER TABLE books
ADD domain_dept varchar(30);

**Output:**

![Screenshot 2025-04-30 094834](https://github.com/user-attachments/assets/817aa068-f6e1-4ce1-9aa6-a0699e77fba9)


**Question 8**

Insert the below data into the Employee table, allowing the Department and Salary columns to take their default values.

EmployeeID  Name         Position
----------  -----------  ----------
4           Emily White  Analyst

Note: The Department and Salary columns will use their default values.    

![Screenshot 2025-04-30 094847](https://github.com/user-attachments/assets/5d619261-448e-48c1-b591-2721df610a3a)

**QUERY**

INSERT INTO Employee (EmployeeID,Name,Position)
VALUES(4, 'Emily White', 'Analyst');

**Output:**

![Screenshot 2025-04-30 094858](https://github.com/user-attachments/assets/4be31bc8-48a0-4ee1-b0d5-fc83d7c56fb4)

**Question  9**

Insert all products from Discontinued_products into Products.

Table attributes are ProductID, ProductName, Price, Stock

![Screenshot 2025-04-30 094911](https://github.com/user-attachments/assets/16518ded-1c0a-4a0c-a832-88a97b158c05)

**QUERY**

INSERT INTO Products(ProductID,ProductName,Price,Stock)
SELECT ProductID, ProductName, Price, Stock FROM Discontinued_products;

**Output:**

![Screenshot 2025-04-30 094927](https://github.com/user-attachments/assets/784453b9-1d1f-40e5-b64b-9a3464689f82)

**Question 10**

In the Products table, insert a record where some fields are NULL, another record where all fields are filled without any NULL values, and a third record where some fields are filled, and others are left as NULL.

ProductID   Name              Category    Price       Stock
----------  ---------------   ----------  ----------  ----------
106         Fitness Tracker   Wearables
107         Laptop            Electronics  999.99      50
108         Wireless Earbuds  Accessories              100

 ![Screenshot 2025-04-30 094939](https://github.com/user-attachments/assets/0ca0b4a0-75fd-4eef-b74b-50eeb8e1338c)

**QUERY**

INSERT INTO Products(ProductID, Name, Category, Price,Stock)
VALUES('106','Fitness Tracker','Wearables',NULL,NULL);
INSERT INTO Products(ProductID, Name, Category, Price,Stock)
VALUES('107','Laptop','Electronic','999.99','50');
INSERT INTO Products(ProductID, Name, Category, Price,Stock)
VALUES('108','Wireless Earbud','Accessorie',NULL,'100');

**Output:**

![Screenshot 2025-04-30 094955](https://github.com/user-attachments/assets/c5ac62d7-eccc-43ef-97d6-e428046f61cd)

