#### Creating a table
CREATE TABLE table_name(characteristics of table);<br>
Creates a table with the characteristics of that table.<br>
Characteristics include the following format: column_name datatype(length of datatype)<br>
Each characteristic should be separated by a comma(,) from the next.

#### Viewing the characteristics of a table
DESCRIBE table_name;<br>
Describes everything about a table for you showing all its characteristics.

#### Deleting a table
DROP TABLE table_name;<br>
Deletes a table and all of its contents.

#### Modifying a table
ALTER TABLE table_name ADD column_name datatype(length of datatype);<br>
Modifies a table by adding a new column to the already existing table.<br><br>
ALTER TABLE table_name DROP column_name;<br>
Modifies a table by deleting a column from a table.

#### Inserting values into a table
INSERT INTO table_name VALUES();<br>
Inserts the values of columns or fields into the table.<br>
Note that when inserting values, they should be in the order of how their columns appear in the table and separated by a comma(,).<br><br>
INSERT INTO table_name(column_name) VALUES();<br>
Inserts the values of specific fields into the table.
