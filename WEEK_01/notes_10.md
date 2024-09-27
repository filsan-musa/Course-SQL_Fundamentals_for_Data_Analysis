<h2> Week 11:  Where & Having Statements </h2>

<b>WHERE:</b>
<p>This clause allows you to filter data based on specific conditions. You can use comparison operators like "=", "<", ">", etc., and logical operators like "AND" and "OR" to refine your filter, which will be further covered in the following week.</p>

```
SQL Syntax Example: Selects all values in column_1 where the entry corresponds exactly to specified string.
SELECT column_1
FROM table_a
WHERE column_1 = ‘string’;
```

Note: We put single quotations (or double quotations)  around the desired value because our value in the above example is a string, for numeric data types (ie. INT or FLOAT) we do not add these quotations. 

<b>HAVING:</b>
<p>This clause filters data for specific groups created with the GROUP BY clause. It allows you to apply additional conditions to the summarized data after grouping.
Here's a breakdown of how HAVING works:<

```sql
SQL Syntax Example:
SELECT *, SUM(column_1)
FROM table_a 
HAVING COUNT(*) < 10;
```

Grouping with GROUP BY: You can use the GROUP BY clause in your SELECT statement to create groups of data by grouping rows based on shared values in one or more columns.

Filtering with HAVING: After grouping, the HAVING clause filters groups meeting a condition with the aggregate function or grouping column. Only qualifying groups are included in the final results.


```sql
SQL Syntax Example:
SELECT column_1, COUNT(*) AS count
FROM table_a
GROUP BY column_1
HAVING COUNT(*) < 10;  - Filter column_1 with values less than 10
```

-This query groups count by colunmn_1 then uses the HAVING clause to filter out counts less than 10.
