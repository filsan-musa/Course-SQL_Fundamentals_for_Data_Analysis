<h2> Week 4: What is an SQL table?</h2>

<b>Tabular Data Storage:</b>
<p>Tabular data storage refers to organizing data in a table format consisting of rows (records) and columns.</p>
<ul>
<li>RECORD: a record, also known as a row or an entry, represents an individual data entry</li>
<li>COLUMN: a column, also known as a field, represents a specific attribute or characteristic of the data. Typically, this is what is referred to as a variable in programming.</li>
<li>VALUE: a value, similar to a cell in a spreadsheet aka a field, is a single element stored within a table.</li>
</ul>

Primary Key:
A primary key is a unique identifier for each record in a table. A primary key can be 
- composite keys
- 
A natural primary key is a key that is derived from the data itself, such as a unique identifier inherent to the data domain.
Natural primary keys are often based on attributes that naturally occur in the data, like email addresses, user_id, ip address, sku, device ids etc.

Foreign Key:
A foreign key is a column or set of columns in a table that establishes a link between data in two tables.
It represents a relationship between the data in the current table (child table) and the data in another table (parent table).
The foreign key column typically contains values that correspond to the primary key values in the related table.
