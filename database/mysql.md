## Introduction
This document contains frequently used command and the corresponding used cases for MySQL database. For simplification, all the variables are written in parenthesis, e.g. (package), (version). The optional parameters are written in sqaure brackets, e.g. [--versions], [--mixed]

&nbsp;
## Table of Content
* [Database Setting](#database-setting)
* [Database Manipulation](#database-manipulation)
* [Table Manipulation](#table-manipulation)
* [Join and Union](#join-and-union)
* [User Management (Admin)](#user-management-admin-)
* [References](#references)

&nbsp;
## Database Setting
<sub>[Back to Top](#introduction)</sub>
#### Start MySQL server (MacOS)
```
$ brew services start mysql
```
#### Start MySQL server (Linux)
```
$ services mysqld start
```
#### Connect to MySQL server
```
$ mysql -h (host) -u (host) -p
```
#### Backup Database
```
$ mysqldump -h (host) -u (host) -p (database) [table] > (file).sql
```
#### Restore Database
```
$ mysql -h (host) -u (user) -p (database) < (file).sql
```
#### Import CSV to existing table
```bash
# Create database and tables in advance
mysqlimport --ignore-lines=1 --fields-terminated-by=',' --local -h (host) -u (user) -p (database) (csv)
```
&nbsp;
## Database Manipulation
<sub>[Back to Top](#introduction)</sub>
#### Show all databases
```sql
SHOW DATABASES;
```
#### Create database
```sql
CREATE DATABASE (DB);
```
#### Remove database
```sql
DROP DATABASE (DB);
```
#### Select database
```sql
USE (DB);
```
#### Log out database
```sql
exit;
```

&nbsp;
## Table Manipulation
<sub>[Back to Top](#introduction)</sub>
#### Show all tables in the database
```sql
USE (DB);
SHOW TABLES;
```
#### Show table structure
```sql
USE (DB);
DESCRIBE (TABLE NAME);
```
#### Create table in the database
```sql
USE (DB);
CREATE TABLE (TABLE NAME) [COL1] [DTYPE1], [COL2] [DTYPE2]...;
```
#### Remove table in the database
```sql
USE (DB);
DROP TABLE (TABLE NAME);
```
#### Copy table
```sql
USE (DB);
CREATE TABLE [NEW TABLE] LIKE [SOURCE TABLE]
```
#### Rename table
```sql
USE (DB);
RENAME [SOURCE TABLE] TO [NEW NAME]
```
#### Insert instance:<br/>
```sql
USE (DB);
INSERT INTO (TABLE) [COL1], [COL2]... VALUES ('[VAL1]', '[VAL2]'...);
```
#### Remove instance
```sql
USE (DB);
DELETE FROM (TABLE) WHERE (CONDITION);
```
#### Clear table
```sql
USE (DB);
DELETE FROM (TABLE);
```
#### Add new columns
```sql
USE (DB);
ALTER TABLE (TABLE) ADD COLUMN [COL1] [DTYPE1], [COL2] [DTYPE2]...;
```
#### Remove columns
```sql
USE (DB);
ALTER TABLE (TABLE NAME) DROP COLUMN (COL);
```
#### Select all instances
```sql
USE (DB);
SELECT ALL (*|COL1|FUN1), (COL2|FUN2)... 
FROM (TABLE)
WHERE [CONDITION]
GROUP BY [COL]
HAVING [CONDITION]
ORDER BY [COL1|FUN1] [DESC|ASC], [COL2|FUN2] [DESC|ASC]... 
LIMIT [BYPASS HOW MANY],[REPORT HOW MANY]
```
#### Select unique instances
```sql
USE (DB);
SELECT DISTINCT (*|COL1|FUN1), (COL2|FUN2)... 
FROM [TABLE]
WHERE [CONDITION]
GROUP BY [COL]
HAVING [CONDITION]
ORDER BY [COL1|FUN1] [DESC|ASC], [COL2|FUN2] [DESC|ASC]... 
LIMIT [BYPASS HOW MANY],[REPORT HOW MANY]
```

&nbsp;
## Join and Union
<sub>[Back to Top](#introduction)</sub>
#### Inner join
```sql
-- Method 1
SELECT (TABLE_A).(COL1), (TABLE_B).(COL2)..., (TABLE_B).(COL1), (TABLE_B).(COL2)...
FROM (TABLE_A), (TABLE_B)
WHERE (TABLE_A).(JOIN_COL) = (TABLE_B).(JOIN_COL)
-- Method 2
SELECT (TABLE_A).(COL1), (TABLE_B).(COL2)..., (TABLE_B).(COL1), (TABLE_B).(COL2)...
FROM (TABLE_A) INNER JOIN (TABLE_B) ON (TABLE_A).(JOIN_COL) = (TABLE_B).(JOIN_COL)
-- Method 3
SELECT (TABLE_A).(COL1), (TABLE_B).(COL2)..., (TABLE_B).(COL1), (TABLE_B).(COL2)...
FROM (TABLE_A) INNER JOIN (TABLE_B) USING (JOIN_COL)
```
#### Outher join
```sql
-- Method 1
SELECT (TABLE_A).(COL1), (TABLE_B).(COL2)..., (TABLE_b).(COL1), (TABLE_B).(COL2)...
FROM (TABLE_a) (LEFT|RIGHT) OUTER JOIN (TABLE_B) ON (TABLE_A).(JOIN COL) = (TABLE_B).(JOIN COL)
-- Method 2
SELECT (TABLE_A).(COL1), (TABLE_B).(COL2)..., (TABLE_B).(COL1), (TABLE_B).(COL2)...
FROM (TABLE_A) (LEFT|RIGHT) OUTER JOIN (TABLE_B) USING (JOIN_COL)
```
#### Union
```sql
SELECT [COL1|FUN1], [COL2,|FUN2]... 
FROM [TABLE_A]
WHERE [CONDITION]
UNION
SELECT [COL1|FUN1], [COL2,|FUN2]... 
FROM [TABLE_B]
WHERE [CONDITION]
```

&nbsp;
## User Management (Admin)
<sub>[Back to Top](#introduction)</sub>
#### List users
```sql
SELECT User, Host from mysql.user;
```
#### Create user
```sql
CREATE USER [USER]@[HOST] IDENTIFIED BY [PASSWORD];
```
#### Remove user
```sql
DROP USER [USER]@[HOST];
```
#### Show user privileges
```sql
SHOW GRANTS FOR [USER]@[HOST];
```
#### Grant user privileges
```sql
GRANT [PRI1], [PRI2]... ON [DB].[TABLE] TO [USER]@[HOST];
FLUSH PRIVILEGES;
```
#### Revoke user privileges
```sql
REVOKE [PRI1], [PRI2]... ON [DB].[TABLE] FROM [USER]@[HOST];
FLUSH PRIVILEGES;
```
&nbsp;
## References
<sub>[Back to Top](#introduction)</sub>
* [Datatypes](https://dev.mysql.com/doc/refman/8.0/en/data-types.html)
* [Operators](https://dev.mysql.com/doc/refman/8.0/en/non-typed-operators.html)
* [Priviledges](https://dev.mysql.com/doc/refman/8.0/en/privileges-provided.html)