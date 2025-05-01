**Question 1**
--
Write SQL query to extract the email domain from each patient's email address and count the number of patients with the same email domain.

![Screenshot 2025-05-01 132340](https://github.com/user-attachments/assets/2d43dede-68aa-4655-a574-534480d7b78f)

**Query:**

```sql
select
substr(EMAIL,INSTR(EMAIL, '@')+1)AS EmailDomain,
count(*)as TotalPatients
from Patients
group by EmailDomain;

```

**Output:**

![Screenshot 2025-05-01 132351](https://github.com/user-attachments/assets/5f02c295-c348-4c5e-91a1-f24b68aab036)


**Question 2**
---
What is the average duration of insurance coverage for patients covered by each insurance company?

![Screenshot 2025-05-01 132402](https://github.com/user-attachments/assets/5c440626-4f05-40b3-80b1-d35a1b920bc3)

**Query:**

```sql
select InsuranceCompany,(AVG(DATE(EndDate)-Date(StartDate)))as AvgCoverageDurationDays
from Insurance
group by InsuranceCompany;

```

**Output:**


![Screenshot 2025-05-01 132416](https://github.com/user-attachments/assets/10175dcf-c822-4e1f-ae38-8abb26204233)


**Question 3**
---
How many medical records are there for each patient?

![Screenshot 2025-05-01 132428](https://github.com/user-attachments/assets/4e688e79-3e20-47c9-ad38-4b2f302b280e)

**Query:**

```sql
select PatientID,
COUNT (RecordID) AS TotalRecords
from MedicalRecords
group by PatientID;

```

**Output:**

![Screenshot 2025-05-01 132443](https://github.com/user-attachments/assets/cc5ed896-5bcd-43f7-bc86-668b97eab77c)

**Question 4**
---
Write a SQL query to find the difference between the maximum and minimum price of fruits?

![Screenshot 2025-05-01 132613](https://github.com/user-attachments/assets/6f20a198-a666-4794-ab6c-aa89f26efb69)

**Query:**

```sql
select MAX(price)-MIN(price)as price_diff
from fruits;

```

**Output:**

![Screenshot 2025-05-01 132621](https://github.com/user-attachments/assets/b6e66da4-9092-461b-86dd-bf847738a917)


**Question 5**
---
Write a SQL query to calculate total purchase amount of all orders. Return total purchase amount.

![Screenshot 2025-05-01 132631](https://github.com/user-attachments/assets/8ae70d3d-2ebf-4566-a19f-f98a7e0e8cf2)


**Query:**

```sql
select
TOTAL(purch_amt)as TOTAL FROM orders;

```

**Output:**

![Screenshot 2025-05-01 132639](https://github.com/user-attachments/assets/c5afe1d3-1d13-4423-8a97-1e534aad828d)

**Question 6**
---
Write a SQL query to find how many employees have an income greater than 50K?

![Screenshot 2025-05-01 132649](https://github.com/user-attachments/assets/2bf96f27-c87e-469a-b339-316b5ada23b8)

**Query:**

```sql
SELECT COUNT(*) AS
employees_count
FROM employee
where income>50000;

```

**Output:**

![Screenshot 2025-05-01 132656](https://github.com/user-attachments/assets/ab9d1291-6ee7-4eab-849f-60adc4045057)


**Question 7**
---
Write a SQL query to find the number of employees whose age is greater than 32.

![Screenshot 2025-05-01 132944](https://github.com/user-attachments/assets/a40257a6-99d9-4e31-9578-5a3ff7caed1e)

**Query:**

```sql
select COUNT(*)AS
COUNT
from employee
where age>32;

```

**Output:**

![Screenshot 2025-05-01 133224](https://github.com/user-attachments/assets/6d60e958-f600-4ece-ab91-4e8144b3043f)


**Question 8**
---
Write the SQL query that accomplishes the selection of number of products for each category from products table which includes only those products where the category ID is greater than 2.

![Screenshot 2025-05-01 133235](https://github.com/user-attachments/assets/e06082c9-343d-4402-8d62-3013087c5f70)


**Query:**

```sql
SELECT category_id,
COUNT(*)AS COUNT
from products
where category_id>2
group by category_id;

```

**Output:**

![Screenshot 2025-05-01 133316](https://github.com/user-attachments/assets/851adc01-19ad-4ec6-b872-2eac140f8aa2)


**Question 9**
---
Write the SQL query that accomplishes the selection of total cost of all products in each category from the "products" table and includes only those products where the total cost is greater than 50.

![Screenshot 2025-05-01 133416](https://github.com/user-attachments/assets/0eef0e16-f2c9-4ede-b30e-5d23addf94fa)


**Query:**

```sql
SELECT category_id,sum(price)as Total_Cost
from products
group by category_id
having sum(price)>50;

```

**Output:**

![Screenshot 2025-05-01 133425](https://github.com/user-attachments/assets/35f297b8-24e2-4c35-b8fd-5d8e57d8f1ca)


**Question 10**
---
Write the SQL query that achieves the grouping of data by age intervals using the expression (age/5)5, calculates the total salary sum for each group, and excludes groups where the total salary sum is not greater than 5000.

![Screenshot 2025-05-01 133438](https://github.com/user-attachments/assets/fb9ed622-d5f4-4c8b-89dd-ea203642727a)


**Query:**

```sql
SELECT (age/5)*5 as age_group,
SUM(salary)
from customer1
group by (age/5)*5
having SUM(salary)>5000;

```

**Output:**

![Screenshot 2025-05-01 133447](https://github.com/user-attachments/assets/f9158798-4e9d-4c56-808e-6b9c222d038b)


## Module 3 Home Challenge - Grade

![Screenshot 2025-05-01 140843](https://github.com/user-attachments/assets/bc97531c-85b8-4671-92a3-c1a8f24609a1)


## RESULT
Thus, the SQL queries to implement aggregate functions, GROUP BY, and HAVING clause have been executed successfully.



