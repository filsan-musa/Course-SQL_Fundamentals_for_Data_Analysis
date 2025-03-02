<h2>Week 12: Logical & Comparison Operators</h2>

<b>What are Logical Operators?</b>
<p>Logical operators are keywords that perform logical operations on boolean values (TRUE or FALSE) within your queries. They help refine your search criteria by combining conditions and filtering data based on specific requirements. Here is a breakdown of some most frequently used logical operators in SQL:</p>

<ul>
<li><b>AND:</b>
<p>This keyword combines multiple conditions in a query, and requires all conditions to be true for a row to be included in the results.</p></li>

```sql
-- SQL Syntax Example: This query retrieves data only for users who meet both of the specified conditions.
SELECT  *
FROM table_a
WHERE column_a > 18 AND column_b = 1;
```

<li><b>OR:</b>
<p>The keyword is used to filter data by specifying that at least one of multiple conditions must be satisfied for a row to be included in the result set.</p></li>

```sql
-- SQL Syntax Example: This query retrieves data from table_a meeting at least one of the specified conditions.
SELECT  *
FROM table_a
WHERE column_c =  ‘string’ OR column_b <= 12;
```

<li><b>BETWEEN:</b>
<p>This keywords filters data based on a range of specified column's values.</p></li>

```sql
-- SQL Syntax Example: This query retrieves data for orders between Jan 1st and Dec 31st, 2024 inclusive.
SELECT  *
FROM table_a
WHERE column_1 BETWEEN '2024-01-01' AND '2024-12-31';
```

<li><b>IN:</b>
<p>This clause filters data based on a list of values, allowing you to check if a specific column value matches any of the elements included in the list.</p></li>

```sql
//SQL Syntax Example: This query select all columns from table_a but only includes the rows where column_1 contains the value ‘Sales’ or ‘Marketing’
SELECT  *
FROM table_a
WHERE column_1 IN ('Sales', 'Marketing');
```
</ul>
<br></br>
<b>What are Comparison Operators?</b>
<p>Comparison Operators are essential in SQL as they help to filter or retrieve data based on specific criteria. These operators compare values in different conditions, and based on the comparison they return a Boolean value (TRUE or FALSE). The following are some of the most commonly used comparison operators in SQL:</p>

<ul>
<li><b>EQUALITY</b>
<p>Checks if two values are equivalent, and is denoted by the equality symbol (=).</p></li>

```sql
//SQL Syntax Example: This query is designed to retrieve all record in table_a where column_1 has a value other than 50.
SELECT  *
FROM table_a
WHERE column_1 = 50;
```


<li><b>INEQUALITY</B>
<p>Checks if two values are not the same, and is denoted by either (!= or <>).</p></li>

```sql
-- SQL Syntax Example: This query is designed to retrieve all record in table_a where column_1 has a value other than 50.
SELECT  *
FROM table_a
WHERE column_1 != 50;
```

<li><b>GREATER THAN:</b>
<p>Checks if one value is higher than another.</p></li>

```sql
-- SQL Syntax Example: This query is designed to retrieve all column_1  dates falling after March 15th, 2024.
SELECT  *
FROM table_a
WHERE column_1 > '2024-03-15';
```


<li><b>GREATER THAN OR EQUAL TO:</b>
<p>Checks if one value is either higher than or equal to another.</p></li>

```sql
-- SQL Syntax Example: This query is designed to retrieve all column_1  dates falling on or  after March 15th, 2024.
SELECT  *
FROM table_a
WHERE column_1>= '2024-03-15';
```


<li><b>LESS THAN (<):</b>
<p>Checks if one value is lower than another.</p></li>

```sql
-- SQL Syntax Example: This query retrieves data for column_1  with a score below 90.
SELECT *
FROM table_a
WHERE column_1< 90;
```

<li><b>IS NULL:</b>
<p>This statement checks whether the value in a particular column is NULL. If the value is NULL, it means that there is missing data in that column.</p></li>

```sql
-- SQL Syntax Example: This query selects all columns from ‘table_a’ but only includes the rows where ‘ column_1’ has no value (is NULL) 
SELECT *
FROM table_a
WHERE column_1 IS NULL;
```

<li><b>IS NOT NULL:</b>
<p>This is a comparison operator that checks for the presence of data in a column. It complements IS NULL and is used to ensure that a value is not missing.</p></li>

```sql
-- SQL Syntax Example: This query selects all columns from “ table_a” but only includes the rows where “column_1’ has a value and is not empty. 
SELECT *
FROM table_a
WHERE column_1 IS NOT NULL;
```

<li><b>LIKE:</b>
<p>This is a useful tool for searching for patterns within text data stored in columns. It enables you to search for specific patterns or partial matches, making it a flexible option for retrieving data that doesn't necessarily require an exact match.</p></li>

```sql
-- SQL Syntax Example: This query selects all columns from ‘table_a’ but only includes the rows where ‘column_1’ contains ‘en’ anywhere within the text. 
SELECT *
FROM table_a
WHERE column_1 LIKE '%en%';
```


<li><b>NOT LIKE:</b>
<p>It allows you to search for text data in a column and exclude rows where the text matches a specific pattern using wildcards.</p></li>

```sql
-- SQL Syntax Example: This query selects all columns from ‘table_1’ but only includes the rows where ‘column_1’ does not contain ‘king’ anywhere within the text. 
SELECT *
FROM table_1
WHERE column_1 NOT LIKE '%king%';
```
</ul>
