**Question 1**
--
Write a SQL statement to Change the category to 'Household' where product name contains 'Detergent' in the products table.

![Screenshot 2025-04-30 202624](https://github.com/user-attachments/assets/72da86a8-c33b-4b39-93a4-ee31818be15c)

**Query:**

```sql
UPDATE Products
set category='Household'
where product_name LIKE '%Detergent%';

```

**Output:**

![Screenshot 2025-04-30 202720](https://github.com/user-attachments/assets/6e85f95d-670b-4f40-95d8-0acb7938652c)

**Question 2**
--
Write a SQL statement to double the availability of the product with product_id 1.

![Screenshot 2025-04-30 202742](https://github.com/user-attachments/assets/8e28805f-7112-42ec-9223-a6a049a07736)

**Query:**

```sql
UPDATE products
set availability=availability*2
where product_id=1;

```

**Output:**

![Screenshot 2025-04-30 202753](https://github.com/user-attachments/assets/b4e8dfde-fd88-4659-b5bc-0b1d245e77b4)

**Question 3**
---
Increase the reorder level by 30% for products from 'Food' category having quantity in stock less than 50% of existing reorder level in the products table.

![Screenshot 2025-04-30 202753](https://github.com/user-attachments/assets/2b7bba17-31e7-47ce-aa18-95bf02be09da)

**Query:**

```sql
UPDATE products
set reorder_lvl=reorder_lvl*1.30
where category='Food'
and quantity<(reorder_lvl*0.50);

```

**Output:**

![Screenshot 2025-04-30 202911](https://github.com/user-attachments/assets/22e6f0d7-0a4d-4f4a-b319-fde808daa90e)

**Question 4**
---
Write a SQL statement to Update the address to '58 Lakeview, Magnolia' where supplier ID is 5 in the suppliers table.

![Screenshot 2025-04-30 202933](https://github.com/user-attachments/assets/9b8b79fc-ef52-4729-b5c6-91a6acf121c1)

**Query:**

```sql
update Suppliers
set address='58 Lakeview, Magnolia'
where supplier_id='5';

```

**Output:**

![Screenshot 2025-04-30 202956](https://github.com/user-attachments/assets/cbdde854-3e3d-4c24-a5aa-1d2408ab1f37)


**Question 5**
---
Write a SQL query to Delete customers from 'customer' table where 'CUST_NAME' contains the substring 'Holmes'.

![Screenshot 2025-04-30 203034](https://github.com/user-attachments/assets/66a441f7-1273-4d3f-acab-320d0ab6ee73)

**Query:**

```sql
delete from Customer
where CUST_NAME LIKE '%HOLMES%';

```

**Output:**

![Screenshot 2025-04-30 203115](https://github.com/user-attachments/assets/6467c529-751f-4bd9-9ff1-6f406caf110d)


**Question 6**
---
Write a SQL query to Delete All Doctors with a NULL Last Name

![Screenshot 2025-04-30 203135](https://github.com/user-attachments/assets/7bdcf218-18fa-4d9c-96af-30f14ee4e564)

**Query:**

```sql
delete from Doctors
where last_name IS NULL;

```

**Output:**

![Screenshot 2025-04-30 203151](https://github.com/user-attachments/assets/4216fcf4-0a6b-455a-8e14-3ec126e85212)


**Question 7**
---
Write a SQL query to Delete a Specific Surgery whose ID is 3

![Screenshot 2025-04-30 203210](https://github.com/user-attachments/assets/7bd3bdaf-ea92-43d2-b48e-68a2d21df465)

**Query:**

```sql
DELETE FROM Surgeries
where surgery_id='3';

```

**Output:**

![Screenshot 2025-04-30 203220](https://github.com/user-attachments/assets/cbc6df2c-586b-4d2d-82cb-7d51b2bdff71)


**Question 8**
---
Write a SQL query to Delete customers from 'customer' table where 'GRADE' is exactly 2.

![Screenshot 2025-04-30 203239](https://github.com/user-attachments/assets/917e6686-0a63-4e6e-a164-053935d51494)

**Query:**

```sql
DELETE FROM Customer
WHERE GRADE=2;
```

**Output:**

![Screenshot 2025-04-30 203251](https://github.com/user-attachments/assets/5c1c0eeb-7663-427d-a603-3ce06043f7af)


**Question 9**
---
Write a SQL query to Delete customers with 'GRADE' 3 or 'AGENT_CODE' 'A008' whose 'OUTSTANDING_AMT' is less than 5000

![Screenshot 2025-04-30 203251](https://github.com/user-attachments/assets/8570bc82-b9bb-4b7b-bc8b-254ded953ca3)

**Query:**

```sql
DELETE FROM Customer
WHERE (GRADE= 3 OR AGENT_CODE ='A008')
AND OUTSTANDING_AMT<5000;
```

**Output:**

![Screenshot 2025-04-30 203341](https://github.com/user-attachments/assets/32f38250-c560-4405-87f7-a90a9d1e371f)


**Question 10**
---
Write a SQL query to Select all patients whose name starts with A.

![Screenshot 2025-04-30 203411](https://github.com/user-attachments/assets/0ca8a10b-923a-4653-83a6-d703004079be)

**Query:**

```sql
SELECT * FROM Patients
where first_name LIKE 'A%';
```

**Output:**

![Screenshot 2025-04-30 203411](https://github.com/user-attachments/assets/5a26674c-5e1b-4170-b85a-3104a3a7bfdd)

## RESULT
Thus, the SQL queries to implement DML commands have been executed successfully.

