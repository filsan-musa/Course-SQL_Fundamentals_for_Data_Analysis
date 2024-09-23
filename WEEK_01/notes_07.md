<h2> Week 7: Constructing a Select Statement:</h2>

In this segment we'll be learning the most basic components of a select query. You will learn how to access a table within your database and pull information. 

<b>FUNDAMENTAL COMPONENTS OF A SELECT QUERY:</b>
<ul><li>SELECT: This statement is fundamental for retrieving columns, or manipulated data pulled from tables specified in the FROM clause.</li>
<li>FROM: This clause identifies the table(s) from which you want to retrieve data. It's essential to tell SQL where to look for information. In some instances, you may also need to reference the database in which the table is situated.</li></ul>

<b>BASIC SAMPLE QUERIES:</b>

Here's what you can do with the SELECT clause:

<ul>
<li>Single Column:
    <p>Selecting one column to retrieve data from that column only. </li>

```sql
# SQL Syntax Example: This retrieves only the values from column1 from table_a
SELECT column_1
FROM table_a;
```


<li> Multiple Columns: 
     <p>List the column names you want to retrieve, separated by commas. The names should match the actual columns in your table. </li>

```sql
# SQL Syntax Example: This query retrieves data from three columns, column1, column2, and column3 from table_a
SELECT column_1, column_2, column_3
FROM table_a;
```

<li>All Columns: 
    <p>Use the asterisk (*) symbol to grab all columns from a table.</p></li>

```sql
# SQL Syntax Example: This retrieves all columns from table_a
SELECT *
FROM table_a;
```
</ul>
<br>

<b>DISTINCT:</b>

This keyword extracts all the unique values in a particular column, effectively eliminating duplicate entries from the result set.

```
# SQL Syntax Example: This retrieves only unique values present in the "column_1" column of the "table_a" table.
SELECT DISTINCT column_1
FROM table_a;
```
<br>

<b>ALIASES:</b>

These are temporary names, which can be assigned to both columns and tables within a particular query. The aliases used do not alter the original names of columns and tables as stored in the database, but rather provide a more convenient and/or accurate way to reference them when writing a query. In short, there are temporary nicknames chosen by the writer of the query, but are best to keep intuitive. Aliases are particularly useful when writing long and complex queries.

```sql
# SQL Syntax Example: The "AS" is a keyword, which preceeds the alias, is used as an identifier of the alias.
SELECT column_1 AS alias_name
FROM table_a AS alias_name;
```

It is worth mentioning that the use of the “AS” keyword is optional, and alias can directly follow the old column or table name without the use of “AS”.

```sql
# SQL Syntax Example: Does not use the "AS" keyword which generally preceeds the alias.
SELECT column_1 alias_name
FROM database_a.table_a alias_name;	
```

