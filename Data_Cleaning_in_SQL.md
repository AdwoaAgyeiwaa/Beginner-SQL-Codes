#### Cleaning String Variables

##### Removing Duplicates
SELECT<br>
 DISTINCT table_column_name<br>
FROM<br>
 dataset.table_name;<br>
Including DISTINCT in SELECT statement removes duplicates.

##### Checking the Length of a Textstring in a Column
SELECT<br>
 LENGTH(table_column_name)<br>
FROM<br>
 dataset.table_name;<br>
The length command helps validate a textstring in a column to check for errors during entry.<br><br>
You can filter out the records that do not meet this validation using the following command:<br>
SELECT<br>
 table_column_name<br>
FROM<br>
 dataset.table_name;<br>
WHERE<br>
 LENGTH(table_column_name) doesn't meet condition;<br><br>
You can then account for this error if you prefer not to update the table by using the substring command, "SUBSTr()"<br>
SELECT<br>
 table_column_name<br>
FROM<br>
 dataset.table_name;<br>
WHERE<br>
 SUBSTR(table_column_name,number of letter to in textstring to start with,number of letters to pull out) = condition;
 
##### Removing Spaces in a Textstring
SELECT<br>
 table_column_name<br>
FROM<br>
 dataset.table_name;<br>
WHERE<br>
 TRIM(table_column_name) = condition;
The "TRIM()" command helps to remove blank spaces before or after a textstring.

##### Adding Strings Together
SELECT<br>
 CONCAT(column_name1, column_name2)<br>
FROM<br>
 table<br>
The "CONCAT()" command adds stings together to create new text strings that can be used as unique keys.

##### Cleaning Misspelt Strings
SELECT<br>
 CASE<br>
  WHEN column_name = 'wrong_value' THEN 'correct_value'<br>
  ELSE column_name<br>
  END AS cleaned_name<br>
FROM<br>
 table<br>
The "CASE" statement goes through one or more conditions and returns a value as soon as a condition is met.


#### Cleaning Integer Variables

##### Checking Maximum and Minimum Values of a Column
SELECT<br>
  MIN(column_name),<br>
  MAX(column_name)<br>
FROM<br>
  table;<br>


#### Cleaning Datatype Errors

#### Typecasting - Converting Data from One Type to Another
SELECT<br>
 CAST(column_name AS datatype_name)<br>
FROM<br>
 table;<br>
The "CAST()" command can be used to convert anything from one data type to another.


#### Returning Non-Null Values in a List
SELECT<br>
 COALESCE(1st_column_name_value_to_look_at, 2nd_column_name_value_to_return_if_1st_is_null)<br>
FROM<br>
 table;<br>
The "COALESCE()"command can be used to return non-null values in a list.
