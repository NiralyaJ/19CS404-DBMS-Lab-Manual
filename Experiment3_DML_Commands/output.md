**Question 1**
--
Write a SQL statement to Change the category to 'Household' where product name contains 'Detergent' in the products table.



```sql
UPDATE Products
set category='Household'
where product_name LIKE '%Detergent%';

**Output:**

![Output1](output.png)

**Question 2**
---
Write a SQL statement to double the availability of the product with product_id 1.



```sql
UPDATE products
set availability=availability*2
where product_id=1;

```

**Output:**

![Output2](output.png)

**Question 3**
---
Increase the reorder level by 30% for products from 'Food' category having quantity in stock less than 50% of existing reorder level in the products table.

```sql
UPDATE products
set reorder_lvl=reorder_lvl*1.30
where category='Food'
and quantity<(reorder_lvl*0.50);

```

**Output:**

![Output3](output.png)

**Question 4**
---
Write a SQL statement to Update the address to '58 Lakeview, Magnolia' where supplier ID is 5 in the suppliers table.

```sql
update Suppliers
set address='58 Lakeview, Magnolia'
where supplier_id='5';

```

**Output:**

![Output4](output.png)

**Question 5**
---
Write a SQL query to Delete customers from 'customer' table where 'CUST_NAME' contains the substring 'Holmes'.

```sql
delete from Customer
where CUST_NAME LIKE '%HOLMES%';

```

**Output:**

![Output5](output.png)

**Question 6**
---
Write a SQL query to Delete All Doctors with a NULL Last Name

```sql
delete from Doctors
where last_name IS NULL;

```

**Output:**

![Output6](output.png)

**Question 7**
---
Write a SQL query to Delete a Specific Surgery whose ID is 3

```sql
DELETE FROM Surgeries
where surgery_id='3';

```

**Output:**

![Output7](output.png)

**Question 8**
---
Write a SQL query to Delete customers from 'customer' table where 'GRADE' is exactly 2.

```sql
DELETE FROM Customer
WHERE GRADE=2;
```

**Output:**

![Output8](output.png)

**Question 9**
---
Write a SQL query to Delete customers with 'GRADE' 3 or 'AGENT_CODE' 'A008' whose 'OUTSTANDING_AMT' is less than 5000

```sql
DELETE FROM Customer
WHERE (GRADE= 3 OR AGENT_CODE ='A008')
AND OUTSTANDING_AMT<5000;
```

**Output:**

![Output9](output.png)

**Question 10**
---
Write a SQL query to Select all patients whose name starts with A.

```sql
SELECT * FROM Patients
where first_name LIKE 'A%';
```

**Output:**

![Output10](output.png)
