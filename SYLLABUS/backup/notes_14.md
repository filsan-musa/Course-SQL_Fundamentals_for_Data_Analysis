Week 14: Use cases for the Case When statement

Case WHEN Statement in SQL
The CASE WHEN statement allows you to implement conditional logic within your SQL queries. It evaluates a series of conditions and returns a specific value based on the first true condition.
Use Cases:
1. Using CASE WHEN with Logical & Comparison Operators
Scenario: You want to assign a grade letter ("Excellent", "Good", "Average", "Below Average") based on student scores stored in a score column.
Explanation: We can use logical operators (AND, OR) and comparison operators (<, >, =) to define the conditions for each grade level.
Syntax:
SELECT student_name, score,
  CASE WHEN score >= 90 THEN 'Excellent'
       WHEN score >= 80 THEN 'Good'
       WHEN score >= 70 THEN 'Average'
       ELSE 'Below Average'
  END AS grade_letter
FROM student_table;


2. Using CASE WHEN with Arithmetic Operators
Scenario: You want to calculate a price discount based on the quantity of an item purchased (e.g., 10% discount for 3 or more items).
Explanation: We can use arithmetic operators (+, -, *) within the THEN clause to perform calculations for the discount.
Syntax:
SELECT product_name, quantity, price,
  CASE WHEN quantity >= 3 THEN price * 0.9  -- 10% discount
       ELSE price
  END AS discounted_price
FROM sales_table;


Benefits of Using CASE WHEN:
Improves code readability by making conditional logic explicit.
Reduces the need for complex WHERE clauses or multiple IF statements.
Can be used for data cleaning and categorization.
