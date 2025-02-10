<h1>Week 15: Introduction to Joins</h1>

SQL joins are powerful tools used to combine data from two or more tables based on a shared column. Here's a breakdown of the different join types and their applications:
<ul>
<li><b>Left Join (Left Outer Join):</b> A left join returns all rows from the left table (the table mentioned first in the query) and corresponding  rows from the right table (the table mentioned second) that meet a specific criteria or set of criteria. For the rows in the left table that do not meet the join criteria the entries will show NULL values. </li>
Application: Use a left  join when you want too see all data from the left table, even if there’s no corresponding data in the right table. 
             
```sql
-- SQL Syntax Example:
SELECT c.name, o.product
FROM customers c
LEFT JOIN orders o ON c.customerid = o.customerid 
```

<li><b>Right Join (Right Outer Join):</b> A right join works similarly to a left join,  but in reverse. It returns all rows from the right table (the table mentioned second in the query) and corresponding  rows from the right table (the table mentioned first) that meet a specific criteria or set of criteria. Unmatched rows from the left table will have NULL values in their corresponding entries . 
Application: Use a right join when you’re primarily interested in data from the right table and want to see if there’s any matching data in the left table. </li>

```sql
-- SQL Syntax Example:
SELECT p.name, c.name 
FROM  products p
RIGHT JOIN orders o ON p.productid= o.productid
RIGHT JOIN customers c ON o. customerid = c.customerid:
```

Note: Essentially, since left joins and right joins are interchangeable so long as you reverse the order of the referenced tables, when writing a query, it is often simpler and a best practice to stick to one of these join types. This will generally make your code logic easier to understand, and  can simplify debugging. In terms of conventions, left joins are more commonly used, this is partly because it is more intuitive, however whichever you choose stick to it.


<li><b>Inner Join (Join):</b> An inner join only returns rows where there’s a match in both tables based on the join condition.</li>

```sql
-- SQL Syntax Example:
SELECT a.column_1, b.column_2
FROM table_a AS a
INNER JOIN table_b AS b ON a.column_1 = b.column_1
```

Customers (CustomerID, Name) and Orders (OrderID, CustomerID, Product). An inner join on CustomerID will return only rows where a customer exists in the Customers table and has placed an order in the Orders table.

<li><b>Full Join (Full Outer Join):</b> An outer join returns all the rows from both tables. Rows that do not meet the join criteria in either of the tables will return NULL values. In simple terms, an outer join combines the results of a left join and a right join.</li>

```sql
--SQL Syntax Example:
SELECT c.Name, p.Name, o.Product
FROM Customers c
FULL JOIN Orders o ON c.CustomerID = o.CustomerID
FULL JOIN Products p ON o.ProductID = p.ProductID;
```

Imagine you want to see all customers and all products, along with information about their orders (if any). A full outer join on CustomerID and ProductID would achieve this.
