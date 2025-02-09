Week 16: How to properly structure a Query

<b>QUERY ORDER</b>
<p>When writing a query in SQL we should know that the placements of different components are very important, however here is a general layout of where different components should be:</p>

```sql
SELECT
FROM 
JOIN 
WHERE 
GROUP BY
HAVING
ORDER BY
LIMIT 
```
Here's an example:

```sql
SELECT 
    -- List columns of interest, and manipulate if necessary using arithmetic operators, CASE WHEN, etc.
    ,column_1
    ,column_2 * 2 AS doubled_column  -- Example of arithmetic manipulation
    ,CASE 
        WHEN column_3 > 10 THEN 'High'
        ELSE 'Low'
    END AS column_3_status   -- Example of CASE WHEN

FROM 
    -- List table, and database if necessary
    database_name.table_name

JOIN 
    -- This is where you would list joining tables
    another_table ON table_name.id = another_table.id  -- Example of an INNER JOIN

WHERE 
    -- Apply your conditions here
    column_1 = 'A' AND column_2 > 100  -- Example condition

GROUP BY 
    -- Group by necessary columns (often for aggregation)
    column_1

HAVING 
    -- Apply conditions to grouped results
    SUM(column_2) > 50  -- Example: Only include groups where sum of column_2 is greater than 50

ORDER BY 
    -- Sort the results (can be ascending or descending)
    column_1 ASC, column_2 DESC  -- Sorting first by column_1 ascending, then column_2 descending

LIMIT 
    -- Limit the number of rows if necessary
    10;  -- Limit the result to the first 10 rows

```

<b>QUERY FORMAT</b> 

When writing your query there is much left to personal preference, however there are some common best practices for writing easy to read/follow code. In all instances consistency is most important. For instance, if you prefer to use upper cases, or lower cases when writing out a query.
<ul>
  1. Upper or Lowercase 
  2. Leading Comma's or Trailing Comma's
  3. Indents
</ul>

<b> VARIABLE NAMING CONVENTIONS</b>
When considering namimg conventions in SQL we can make some choices, but there are a few things that should never be done when naming your variable. Generally, we want to avoid using a "-" since this something that SQL cannot handle.
1. SNAKECASE, CAMELCASE, PASCALCASE

d. Common Errors & Debugging

1. Syntax Errors
2. Logic Errors

e. Reference a Database
In the case that you are dealing with a large number of databases to pull data from, you may need to reference the specific database in which the table you're referencing originates. 

```sql
SELECT column_1
      ,column_2
      ,column_3
FROM database_a.table_a
