<h2>Week 5: Understand SQL commands and components</h2>

<b>SQL Commands:</b>
<p>An SQL command, is essentially the action you're trying to take (e.g., SELECT, INSERT), and is typically found at the start of a query or statement. There are five categories or classes of SQL Command: DDL (Data Definition Language), DML (Data Manipulation Language), DQL (Data Query Language), DCL (Data Control Language), and TCL (Transaction Control Language). 
</p>
<ul><li>Example: DML (ie. INSERT, UPDATE, DELETE), DQL (ie. SELECT), etc.</li></ul>

![Screenshot 2025-05-20 at 8 31 05 PM](https://github.com/user-attachments/assets/43639ac5-8b4b-40eb-85de-9059724566cb)

<b>SQL Statements & Queries:</b>
<p>An SQL statement is a complete instruction in SQL that performs an action. A query is a specific type of SQL statement that uses a Data Query Language (DQL) command, most commonly SELECT, and is used to retrieve data—usually producing an output. Recall, all queries are statements but not all statements are queries.</p> 

<ul><li>Example: Selecting all the inputs in <code>table_a</code>.</li></ul>
  
```sql
SELECT *
FROM table_a
```

```sql
UPDATE table_a
SET column_1 = 'value_b'
WHERE column_1 = 'value_a';
```


<b>SQL Functions:</b>
<p>SQL functions are built-in or user-defined routines that accept parameters, perform actions, and return a value. They can be used within SQL statements to perform calculations, and extract information.</p>
<ul><li>Example: aggregate functions (ie. SUM, AVG, COUNT, MAX, MIN), numeric transformations(ie. ROUND, FLOOR), and conversion functions (ie. CAST, CONVERT) etc.</li></ul>

![Screenshot 2025-05-20 at 8 32 46 PM](https://github.com/user-attachments/assets/f86d8b3e-bdbf-452e-b1ba-4e153039c93e)


<b>SQL Clauses:</b>
<p>SQL clauses are components of SQL statements that define the conditions, or filters to be applied to the data. They control the behaviour of SQL statements, and specify what data to retrieve, modify, or operate on.</p>
<ul><li>Example: FROM, DISTINCT, WHERE, HAVING, GROUP BY, ORDER BY, LIMIT etc. </li></ul>

![Screenshot 2025-05-20 at 8 36 02 PM](https://github.com/user-attachments/assets/27f3c716-a71b-461e-9869-453c70bae40c)


<b>SQL Operators:</b>
<p>SQL operators are symbols or keywords used to perform operations on data values or expressions. They can be used within SQL statements to compare values, perform arithmetic calculations, concatenate strings, and more.</p>
<ul><li>Example: comparison operators ( ie. =, !=, <, >, <=, >=, BETWEEN, LIKE), arithmetic operators (ie.+, -, *, /, %), logical operators (ie. AND, OR, NOT), and assignment operators (ie. =, +=, -=) etc.</li></ul>

