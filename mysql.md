## MySQL Structure
<p><strong>Numeric types</strong>:</p>

<table><thead>
<tr>
<th>Data Type</th>
<th>Explanation</th>
</tr>
</thead><tbody>
<tr>
<td><code>tinyint</code></td>
<td>A very small integer. The signed range for this numeric data type is -128 to 127, while the unsigned range is 0 to 255.</td>
</tr>
<tr>
<td><code>smallint</code></td>
<td>A small integer. The signed range for this numeric type is -32768 to 32767, while the unsigned range is 0 to 65535.</td>
</tr>
<tr>
<td><code>mediumint</code></td>
<td>A medium-sized integer. The signed range for this numeric data type is -8388608 to 8388607, while the unsigned range is 0 to 16777215.</td>
</tr>
<tr>
<td><code>int</code> or <code>integer</code></td>
<td>A normal-sized integer. The signed range for this numeric data type is -2147483648 to 2147483647, while the unsigned range is 0 to 4294967295.</td>
</tr>
<tr>
<td><code>bigint</code></td>
<td>A large integer. The signed range for this numeric data type is -9223372036854775808 to 9223372036854775807, while the unsigned range is 0 to 18446744073709551615.</td>
</tr>
<tr>
<td><code>float</code></td>
<td>A small (single-precision) floating-point number.</td>
</tr>
<tr>
<td><code>double</code>, <code>double precision</code>, or <code>real</code></td>
<td>A normal sized (double-precision) floating-point number.</td>
</tr>
<tr>
<td><code>dec</code>, <code>decimal</code>, <code>fixed</code>, or <code>numeric</code></td>
<td>A packed fixed-point number. The display length of entries for this data type is defined when the column is created, and every entry adheres to that length.</td>
</tr>
<tr>
<td><code>bool</code> or <code>boolean</code></td>
<td>A Boolean is a data type that only has two possible values, usually either <code>true</code> or <code>false</code>.</td>
</tr>
<tr>
<td><code>bit</code></td>
<td>A bit value type for which you can specify the number of bits per value, from 1 to 64.</td>
</tr>
</tbody></table>

<p><strong>Date and time types</strong>:</p>

<table><thead>
<tr>
<th>Data Type</th>
<th>Explanation</th>
</tr>
</thead><tbody>
<tr>
<td><code>date</code></td>
<td>A date, represented as <code>YYYY-MM-DD</code>.</td>
</tr>
<tr>
<td><code>datetime</code></td>
<td>A timestamp showing the date and time, displayed as <code>YYYY-MM-DD HH:MM:SS</code>.</td>
</tr>
<tr>
<td><code>timestamp</code></td>
<td>A timestamp indicating the amount of time since the <a href="https://en.wikipedia.org/wiki/Unix_time">Unix epoch</a> (00:00:00 on January 1, 1970).</td>
</tr>
<tr>
<td><code>time</code></td>
<td>A time of day, displayed as <code>HH:MM:SS</code>.</td>
</tr>
<tr>
<td><code>year</code></td>
<td>A year expressed in either a 2 or 4 digit format, with 4 digits being the default.</td>
</tr>
</tbody></table>

<p><strong>String types</strong>:</p>

<table><thead>
<tr>
<th>Data Type</th>
<th>Explanation</th>
</tr>
</thead><tbody>
<tr>
<td><code>char</code></td>
<td>A fixed-length string; entries of this type are padded on the right with spaces to meet the specified length when stored.</td>
</tr>
<tr>
<td><code>varchar</code></td>
<td>A string of variable length.</td>
</tr>
<tr>
<td><code>binary</code></td>
<td>Similar to the <code>char</code> type, but a binary byte string of a specified length rather than a nonbinary character string.</td>
</tr>
<tr>
<td><code>varbinary</code></td>
<td>Similar to the <code>varchar</code> type, but a binary byte string of a variable length rather than a nonbinary character string.</td>
</tr>
<tr>
<td><code>blob</code></td>
<td>A binary string with a maximum length of 65535 (2^16 - 1) bytes of data.</td>
</tr>
<tr>
<td><code>tinyblob</code></td>
<td>A <code>blob</code> column with a maximum length of 255 (2^8 - 1) bytes of data.</td>
</tr>
<tr>
<td><code>mediumblob</code></td>
<td>A <code>blob</code> column with a maximum length of 16777215 (2^24 - 1) bytes of data.</td>
</tr>
<tr>
<td><code>longblob</code></td>
<td>A <code>blob</code> column with a maximum length of 4294967295 (2^32 - 1) bytes of data.</td>
</tr>
<tr>
<td><code>text</code></td>
<td>A string with a maximum length of 65535 (2^16 - 1) characters.</td>
</tr>
<tr>
<td><code>tinytext</code></td>
<td>A <code>text</code> column with a maximum length of 255 (2^8 - 1) characters.</td>
</tr>
<tr>
<td><code>mediumtext</code></td>
<td>A <code>text</code> column with a maximum length of 16777215 (2^24 - 1) characters.</td>
</tr>
<tr>
<td><code>longtext</code></td>
<td>A <code>text</code> column with a maximum length of 4294967295 (2^32 - 1) characters.</td>
</tr>
<tr>
<td><code>enum</code></td>
<td>An enumeration, which is a string object that takes a single value from a list of values that are declared when the table is created.</td>
</tr>
<tr>
<td><code>set</code></td>
<td>Similar to an enumeration, a string object that can have zero or more values, each of which must be chosen from a list of allowed values that are specified when the table is created.</td>
</tr>
</tbody></table>

## DUMP MySQL
<ul>
<li class="has-line-data" data-line-start="1" data-line-end="2">O MySQL disponibiliza uma ferramenta simples para exportar bancos de dados diretamente no servidor, o mysqldump. Com essa ferramenta você pode fazer dumps de bancos rodando no servidor local ou exportar bancos para outros servidores diretamente.</li>
<li class="has-line-data" data-line-start="2" data-line-end="3">O arquivo exportado contém uma série de comandos e parametros SQL para a criação e importação dos dados.</li>
<li class="has-line-data" data-line-start="3" data-line-end="21">FAZENDO O BACKUP DE UM BANCO MYSQL
<ul>
<li class="has-line-data" data-line-start="4" data-line-end="6">
<p class="has-line-data" data-line-start="4" data-line-end="5">Para utilizar o mysqldump para realizar o backup você precisa ter acesso ao servidor que o serviço está rodando.      - Este acesso pode ser feito por SSH, caso você tenha as credenciais. Após o acesso, você pode usar o comando a seguir:</p>
<ul>
<li class="has-line-data" data-line-start="5" data-line-end="6">mysqldump -u [usuario] –p [banco] &gt; [arquivo.sql]</li>
</ul>
</li>
<li class="has-line-data" data-line-start="6" data-line-end="10">
<p class="has-line-data" data-line-start="6" data-line-end="7">Os parâmetros utilizados no comando acima são os seguintes:</p>
<ul>
<li class="has-line-data" data-line-start="7" data-line-end="8">[usuario] - Nome de usuário com acessos ao banco</li>
<li class="has-line-data" data-line-start="8" data-line-end="9">[banco] - Nome do banco de dados</li>
<li class="has-line-data" data-line-start="9" data-line-end="10">[arquivo.sql] - Nome do arquivo do dump</li>
</ul>
</li>
<li class="has-line-data" data-line-start="10" data-line-end="11">
<p class="has-line-data" data-line-start="10" data-line-end="11">EXPORTAR APENAS A ESTRUTURA DO BANCO</p>
</li>
<li class="has-line-data" data-line-start="11" data-line-end="13">
<p class="has-line-data" data-line-start="11" data-line-end="12">Se você deseja apenas exportar a estrutura do banco, se informações, basta adicionar o comando --no-data, como no exemplo:</p>
<ul>
<li class="has-line-data" data-line-start="12" data-line-end="13">mysqldump -u [usuario] –p --no-data [banco] &gt; [arquivo.sql]</li>
</ul>
</li>
<li class="has-line-data" data-line-start="13" data-line-end="14">
<p class="has-line-data" data-line-start="13" data-line-end="14">EXPORTAR APENAS AS INFORMAÇÕES</p>
</li>
<li class="has-line-data" data-line-start="14" data-line-end="17">
<p class="has-line-data" data-line-start="14" data-line-end="15">Se você deseja exportar apenas as informações do banco, sem a estrutura, basta adicionar o comando --no-create-info, como no exemplo a seguir:</p>
<ul>
<li class="has-line-data" data-line-start="16" data-line-end="17">mysqldump -u [usuario] –p --no-create-info [banco] &gt; [arquivo.sql]</li>
</ul>
</li>
<li class="has-line-data" data-line-start="17" data-line-end="18">
<p class="has-line-data" data-line-start="17" data-line-end="18">EXPORTAR DIVERSOS BANCOS PARA UM ÚNICO ARQUIVO</p>
</li>
<li class="has-line-data" data-line-start="18" data-line-end="21">
<p class="has-line-data" data-line-start="18" data-line-end="19">Você pode passar como parâmetro diversos bancos de dados para serem exportados para um único arquivo:</p>
<ul>
<li class="has-line-data" data-line-start="19" data-line-end="20">mysqldump -u [usuario] –p [banco1, banco2, …] &gt; [arquivo.sql]</li>
<li class="has-line-data" data-line-start="20" data-line-end="21">mysqldump -u [usuario] –p --all-databases &gt; [arquivo.sql]</li>
</ul>



## MySQL CLI

Commands
-----------

Access monitor: `mysql -u [username] -p;` (will prompt for password)

Show all databases: `show databases;`

Access database: `mysql -u [username] -p [database]` (will prompt for password)

Create new database: `create database [database];`

Select database: `use [database];`

Determine what database is in use: `select database();`

Show all tables: `show tables;`

Show table structure: `describe [table];`

List all indexes on a table: `show index from [table];`

Create new table with columns: `CREATE TABLE [table] ([column] VARCHAR(120), [another-column] DATETIME);`

Adding a column: `ALTER TABLE [table] ADD COLUMN [column] VARCHAR(120);`

Adding a column with an unique, auto-incrementing ID: `ALTER TABLE [table] ADD COLUMN [column] int NOT NULL AUTO_INCREMENT PRIMARY KEY;`

Inserting a record: `INSERT INTO [table] ([column], [column]) VALUES ('[value]', [value]');`

MySQL function for datetime input: `NOW()`

Selecting records: `SELECT * FROM [table];`

Explain records: `EXPLAIN SELECT * FROM [table];`

Selecting parts of records: `SELECT [column], [another-column] FROM [table];`

Counting records: `SELECT COUNT([column]) FROM [table];`

Counting and selecting grouped records: `SELECT *, (SELECT COUNT([column]) FROM [table]) AS count FROM [table] GROUP BY [column];`

Selecting specific records: `SELECT * FROM [table] WHERE [column] = [value];` (Selectors: `<`, `>`, `!=`; combine multiple selectors with `AND`, `OR`)

Select records containing `[value]`: `SELECT * FROM [table] WHERE [column] LIKE '%[value]%';`

Select records starting with `[value]`: `SELECT * FROM [table] WHERE [column] LIKE '[value]%';`

Select records starting with `val` and ending with `ue`: `SELECT * FROM [table] WHERE [column] LIKE '[val_ue]';`

Select a range: `SELECT * FROM [table] WHERE [column] BETWEEN [value1] and [value2];`

Select with custom order and only limit: `SELECT * FROM [table] WHERE [column] ORDER BY [column] ASC LIMIT [value];` (Order: `DESC`, `ASC`)

Updating records: `UPDATE [table] SET [column] = '[updated-value]' WHERE [column] = [value];`

Deleting records: `DELETE FROM [table] WHERE [column] = [value];`

Delete *all records* from a table (without dropping the table itself): `DELETE FROM [table];`
(This also resets the incrementing counter for auto generated columns like an id column.)

Delete all records in a table: `truncate table [table];`

Removing table columns: `ALTER TABLE [table] DROP COLUMN [column];`

Deleting tables: `DROP TABLE [table];`

Deleting databases: `DROP DATABASE [database];`

Custom column output names: `SELECT [column] AS [custom-column] FROM [table];`

Export a database dump (more info [here](http://stackoverflow.com/a/21091197/1815847)): `mysqldump -u [username] -p [database] > db_backup.sql`

Use `--lock-tables=false` option for locked tables (more info [here](http://stackoverflow.com/a/104628/1815847)).

Import a database dump (more info [here](http://stackoverflow.com/a/21091197/1815847)): `mysql -u [username] -p -h localhost [database] < db_backup.sql`

Logout: `exit;`


Aggregate functions
-----------

Select but without duplicates: `SELECT distinct name, email, acception FROM owners WHERE acception = 1 AND date >= 2015-01-01 00:00:00`

Calculate total number of records: `SELECT SUM([column]) FROM [table];`

Count total number of `[column]` and group by `[category-column]`: `SELECT [category-column], SUM([column]) FROM [table] GROUP BY [category-column];`

Get largest value in `[column]`: `SELECT MAX([column]) FROM [table];`

Get smallest value: `SELECT MIN([column]) FROM [table];`

Get average value: `SELECT AVG([column]) FROM [table];`

Get rounded average value and group by `[category-column]`: `SELECT [category-column], ROUND(AVG([column]), 2) FROM [table] GROUP BY [category-column];`


Multiple tables
-----------

Select from multiple tables: `SELECT [table1].[column], [table1].[another-column], [table2].[column] FROM [table1], [table2];`

Combine rows from different tables: `SELECT * FROM [table1] INNER JOIN [table2] ON [table1].[column] = [table2].[column];`

Combine rows from different tables but do not require the join condition: `SELECT * FROM [table1] LEFT OUTER JOIN [table2] ON [table1].[column] = [table2].[column];` (The left table is the first table that appears in the statement.)

Rename column or table using an _alias_: `SELECT [table1].[column] AS '[value]', [table2].[column] AS '[value]' FROM [table1], [table2];`


Users functions
-----------

List all users: `SELECT User,Host FROM mysql.user;`

Create new user: `CREATE USER 'username'@'localhost' IDENTIFIED BY 'password';`

Grant `ALL` access to user for `*` tables: `GRANT ALL ON database.* TO 'user'@'localhost';`


Find out the IP Address of the Mysql Host
-----------
`SHOW VARIABLES WHERE Variable_name = 'hostname';` ([source](http://serverfault.com/a/129646))