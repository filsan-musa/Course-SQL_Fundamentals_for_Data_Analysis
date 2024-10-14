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
<p>Extracts the time part from a datetime value, typically returning the current time or the time portion of a specific datetime. Time() returns the time in the format HH:MM:SS.<li>
Example: If the datetime is 2024-09-16 14:30:45, Time() would return 14:30:45.</li></p></li>

<li><b>DAY():</b>
<p>Extracts the day of the month from a given date or datetime, returning an integer value representing the day.
Example: For the date 2024-09-16, Day() would return 16.</p></li>

<li><b>MONTH():</b>
<p>Extracts the month from a given date or datetime, returning an integer value representing the month.
Example: For the date 2024-09-16, Month() would return 9.</p></li>

<li><b>YEAR():</b>
<p>Extracts the year from a given date or datetime, returning the year as a four-digit integer.
Example: For the date 2024-09-16, Year() would return 2024.</p></li>

<li><b>TIMESTAMP():</b> Represents a specific point in time, including both date and time, typically returns the date and time or can be used to represent a specific moment in time with the format YYYY-MM-DD HH:MM:SS.
Example: If the current date and time are 2024-09-16 14:30:45, the Timestamp() function might return this exact value.</li>

<li><b>DATE():</b> Extracts or returns the date part from a datetime value, typically ignoring the time portion.
Usage: Date() returns a date in the format YYYY-MM-DD.
Example: For the datetime 2024-09-16 14:30:45, Date() would return 2024-09-16.</li>
</ul>

<b>DATETIME KEYWORDS</b>

<li> CURRENT_TIME, CURRENT_DAY, 
</li>
