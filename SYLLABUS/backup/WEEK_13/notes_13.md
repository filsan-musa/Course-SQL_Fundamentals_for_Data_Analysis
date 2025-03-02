Week 13: Arithmetic Operators

Arithmetic operators: In SQL, you can use mathematical functions to manipulate numerical data from your tables, allowing you to analyze and transform your data.

Product  (*): This operator multiplies two values.

SQL Syntax Example:
SELECT column_1 * column_2 AS column_3
FROM table_a;

This query selects a new column name ‘column_3’ from ‘table_a’ , where each value in ‘column_3’ is the product of the corresponding values in ‘coolumn_1’ and ‘column_2’. 

Division (/): This operator divides one value by another.

SQL Syntax Example:
SELECT column_1 = SUM(rating) / COUNT(*)
FROM table_a;

This syntax calculates the average rating by dividing the sum of ratings by the total number of reviews.

Addition (+): This operator adds two values.

SQL Syntax Example:
SELECT *
FROM table_a
WHERE column_2 + column_1> 1000;

This syntax checks if the sum of balance and interest_rate in a bank account is greater than 1000.

Subtraction (-): This operator subtracts one value from another.

SQL Syntax Example:
SELECT column_1
FROM table_a
WHERE YEAR(CURDATE()) - YEAR(hire_date) >= 5;

This syntax calculates the years of experience for employees by subtracting the year of hire (YEAR(hire_date)) from the current year (YEAR(CURDATE())).


Modulo (%): This operator calculates the remainder after a division operation.

SQL Syntax Example:
SELECT column_1, column_2
FROM table_a
WHERE column_1 % 2 = 1;

This syntax retrieves data for students with odd-numbered IDs. The modulo operation (id % 2) leaves a remainder of 1 for odd IDs.
