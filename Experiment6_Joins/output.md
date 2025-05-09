**Question 1**
--
Write the SQL query that achieves the selection of all columns from the "nurses" table (aliased as "n") and the "department_name" column from the "departments" table, with an inner join on the "department_id" column.

```sql

SELECT nurses.*, departments.department_name
FROM nurses
INNER JOIN departments
ON nurses.department_id = departments.department_id;

```

**Output:**

![Output1](output.png)

**Question 2**
---
Write the SQL query that achieves the selection of the "name" column from the "salesman" table (aliased as "s"), the "cust_name," "city," "grade," and "salesman_id" columns from the "customer" table (aliased as "c"), with a left join on the "salesman_id" column and a condition filtering for customers with a grade less than or equal to 100.

```sql
SELECT 
    s.name, 
    c.cust_name, 
    c.city, 
    c.grade, 
    c.salesman_id
FROM 
    salesman s
LEFT JOIN 
    customer c 
ON 
    s.salesman_id = c.salesman_id
WHERE 
    c.grade <= 100;

```

**Output:**

![Output2](output.png)

**Question 3**
---
From the following tables write a SQL query to find those customers with a grade less than 300. Return cust_name, customer city, grade, Salesman, salesmancity. The result should be ordered by ascending customer_id. 

```sql
SELECT 
    c.cust_name, 
    c.city, 
    c.grade, 
    s.name AS Salesman, 
    s.city AS city
FROM 
    customer c
JOIN 
    salesman s 
ON 
    c.salesman_id = s.salesman_id
WHERE 
    c.grade < 300
ORDER BY 
    c.customer_id ASC;

```

**Output:**

![Output3](output.png)

**Question 4**
---
Write the SQL query that achieves the selection of all columns from the "customer" table (aliased as "c"), with a left join on the "customer_id" column and a condition filtering for orders with an order date between '2012-07-01' and '2012-07-30'.

```sql
SELECT 
    c.*
FROM 
    customer c
LEFT JOIN 
    orders o 
ON 
    c.customer_id = o.customer_id
WHERE 
    o.ord_date BETWEEN '2012-07-01' AND '2012-07-30';

```

**Output:**

![Output4](output.png)

**Question 5**
---
Write the SQL query that achieves the selection of all columns from the "test_results" table (aliased as "t"), with an inner join on the "patient_id" column and a condition filtering for patients with the first name 'Alice'.

```sql

SELECT 
    t.*
FROM 
    test_results t
INNER JOIN 
    patients p 
ON 
    t.patient_id = p.patient_id
WHERE 
    p.first_name = 'Alice';

```

**Output:**

![Output5](output.png)

**Question 6**
---
From the following tables write a SQL query to locate those salespeople who do not live in the same city where their customers live and have received a commission of more than 12% from the company. Return Customer Name, customer city, Salesman, salesman city, commission.  

```sql

SELECT 
    c.cust_name AS "Customer Name", 
    c.city AS "city", 
    s.name AS "Salesman", 
    s.city AS "city", 
    s.commission
FROM 
    customer c
JOIN 
    salesman s 
ON 
    c.salesman_id = s.salesman_id
WHERE 
    c.city <> s.city
    AND s.commission > 0.12;


```

**Output:**

![Output6](output.png)

**Question 7**
---
Write a SQL statement to join the tables salesman, customer and orders so that the same column of each table appears once and only the relational rows are returned. 

```sql
SELECT 
    o.ord_no, 
    o.purch_amt, 
    o.ord_date, 
    c.cust_name, 
    c.city AS customer_city, 
    c.grade, 
    s.name AS salesman_name, 
    s.city AS salesman_city, 
    s.commission
FROM 
    orders o
JOIN 
    customer c ON o.customer_id = c.customer_id
JOIN 
    salesman s ON o.salesman_id = s.salesman_id;

```

**Output:**

![Output7](output.png)

**Question 8**
---
Write the SQL query that achieves the selection of all columns from the "patients" table and the specialization from the "doctors" table (aliased as "doctor_specialization"), with an inner join on the "doctor_id" column.

```sql

SELECT 
    p.patient_id, 
    p.first_name, 
    p.last_name, 
    p.date_of_birth, 
    p.admission_date, 
    p.discharge_date, 
    p.doctor_id, 
    d.specialization AS doctor_specialization
FROM 
    patients p
INNER JOIN 
    doctors d 
ON 
    p.doctor_id = d.doctor_id;

```

**Output:**

![Output8](output.png)

**Question 9**
---
 From the following tables write a SQL query to find the salesperson(s) and the customer(s) he represents. Return Customer Name, city, Salesman, commission.

```sql

SELECT 
    c.cust_name AS "Customer Name", 
    c.city AS "city", 
    s.name AS "Salesman", 
    s.commission
FROM 
    customer c
JOIN 
    salesman s 
ON 
    c.salesman_id = s.salesman_id;

```

**Output:**

![Output9](output.png)

**Question 10**
---
From the following tables write a SQL query to find those orders where the order amount exists between 500 and 2000. Return ord_no, purch_amt, cust_name, city.

```sql

SELECT 
    o.ord_no, 
    o.purch_amt, 
    c.cust_name, 
    c.city
FROM 
    orders o
JOIN 
    customer c 
ON 
    o.customer_id = c.customer_id
WHERE 
    o.purch_amt BETWEEN 500 AND 2000;

```

**Output:**

![Output10](output.png)
