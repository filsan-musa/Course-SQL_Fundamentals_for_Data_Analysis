<h2>Week 8: Basic Aggregations</h2>

COUNT: This function calculates the number of rows that meets the specified conditions outlined within a query.

```
SQL Syntax Example:
SELECT COUNT(*) 
FROM table_a;
```

This  count the number of rows in a table called table_a

SUM: This function calculates the sum of all values within a numeric column. This is useful for finding quantities like total sales, overall expenses, or any other measurable sum.

SQL Syntax Example:
SELECT SUM(column_1) 
FROM table_a;

Calculate the sum of the values in a column called column_1 in a table named table_a
     
AVG: This function calculates the average (mean) of all values within a numeric column.

SQL Syntax Example
SELECT AVG(column_1) 
FROM table_a;

 The AVG() function to calculate the average value of the values in a column called column_1 in a table named table_a

MAX: This function identifies the highest (maximum) value within a numeric column.
SQL Syntax Example:
SELECT MAX(column_1) 
FROM table_a;

The MAX() function to find the maximum value in a column called column_1 in a table named table_a. 

MIN: This function identifies the lowest (minimum) value within a numeric column. 

SQL Syntax Example:
SELECT MIN(column_1) 
FROM table_a;

The MIN() function to find the minimum value in a column called column_1 in a table named table_a. 

Aggregate functions typically ignore NULL values when performing calculations, unless you're using COUNT(*) which counts all rows including those with NULLs. If you wish to include NULLS in your calculations, which can be useful in the case of calculating an average for instance, you can convert all NULL values to 0s. This can be done through a CASE WHEN statement, or some alternative methods which may not be taught in this course.
