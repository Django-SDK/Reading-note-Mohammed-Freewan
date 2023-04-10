**1 : 1. How can we cretae table in sql database?**

You can create a new table by specifying the table name,
along with all column names and their types:
Use this command to create Table :
CREATE TABLE tablename(
Colname datatype,
)

**2: 2. How can we insert data in sql database?**

The INSERT statement is used to populate a table with rows:
INSERT INTO weather VALUES ('San Francisco', 46, 50, 0.25, '1994-11-27');

**3: 3. How can we update data in sql database?**

You can update existing rows using the UPDATE command.
Suppose you discover the temperature readings are all off by 2 degrees after November 28.
You can correct the data as follows:
UPDATE weather
SET temp_hi = temp_hi - 2, temp_lo = temp_lo - 2
WHERE date > '1994-11-28’;

**4: 4. How can we delete data in sql database?**

Rows can be removed from a table using the DELETE command.
Suppose you are no longer interested in the weather of Hayward.
Then you can do the following to delete those rows from the table
:
DELETE FROM weather WHERE city = 'Hayward’;

**5: 5. How can we select data in sql database?**

The SELECT statement is used to select data from a database.

SELECT Syntax
SELECT column1, column2, ...
FROM table_name;

**6: 6. How can we order by in sql database?**

You can request that the results of a query be returned in sorted order:
SELECT * FROM weather
ORDER BY city;


