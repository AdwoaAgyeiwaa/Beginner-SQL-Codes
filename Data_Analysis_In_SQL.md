# Sorting Data
## Sorting data using the `ORDER BY` command
The following syntax can be used to sort data in descending or ascending order:
```
SELECT
 column_name
FROM 
 table
ORDER BY
 column_name DESC or ASC;
 ```
## Sorting after Filtering Data using the `WHERE` and `ORDER BY` commands
```
SELECT
 column_name
FROM 
 table
WHERE
 column_name = "condition"
ORDER BY
 column_name DESC or ASC;
 ```
# Filtering Data
## Filtering out a column of data
```
SELECT
 column_name
FROM 
 table
WHERE
 column_name = "condition";
```
## Filtering out multiple columns of data
```
SELECT
 column_name
FROM 
 table
WHERE
 column_name1 = "condition"
AND
 column_name2 = "condition";
```
## Filtering out a range of data within a column
We can use the `BETWEEN` and `AND` commands to filter out ranges of values:
```
SELECT
 column_name
FROM 
 table
WHERE
 column_name1 BETWEEN 'condition1' AND 'condition2';
```
# Combining Multiple TextStrings
We can use `CONCAT` to pull and concatenate data from different columns:
```
SELECT
 CONCAT(column_name1,column_name2) AS column_name3
FROM 
 table
```
# Aggregating Data
## Combining rows from two or more columns using `JOIN`
We can use the JOIN clause to aggregate data. JOIN is used to combine rows from two or more tables based on a common or related column. You can think of a JOIN as the SQL version of VLOOKUP in spreadsheets. There are 4 common JOINs used in data aggregation:
### `INNER JOIN`
An INNER JOIN is a function that returns records with matching values from both tables. To appear in the results table, the records must be key values in each other's tables. When we write INNER JOIN into SQL, the default value is usually JOIN. As a result, JOIN can be used as a shortcut.
```
SELECT
  table1.column_name1 AS new_column_name1,
  table2.column_name2 AS new_column_name2
FROM
  dataset.table1
INNER JOIN
  dataset.table2
ON
  table1.matching_column_name = table2.matching_column_name;
```
### `LEFT JOIN`
A LEFT JOIN function returns all records from the left table and only the matched records from the right table. The table mentioned first is left and the table mentioned second is right. We can also think of left as a table name to the left of the JOIN statement and right as a table name to the right of the JOIN statement. Each row in the left table appears in the results even if there are no matches in the right table.
```
SELECT
  table1.column_name1 AS new_column_name1,
  table2.column_name2 AS new_column_name2
FROM
  dataset.table1
LEFT JOIN
  dataset.table2
ON
  table1.matching_column_name = table2.matching_column_name;
```
### `RIGHT JOIN`
A RIGHT JOIN function returns all records from the right table and only the matched records from the left table. The table mentioned first is right and the table mentioned second is left. We can also think of right as a table name to the right of the JOIN statement and left as a table name to the left of the JOIN statement. RIGHT JOIN is the exact opposite of LEFT JOIN. You can get the same results if you flip the order of the tables and use a LEFT JOIN.
```
SELECT
  table1.column_name1 AS new_column_name1,
  table2.column_name2 AS new_column_name2
FROM
  dataset.table1
RIGHT JOIN
  dataset.table2
ON
  table1.matching_column_name = table2.matching_column_name;
```
### `FULL OUTER JOIN`
The FULL OUTER JOIN combines the RIGHT and LEFT JOINS to return all matching records from both tables. This indicates that it will return all of the records from both tables. If there are records in one table without a match, it'll create a record with null values for the other table. This is sometimes referred to as just `FULL JOIN`
```
SELECT
  table1.column_name1 AS new_column_name1,
  table2.column_name2 AS new_column_name2
FROM
  dataset.table1
FULL OUTER JOIN
  dataset.table2
ON
  table1.matching_column_name = table2.matching_column_name;
```
## Counting Data
### Counting all non-null values using `COUNT`
The `COUNT` aggregate function is used to determine the number of rows in the output. It returns the number of rows that matches a specified criterion in the WHERE clause including duplicate data. It eliminates the NULL values in the output but does not eliminate duplicates of data.
```
SELECT
  COUNT(column_name) AS alias_name
FROM
  table_name
WHERE
  condition;
```
### Counting only unique values using `COUNT(DISTINCT)`
`COUNT(DISTINCT)` returns the distinct number of rows after satisfying conditions specified in the WHERE clause. It gives a distinct number of rows after eliminating NULL and duplicate values. It eliminates the NULL and duplicate values in the output.
```
SELECT
  COUNT(DISTINCT column_name) AS alias_name
FROM
  table_name
WHERE
  condition;
```
### Counting all number of rows using `COUNT(*)`
The `COUNT(*)` command returns the total number of rows after satisfying conditions specified in the where clause. It considers all rows regardless of any duplicate, NULL values. It does not eliminate the NULL values in the output.
```
SELECT
  COUNT(*)
FROM
  table_name
WHERE
  condition;
```
## Aggregating data using subqueries

# Data Calculations
## Queries and calculations
SELECT
  column_name1,
  column_name2,
  (column_name1 + column_name2) * column_name3 AS column_name4
## Aggregate functions
SUM
AVG
## Grouping Data
We use the `GROUP BY` command to group rows that have the same values into summary rows, such as "find the number of customers in each country".<br>
The GROUP BY statement is often used with aggregate functions (COUNT(), MAX(), MIN(), SUM(), AVG()) to group the result-set by one or more columns.<br>
The GROUP BY clause is used in collaboration with the SELECT statement to arrange identical data into groups. This GROUP BY clause follows the WHERE clause in a SELECT statement and precedes the ORDER BY clause.
```
SELECT 
  column_name(s)
FROM 
  table_name
WHERE
  condition
GROUP BY
  column_name(s)
ORDER BY
  column_name(s);
```
`EXTRACT` command
# Temporary Tables
`WITH` command
`SELECT INTO` command
`CREATE TABLE` command 
