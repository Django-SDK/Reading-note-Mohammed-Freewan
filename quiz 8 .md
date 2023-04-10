**1 : 1. What is postgreSQL?**
PostgreSQL is an advanced, enterprise class open source relational database that supports both SQL (relational) and JSON (non-relational) querying.

**2 : How can we use postgreSQL in shell or UI?**

in UI : 
sudo -u postgres psql

in SHELL :

psql -U

**3. How To create database, table and insert data in postgreSQL?**

CREATE TABLE employee (
    emp_id 	INT PRIMARY KEY,
    first_name VARCHAR(50) NOT NULL,
    last_name VARCHAR(50) NOT NULL,
    gender CHAR(1),
    birthdate DATE,
    email VARCHAR(100) UNIQUE,
    salary INT


**4:  How to order by in postgreSQL?**

When you query data from a table, the SELECT statement returns rows in an unspecified order. To sort the rows of the result set, you use the ORDER BY clause in the SELECT statement.

The ORDER BY clause allows you to sort rows returned by a SELECT clause in ascending or descending order based on a sort expression.

The following illustrates the syntax of the ORDER BY clause:

SELECT
	select_list
FROM
	table_name
ORDER BY
	sort_expression1 [ASC | DESC],
        ...
	sort_expressionN [ASC | DESC];
