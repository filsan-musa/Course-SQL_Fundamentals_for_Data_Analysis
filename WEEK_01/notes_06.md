<h2>Week 6: What are the SQL data types?</h2>

<p> When creating a variable in SQL, it is important to specify the data type that the values stored in the variable will assume. This defines the storage requirements (ie. allocate memory, storage etc), valid operations, and potential values for the variable.</p>

<b>BOOLEAN:</b>
<ul><li>BOOLEAN: Stores logical values (ie. True or False). These values can also take integer forms of 1 for True and 0 for false (essentially data is denoted by a single bit).</li></ul>

<b>NUMERIC:</b>
<ul><li>INT (OR INTEGER): Stores any integer value that uses up to 4 bytes of storage. It can typically store integer values between -2,147,483,648 to 2,147,483,647</li>
<ul><li>BIGINT: Stores any integer value that uses up to 8 bytes of storage. It can typically store integer values in the range of -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807.</li>
<li>SMALLINT: Stores any integer value that uses up to 2 bytes of storage. It can typically store integer values in the range of -32,768 to 32,767.</li>
<li>Example: -1,897,234,6540, 0, 10, 6666666 etc.</li></ul>
<li>FLOAT: Stores any real number value that uses up to 8 bytes of storage.</li>
<ul><li>Example: -1, 0, 7.2598234, π, ⅓, sqrt 2 etc.</li></ul></ul>

<b>STRING:</b>
<ul><li>CHAR(n): Stores fixed-length character strings, if total string length is less than n the remaining space will be filled with whitespace</li>
<ul><li>Example: CHAR(2) can store only up to 2 characters, any character combination up to 2 character space. ON, !, a@, 3b are all valid entries.</ul>
<li>VARCHAR(n): Variable-length character strings with a maximum length of n.</li>
<ul><li>Example: VARCHAR(24) can store any length of characters between 1-24. As opposed to CHAR(n) which fills empty spaces with whitespace, any unused space will be saved.</ul>
<li>TEXT: Variable-length character strings with no maximum length.</li></ul>

<b>DATETIME:</b>
<ul><li>DATE: Stores date values in the following format: YYYY-MM-DD.</li>
<li>TIME: Stores time values in the following format: HH:MM:SS.</li>
<li>TIMESTAMP: Stores date and time (also known as datetime) values in the following format: YYYY-MM-DD HH:MM:SS.</li></ul>
