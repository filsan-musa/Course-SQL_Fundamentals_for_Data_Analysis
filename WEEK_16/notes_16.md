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

<p><b> VARIABLE NAMING CONVENTIONS</b></p>
<p>When considering naming conventions in SQL, it's important to adopt practices that promote readability, consistency, and maintainability of your code. While you have some flexibility in how you name your variables, there are certain rules to follow. Some practices should be avoided entirely to avoid potential issues.</p>

<ul>
<p>1. <b>Avoid Using Special Characters:</b></p>
<ol><p> Avoid using hyphens (`-`), spaces or other special character (ie. @, $, * etc.) in variable names, as these can cause syntax errors or other issues in SQL queries. SQL doesn't handle hyphens well because it interprets them as subtraction operators. As a general rule of thumb, refrain from ever using hyphens for naming variable since they can't be handled by most programming languages (ie. Python, C++, and Java to name a few).</p></ol>

<p> In other words, <b><u>DO NOT</u></b> use naming convention methods such as the Kebab Case (<code>kebab-case</code>) or Train Case (<code>Train-Case</code>).</p>

<p>2. <b>Common Naming Conventions:</b></p>
<ul>
<p>
  <li><b>Snake Case (<code>snake_case</code>):</b> This convention uses underscores to separate words. It is often used in SQL to name columns, tables, and variables.</li>
  <o><i>Example: `order_total_amount`, `customer_id`.</i></o>
  <li><b>Camel Case (<code>camelCase</code>):</b> In this style, the first letter of the first word is lowercase, and the first letter of subsequent words is uppercase. This is often used in programming languages like JavaScript, but less common in SQL.</li>
<o><i>Example: `orderTotalAmount`, `customerId`.</i></o>
  <li><b>Pascal Case (<code>PascalCase</code>):</b> Similar to CamelCase but with the first letter of the first word capitalized. Pascal case is more common in object-oriented programming but not widely used in SQL</li> 
<o><i>Example: `OrderTotalAmount`, `CustomerId`.</i></o>
</p>
</ul>



<p>3. <b>Best Practices:</b></p>
<ul>
  <li><b>Consistency:</b> Choose one naming convention and stick to it throughout your database schema and queries. Consistency will help keep your codebase organized and easy to read</li>
  <li><b>Clarity:</b> Use descriptive names for your variables that clearly indicate the nature of the information stored in said variable. Avoid abbreviations unless they are widely recognized (e.g., `uid` for unique identifier, or 'ip' for internet protocol address).</li>
  <li><b>Brief:</b> While being descriptive when naming your variable is desireable, avoid excessively long or overly descriptive variable names. Aim for brevity without sacrificing clarity.</li>
  <li><b>Avoid Reserved Keywords:</b> Never use SQL reserved keywords like <code>SELECT</code>, <code>WHERE</code>, or <code>TABLE</code> as variable names. This can lead to errors or ambiguity in your queries.</li>
  <li><b>Use Singular Names for Tables:</b> Use singular names for table names (e.g., `customer` instead of `customers`). It is a commonly accepted convention to treat tables as individual entities.</li>
  <li><b>Use Plural Names for Collections:</b> While singular for tables is a common convention, use plural names when referencing collections of entities, like `orders` or `products`.</li>
</ul>
</ul>

<p><b>COMMON ERRORS & DEBUGGING</b></p>
<p>Errors are often some of the most annoying and common issues to occur when writing code. </p>
<ul>
Visible Errors:
1. Syntax Errors
2. Logic 
</ul>
<ul>
To debug code, you first must read and interpret the error message. If the message is not giving a specific error, it often includes the first effected line. This mean when resolving errors in SQL the first error encoured will be the only one listed
</ul>

<p><b>REFERENCE A DATABASE</b></p>
<p>In the cases where you are encounter a large number of databases to pull data from, you may need to specify the database that contains the table you want to query. This is also helpful to avoid pulling from similarly named tables which may exist in another database.</p>

```sql
SELECT column_1
      ,column_2
      ,column_3
FROM database_a.table_a
```
<p>Note: <code>database_a.table_a</code>: This syntax allows you to specify that you're querying the <code>table_a</code> table from <code>database_a</code>, ensuring the correct database context is used when executing the query.</p>
