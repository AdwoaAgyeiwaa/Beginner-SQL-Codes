# Cleaning String Variables

### Removing Duplicates
```
SELECT
 DISTINCT table_column_name
FROM
 dataset.table_name;
 ```
Including `DISTINCT` in `SELECT` statement removes duplicates.

### Checking the Length of a Textstring in a Column
```
SELECT
 LENGTH(table_column_name)
FROM
 dataset.table_name;
```
The length command helps validate a textstring in a column to check for errors during entry.<br><br>
You can filter out the records that do not meet this validation using the following command:
```
SELECT
 table_column_name<br>
FROM
 dataset.table_name;<br>
WHERE
 LENGTH(table_column_name) doesn't meet condition;
```
You can then account for this error if you prefer not to update the table by using the substring command, "SUBSTr()"<br>
```
SELECT
 table_column_name
FROM
 dataset.table_name;
WHERE
 SUBSTR(table_column_name,number of letter to in textstring to start with,number of letters to pull out) = condition;
``` 
### Removing Spaces in a Textstring
```
SELECT
 table_column_name
FROM
 dataset.table_name
WHERE
 TRIM(table_column_name) = condition;
```
The "TRIM()" command helps to remove blank spaces before or after a textstring.

### Adding Strings Together
```
SELECT
 CONCAT(column_name1, column_name2)
FROM
 table
```
The "CONCAT()" command adds stings together to create new text strings that can be used as unique keys.

### Cleaning Misspelt Strings
```
SELECT
 CASE
  WHEN column_name = 'wrong_value' THEN 'correct_value'<br>
  ELSE column_name<br>
  END AS cleaned_name<br>
FROM
 table
```
The "CASE" statement goes through one or more conditions and returns a value as soon as a condition is met.


# Cleaning Integer Variables

### Checking Maximum and Minimum Values of a Column
```
SELECT
  MIN(column_name),
  MAX(column_name)
FROM
  table;
```

# Cleaning Datatype Errors

### Typecasting - Converting Data from One Type to Another
```
SELECT
 CAST(column_name AS datatype_name)
FROM
 table;
```
The "CAST()" command can be used to convert anything from one data type to another.

### Returning Non-Null Values in a List
```
SELECT
 COALESCE(1st_column_name_value_to_look_at, 2nd_column_name_value_to_return_if_1st_is_null)
FROM
 table;
```
The "COALESCE()"command can be used to return non-null values in a list.
