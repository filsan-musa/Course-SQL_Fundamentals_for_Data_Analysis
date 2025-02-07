<h2>Week 10: Limit, Order By, Group By </h2>

<b>LIMIT: </b>
<p>The limit clause allows you to specify the maximum number of rows to be returned by a SELECT statement. It's almost always placed at the end of the query. </p>

```sql
# SQL Syntax Example: This query pulls 10 records from table_a
SELECT *
FROM table_a
LIMIT 10;
```           


<b>ORDER BY:</b>
<p>This clause sorts the retrieved data based on the specified column(s). You can specify ascending (ASC) or descending (DESC) order. If you do not specify, SQL will default to using ASC, this means that if you intend to sort by the ascending order adding ASC to your clause is optional.</p> 

```sql
# SQL Syntax Example:
SELECT column_1, column_2
FROM table_a
ORDER BY column_1 ASC, age DESC;
```

Alternatively, You can use ordinal numeric representation to denote column. This can be used for both ORDER BY and GROUP BY. 

```sql
SELECT column_1, column_2
FROM table_a
ORDER BY 1 ASC, 2 DESC;
```

<b>GROUP BY:</b>
<p>This clause categorizes rows in a SELECT statement based on shared values in one or more columns. This grouping is often used with aggregate functions like COUNT, SUM, or AVG to calculate summary statistics for each group.</p>

```sql
#SQL Syntax Example:
SELECT column_1, SUM(column_2)
FROM table_a
GROUP BY column_1
```
