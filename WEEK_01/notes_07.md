<h2> Week 7: Constructing a Select Statement:</h2>

SELECT: This is the fundamental clause for retrieving columns, or manipulated data pulled from tables specified in the "FROM" clause (see FROM) data from tables. 

FROM: This clause identifies the table(s) from which you want to retrieve data. It's essential to tell SQL where to look for the information. In many instances, you will also need to reference the database in which the table is situated.

 Here's what you can do with the SELECT clause:

Select All: Use the asterisk (*) symbol to grab all columns from a table.

SQL Syntax Example:
SELECT *
FROM table_a;

This retrieves all columns from the table

Single Column: Mention the specific column name to retrieve data from that column only.

SQL Syntax Example:
SELECT column_1
FROM table_a;

This retrieves only the values from the "column1" column within the "table_name" table.

Multiple Columns: List the column names you want to retrieve, separated by commas. The names should match the actual columns in your table.

SQL Syntax Example:
SELECT column_1, column_2, column_3
FROM table_a;

This query retrieves data from three specific column1, column2, and column3 in a table named table_name.

DISTINCT: This keyword extracts all the unique values in a particular column, effectively eliminating duplicate entries from the result set.

SQL Syntax Example:
SELECT DISTINCT column_1
FROM table_a;

This retrieves only unique values present in the "column_1" column of the "table_a" table.


ALIASES: These are temporary names, which can be assigned to both columns and tables within a particular query. The assigned aliases used do not alter the original names stored in the database, but rather provide a more convenient and/or accurate way to reference them when writing a query. They are particularly useful when writing more complex queries.

SQL Syntax Example:
SELECT column_1 AS alias_name
FROM table_a AS alias_name;

column1: This refers to the actual name of the column in your table.
AS:  "AS" is a keyword used to introduce the alias.
DISCLAIMER: The “AS” is optional, and alias name can directly follow the old column or table name without the use of “AS”
SELECT column_1 alias_name
FROM database_a.table_a alias_name;	
alias_name: This is the temporary nickname you choose for the column. It can be anything descriptive or shorter than the original name.

