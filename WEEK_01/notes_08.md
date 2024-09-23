<h2>Week 8: Basic Aggregation Functions</h2>

Aggregation functions are often viewed as one of the primary tools for data manipulation (ie. transforming and summarizing data). In this section, we'll explore some of the most common aggregation functions: COUNT, SUM, AVG, MAX, and MIN. These functions enable you to calculate values within a specified column or set of columns, and can only be applied to columns with numeric data types.

<ul>
<li><b>COUNT:</b> This function calculates the number of rows that meets the specified conditions outlined within a query.

```sql
# SQL Syntax Example: This counts the number of rows in table_a
SELECT COUNT(*) 
FROM table_a;
```

<li>SUM: This function calculates the sum of all values within a numeric column. This is useful for finding quantities like total sales, overall expenses, or any other measurable sum.</li>

```sql
# SQL Syntax Example: Calculates the sum of the values in column_1 in table_a
SELECT SUM(column_1) 
FROM table_a;
```
     
<li>AVG: This function calculates the average (mean) of all values within a numeric column.</li>

```sql 
# SQL Syntax Example: Calculate the mean value in column_1 in table_a
SELECT AVG(column_1) 
FROM table_a;
```

<li>MAX: This function identifies the highest value within a numeric column.</li>

```sql
# SQL Syntax Example: Finds the maximum (highest) value in column_1 in table_a
SELECT MAX(column_1) 
FROM table_a;
```

<li>MIN: This function identifies the lowest value within a numeric column.</li>

```sql
# SQL Syntax Example: Finds the minimum (lower) value in column_1 in table_a
SELECT MIN(column_1) 
FROM table_a;
```
</ul>

NOTE: Aggregate functions typically ignore NULL values when performing calculations, unless you're using COUNT(*) which counts all rows including those with NULLs. If you wish to include NULLS in your calculations, which can be useful in the case of calculating an average for instance, you can convert all NULL values to 0s. This can be done through a CASE WHEN statement, or some alternative methods which may not be taught in this course.
