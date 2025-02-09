<h2>Week 9: Basic Formatting Functions & Keywords</h2>

<b> STRING FUNCTIONS </b>
<ul>
<li><b>LOWER()</b>
<p>When you want to convert all characters in a string to lowercase. This is useful for ensuring case-insensitive comparisons or standardizing data.
Application: Standardizing usernames for login purposes (all usernames in lowercase for easier comparison).</p></li>

```sql
SELECT LOWER(column_name) AS formatted_data
FROM your_table
```

<li><b>UPPER()</b>
<p>When you want to convert all characters in a string to uppercase. This can be useful for displaying data in a specific format.
Application: Converting product names to uppercase for a catalog.</p></li>

```sql
SELECT UPPER(column_name) AS formatted_data
FROM your_table;
```
</ul>
<b>NUMERIC FUNCTIONS</b>
<ul>
<li><b>FLOOR()</b>
<p>When you want to round a number down to the nearest whole number (integer).
Application: Calculating the whole number of items needed based on a fractional quantity (e.g., flooring 2.5 items to 2 items).</p></li>

```sql
SELECT FLOOR(numeric_column) AS rounded_down_value
FROM your_table;
```

<li><b>ROUND()</b>
<p>When you want to round a number to a specified number of decimal places. You can round up, down, or to the nearest even number.
Application: Rounding currency values to two decimal places for display purposes.</p></li>

```sql
SELECT ROUND(numeric_column, decimal_places) AS rounded_value
FROM your_table;
```
Note: The specific syntax for ROUND can vary slightly depending on the SQL platform you're using.
</ul>

<b>DATETIME FUNCTIONS</b>
<ul>
<li><b>TIME()</b>
<p>Extracts the time part from a datetime value, typically returning the current time or the time portion of a specific datetime. Time() returns the time in the format HH:MM:SS.</p>
<p><i>Example: If the datetime is 2024-09-16 14:30:45, Time() would return 14:30:45.</i></p></li>

<li><b>DAY():</b>
<p>Extracts the day of the month from a given date or datetime, returning an integer value representing the day</p>
<p><i>Example: For the date 2024-09-16, Day() would return 16.</i></p></li>

<li><b>MONTH():</b>
<p>Extracts the month from a given date or datetime, returning an integer value representing the month.</p>
<p><i>Example: For the date 2024-09-16, Month() would return 9.</i></p></li>

<li><b>YEAR():</b>
<p>Extracts the year from a given date or datetime, returning the year as a four-digit integer.</p>
<p><i>Example: For the date 2024-09-16, Year() would return 2024.</i></p></li>

<li><b>TIMESTAMP():</b> 
<p>Represents a specific point in time, including both date and time, typically returns the date and time or can be used to represent a specific moment in time with the format YYYY-MM-DD HH:MM:SS.</p>
<p><i>Example: If the current date and time are 2024-09-16 14:30:45, the Timestamp() function might return this exact value.</i></p></li>

<li><b>DATE():</b> 
<p>Extracts or returns the date part from a datetime value, typically ignoring the time portion.
Usage: Date() returns a date in the format YYYY-MM-DD.</p>
<p><i>Example: For the datetime 2024-09-16 14:30:45, Date() would return 2024-09-16.</i></p></li>
</ul>

<b>DATETIME KEYWORDS</b>
<ul>
<li><b> CURRENT_TIMESTAMP:</b>
<p>Returns the current date and time, usually in the format YYYY-MM-DD HH:MM:SS. Alternatively, you can use CURRENT_DATE to extract the date, and CURRENT_TIME to extract the current time.</p>
</li>

<li><b> NOW():</b>
<p>Returns the current date and time, in the format YYYY-MM-DD HH:MM:SS. The NOW() function does not work in SQLite which is used in this course, but is popular in other flavours of SQL (ie. MySQL, PostgreSQL, MariaDB). CURRENT_TIMESTAMP is generally more widely supported and more standardized than NOW().</p>
</li>

Note: These are some of the most commonly used datetime keywords and are sufficient for an intro level understanding of datetime keywords.
<ul>
