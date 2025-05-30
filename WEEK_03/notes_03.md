<h2> Week 3: Relational Database Fundamentals</h2>

<b>Tabular Data Storage:</b>
<p>Tabular data storage refers to organizing data in a tabular format, often called a table or an entity, consisting of rows (records/entries) and columns (attributes/field).</p>
<ul>
<li><b>RECORD:</b> A record, also known as a row, entry, or entity represents an individual data entry</li>
<li><b>COLUMN:</b> An column, also known as an attribute or field, represents a specific attribute or characteristic of the data. Typically, this is what is referred to as a variable in programming.</li>
<li><b>VALUE:</b> a value, similar to a cell in a spreadsheet aka a field, is a single element stored within a table.</li>
</ul>

<b> What is an SQL key? </b>
<p> These are components of relational databases that help define relationships between tables and ensure data integrity. SQL keys are like identification numbers for rows in a database table. For instance, a bank
account number uniquely identifies a bank account, a VIN number uniquely identifies a car, a social
insurance or security number identifies a person. There are two main types: primary keys, and foreign keys.</p>

<ul><li><b>PRIMARY KEY:</b>
A primary key is a unique identifier for each record in a table. Let's go over some of the most frequently used primary key types:
<ul>
<li><b>SURRAGATE KEY:</b>
  These are artificially generated unique identifiers, auto-incrementing or randomly generated, that typically only serve meaning within the context of the table.
<li><b>NATURAL KEY:</b> A natural primary key is a key that is derived from the data itself, such as a unique identifier inherent to the data domain. 
  Natural primary keys are often based on attributes that naturally occur in the data, like email addresses, user_id, ip address, sku, device ids etc.</li>
</ul></li></ul>

<ul><li><b>FOREIGN KEY:</b>
A foreign key is a column or set of columns in a table that establishes a link between data in two tables.
It represents a relationship between the data in the current table (child table) and the data in another table (parent table).
The foreign key column typically contains values that correspond to the primary key values in the related table.</li></ul>

<b>Why do we need to know about keys?</b>

<p>This is because having a great understanding of primary and foreign keys are important for performing joins,  data integrity, normalization, and query optimization. In the context of this course, these concepts will be  useful for performing joins later on in this course. Whilst the focus of this course may be on joins, a deeper understanding of keys can be beneficial to your data science journey.</p>

