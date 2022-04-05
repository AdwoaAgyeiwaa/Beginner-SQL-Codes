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
 column_name
FROM 
 table
```
