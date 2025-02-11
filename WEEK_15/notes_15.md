<h1>Week 15: Introduction to Joins</h1>

SQL joins are powerful tools used to combine data from two or more tables based on a shared column. Here's a breakdown of the different join types and their applications:
<ul>
<li><b>Left Join (Left Outer Join):</b> A left join returns all rows from the left table (the table mentioned first in the query) and corresponding  rows from the right table (the table mentioned second) that meet a specific criteria or set of criteria. For the rows in the left table that do not meet the join criteria the entries will show NULL values. </li>
             
```sql
-- SQL Syntax Example:
SELECT a.column_1, b.column_2
FROM table_a AS a
LEFT JOIN table_b AS b ON a.column_1 = b.column_1
```

<li><b>Right Join (Right Outer Join):</b> A right join works similarly to a left join,  but in reverse. It returns all rows from the right table (the table mentioned second in the query) and corresponding  rows from the right table (the table mentioned first) that meet a specific criteria or set of criteria. Unmatched rows from the left table will have NULL values in their corresponding entries.</li>

```sql
-- SQL Syntax Example:
SELECT a.column_1, b.column_2
FROM table_a AS a
RIGHT JOIN table_b AS b ON a.column_1 = b.column_1
```

Note: Essentially, since left joins and right joins are interchangeable so long as you reverse the order of the referenced tables, when writing a query, it is often simpler and a best practice to stick to one of these join types. This will generally make your code logic easier to understand, and  can simplify debugging. In terms of conventions, left joins are more commonly used, this is partly because it is more intuitive, however whichever you choose stick to it.


<li><b>Inner Join (Join):</b> An inner join only returns rows where there’s a match in both tables based on the join condition.</li>

```sql
-- SQL Syntax Example:
SELECT a.column_1, b.column_2
FROM table_a AS a
INNER JOIN table_b AS b ON a.column_1 = b.column_1
```

<li><b>Full Join (Full Outer Join):</b> An outer join returns all the rows from both tables. Rows that do not meet the join criteria in either of the tables will return NULL values. In simple terms, an outer join combines the results of a left join and a right join.</li>

```sql
--SQL Syntax Example:
SELECT a.column_1, b.column_2, c.column_3
FROM table_a AS a
FULL JOIN table_b AS b ON a.column_1 = b.column_2
FULL JOIN table_c AS c ON a.column_1 = c.column_3
```

![image](https://github.com/user-attachments/assets/43670ded-3381-48cb-b71f-216b86a0d8c9)

