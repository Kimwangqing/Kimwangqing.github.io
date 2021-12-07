---
layout: post
title: "MySQL Study Notes "
date: 2020-09-10
excerpt: "MySQL Study Notes"
tags: [sample post, images, test]
comments: true
mermaid: true
feature: /assets/img/SQL.jpg
---

[TOC]

# SQL Study Notes
## Basic Knowledge
### 数据库类型
数据库按照**数据结构**来组成、存储、存储和管理数据，共三种模型：
* 层次模型
* 网状模型
* 关系模型（基于数学理论，最终获得绝对市场份额）

### SQL Defines Several Operation Abilities
* DDL: Data Definition Language: Creating form, deletiing form, modifying form structure(修改表结构), etc,.
* DML: Data Manipulation Language: Adding data, deleting data, updating data, etc,.
* DQL: Data Query Language: querying(the most commonly operation) 

### MySQL 
Actually, MySQL is a SQL interface only, and including multiple data engines. 
Different form can use different data engine. It is reasonable to use **InnoDB**(created by Innobase Oy company, and acquired by Oracle in 2006) when you don't know which one engine should be used. 

Community Edition: a free and open source version created MySQL. 
The following versions incremented sequentially on price and function by MySQL are:
* Stardard Edition
* Enterprise Edition
* Cluster Carrier Grade Edition(集群版)

## Run SQL
1. Run SQL with MySQL 8.0 Command Line Client.
2. Run SQL with Windows command line. 
    1). Enter the file including MySQL.
    2). Run `mysql -u root -p`
To restart mysql server, use `net start mysql`

## Relationship Model (关系模型)
* Each row calls Record（记录）.
* Each column calls Column(字段：整型、浮点型、字符串、日期等).
In relationship model, the relation is maintained by primary keys and foreign keys (主键和外键). 

### Primary Key
One Column  seperates two Records(they are same execpt one Column(字段) ) called a primary key(主键).
Better not to **change the primary key** when it inserted into the form. Because the primary key is only the Column to locate(确定) the record.

#### Principle
**The principle of selecting the primary key is**
* A primary key column doesn't relate to transactions. Because transactions are easy to be changed as to scenarios. These keys, such as ID, phone number and email address, which seems that they have unique properties, actually, they will be changed as to scenarios, cannot be assigned as primary keys.
* A primary key column cannot contain `NULL` value.
* A primary key is always defined as “id", the most common types are: 
	* BIGINT(自增整数类型) Database allocates one BIGINT when inserting each record, in this way, we don't worry the primary key will be repeated, and also cannot be created in advance. This type of id can meet requirements for most applications. 
	* 全局唯一 GUID 类型

#### Composite Keys (联合主键)
Two or more than two columns are allowed to be set as primary keys called Composite Keys (**Try not to use associate keys**).

### Foreign Key (外键)
The Column associating to another form is called a foreign key. 
![](../pic/MySQL study notes/foreign key.jpg)

* Delete foreign keys through `ALTER TABLE student`（表名） and  `DROP FOREIGN KEY fk_class_id`（外键名）. It doesn't mean to delete the foreign key column by deleting the foreign key constraints. To delete the column with the foreign key constraint by using `DROP COLUMN ...`
* D and  COLUMN(column name)`. 
* Foreign keys can define one-to-many, many-to-many, and one-to-one relationships.
* 外键既可以通过数据库来约束，也可以不设置约束，仅依靠应用程序的逻辑来保证。
* Through foreign key constraints, the invalid data cannot  be inserted into the relationship database, such as, the `class` form doesn't exist the record of `id=99`, the `student` form cannot insert the `class_id=99` record. 
* The foreign key constraints reduces database performance. For the purpose of speed, most applications don't use the foreign key constraints. 
* 关系数据库通过外键可以实现一对多、多对多和一对一的关系。外键既可以通过数据库来约束，也可以不设置约束，仅依靠应用程序的逻辑来保证。

### Index(索引) 
The use of the index is to speed up inqueries by locating records that match query conditions, instead of scanning the entire tables. 
* Creating Index by `ALTER TABLE ...` (table name)
               `ADD INDEX ...`(index name)
例如：
> `ALTER TABLE` students
> `ADD INDEX` idx_score(score); (index_score is the index name which is arbitrary. If more than one column to index, the name should be written one by one, such as, 
> `ALTER TABLE` students
> `ADD INDEX` index_name_score (name, score).
* If the more different about the column values, the higher inquery efficiency of the index.
* The index is senseless if the column values are same mostly, such as the value of gender.
* More than one index can be created in one table, but they make the speed slow down when the table inserts, deletes, updates records meanwhile the index should be modified simutaneously. 
* The relationship database creates the index to the primary key automatically. The efficiency is the highest to use the primary key index. 

#### Unique Index and Primary Key
**A column containing unique values, such as an identity ID and a mobile number which relates to transactions, cannot be defined as a primary key, but it can be added a unique index to make sure the uniqueness.**

>`ALTER TABLE` students
>`ADD UNIQUE INDEX` uni_name  (name);

or can be added a unique constraint to the column to keep the uniqueness of the column (because index consumes disk).
>`ALTER TABLE` students
>`ADD CONSTRAINT` uni_name `UNIQUE` (name);

## Prepare Data
* Use the data prepared by Liao by copying the scripts from the github into Notepad in d: and  saving it as sql file (to select the saving type is must, only to add .sql in the file name is invalid ).
* Run cmd.
* Run `mysql -u root -p`.
* Enter the password.
* Run `source d:\init-test-data.sql` to upload the source to mysql (or init-test-data if the name doesn't includ the suffix but the saved format is sql.)
* Get the result as shown in the following pic.
![](../pic/MySQL study notes/init-test-data.jpg?raw=true)
*  (To fix mess data)
    ![](../pic/MySQL study notes/variable%20value.jpg?raw=true)
  * Use `show variables like 'char%'` (单、双引号都可以） to check the variable value. 
  	* The source script use `CHARSET=utf8` 
  	* Find the inconsistance between `character_set_client | gbk` and ` character_set_server | utf8mb4`
  	* Run `set character_set_client = utf8` &  `set character_set_server = utf8` to make them consistant.
  	* Run `source d:\init-test-data;` to import the database again.
  	* Run `SELECT * FROM students`, and then the misdata is fixed. 
    ![](../pic/MySQL study notes/fixinconsistance.jpg?raw=true)
    
## Query Data
* Query language: `SELECT * FROM <the name of the table>
	* `SELECT` means will perform a query.
	* `*` means all columns.
	* `FROM` means which table to be checked. 
	* `...` means the name of the table.
	* `SELECT` can perform calculation
       perform `select 100+200`
       get result `300`
    * Perform `SELECT 1` to check if the data base has been collected. 

## Query Conditions
* Run `SELECT * FROM <name of the table> WHERE <condition>`
  For example, `SELECT * FROM students WHERE score >= 80;`

### Query Conditions - AND
* Use `AND` to connect conditions.
  For example, `SELECT * FROM students WHERE score >= 80 AND gender = `M`; (the both is okay to use single quotes or not)

### Query conditions - OR
* TO select either condition A or condition B. 

### Query Conditions - NOT 
For example,  
`SELECT * FROM students WHERE score >= '80' AND NOT class_id = '2';`
(`AND` `NOT` can be used together.)

* `NOT class_id = 2` same as `class_id <> 2`, so `NOT` format is not often be used. 
`SELECT * FROM students WHERE score >= 80 AND class_id <> 2;`

### Query Conditions - ()
For example, `SELECT * FROM students WHERE (score < 80 OR score > 90) AND gender = 'M';`

### Query Conditions - Priority
If don't use brackets (), conditions to be performed by the priority from `NOT`, `AND` to `OR`, but the brackets () can break the priority. 

### Query Conditions - LIKE
`LIKE` means similarity. For example, `name LIKE 'ab%'`, `%` means any character;
`show variables like 'char%'`(单、双引号都可以）

### Practice
![](../pic/MySQL study notes/query-practice.jpg?raw=true)

## Query Projections
* Use query projections to select specified column. 
* Use comma to seperate each column query. 
  For example, `SELECT id, score, name FROM students;`

### Give Another Name to Column
* Give another name to the column by putting another name besides of the original one. 
  For example, `SELECT id, score points, name FROM students;` `points` is the alias of score. 

### Query Projections with WHERE conditions
Query projections can combine with WHERE conditions to perfom complex query. 
For example, `SELECT id, score, name FROM students WHERE gender = 'M';

## Query Order
* Query results in an order of by default. 
* Use `ORDER BY` to sort in other conditions. 
  For example, `SELECT id FROM students ORDER BY score;`
  
### Descending Order
* Query results in a reverse order by using `ORDER BY ... DESC. 

### Ascending Order
* Query results in a normal order by using `ORDER BY ... ASC`, which is same with `ORDER BY ...`.

* If there are same data occourred, to order them by adding the column name. 
  For example, `SELECT id, name, gender, score FROM students ORDER BY score DESC;` 
  ![](../pic/MySQL study notes/score%20order%20without%20gender.jpg?raw=true)
  (Male is prior to Female by default.)
  ![](../pic/MySQL study notes/score%20order%20with%20gender.jpg?raw=true)
  (Female is prior to Male by adding the  gender in ORDER BY.)
  
* `SELECT class_id, gender, score FROM test.students GROUP BY class_id, gender ORDER BY score DESC;`
  
  Put `ORDER BY` behind of `GROUP BY`.  

### ORDER BY with WHERE
* Put `ORDER BY` behind of `WHERE`.
For example, `SELECT * FROM students WHERE class_id = 1 ORDER BY score DESC;`

### ORDER BY with GROUP BY
For example, `SELECT class_id, gender, name, max(score) from test.students group by class_id, gender order by class_id;`

## Select Data and Split on Pages
* Use `LIMIT <M> OFFSET <N>` to perform.
  For example, `SELECT * FROM students LIMIT 3 OFFSET 0;`, that means the max of selection is 3 records on each page and index from 0 (SQL index from 0 but counts from 0 + 1), and show the first page only. 
  
  If wants to show the second page, use LIMIT 3  OFFSET 3.
  
* OFFSET = pageSize * (pageIndex - 1) 
	* pageSize = LIMIT 
	* pageIndex is the current page number and is different with OFFSET. pageIndex counts from 1.
	
* `LIMIT <M> OFFSET <N>` can be simplified as `LIMIT <N>,<M>;` 

* Use `SELECT COUNT(*) FROM students;` to get the total number of records of the table. 
  ![](../pic/MySQL study notes/count(id).jpg?raw=true)

## Aggregate Selection
* Use `SELECT COUNT(*) FROM xxx` to count the total number of records and to get a two-dimentional table not only a number. 
  For example, `SELECT COUNT(*) FROM students;`
* `SELECT COUNT(*) FROM xxx` = `SELECT COUNT(id) FROM students;`
* Give another name to `COUNT(*)` by adding a name besides of `COUNT(*)`.
  For example, `SELECT COUNT(*) num FROM students;`
* Can perform with WHERE.
  For example, `SELECT COUNT(*) boy From students WHERE gender = 'M' (The single quotes are must for gender. )

### Other Aggregate Selection
|Type|Des.|
|---|---|
|SUM|Get the total value of the column. Must be numbers.|
|AVG|Get the avarage value of the column. Must be numbers. For example,  `SELECT AVG(score) FROM students;` |
|MAX|Get the maximum value of the column. Not limited to be numbers. For strings will get the first row. For example,`SELECT MAX(name) FROM students;`|
|MIN|Get the minimum value of the column. Not limited to be numbers. For strings will get the last row. For example,`SELECT MIN(name) FROM students;`|

* Use `SELECT CEILING(COUNT(id)/<limit number>) FROM xxx;` or `SELECT CEILING(COUNT(*)/<limit number>) FROM xxx;` to get the total number of the splitted pages. 
  ![](../pic/MySQL study notes/ceiling(count(id).jpg?raw=true) 
  (**CEILING(X) or CEIL(X) means to get the integer upward（向上取整）.**)
For example, 
  `select class_id [班级], gender [性别], max(score) [最高分]  from students
  GROUP BY class_id, gender
  ORDER BY max(score) desc`
### Aggregate Selection Perform with WHERE
* `SELECT AVG(score) FROM students WHERE gender = 'M'`。

### GROUP BY
* Use `GROUP BY` to instead WHERE condition, because it doesn't need write WHERE when each condition changed, and get each group of result instead of only one result. 
* As usual, `group by` at the last of the syntax. 
For example:
![](../pic/MySQL study notes/group%20by%20classid.jpg?raw=true)

#### Having clause
The Having clause is often used with the Group By clause to filter gropus bases on specific conditions, which is like WHERE clause. 

#### Limit clause
The limit clause is used to restrict the number of rows retrieved in the result of the query, which can make a certain number of the records on each page. 


### Practices
![](../pic/MySQL study notes/group%20practice1.jpg?raw=true)
![](../pic/MySQL study notes/group%20practice2.jpg?raw=true)

## Select from Muti-table (no suggest to use)
* SELECT * FROM table1, table2;
* The row number of muti-table is the row number of each table times each other. 
* The column number of muti-table is the column number of each table adds up together. 
* Use select projection to query. 
* Alias for the repeated column name of the multi-table, 
  `table1.columnname alias, table2.columnname alias;`
* Alias for table to make the process simplification.
  For example:
  SELECT
    students.id sid,
    students.name,
    students.gender,
    students.score,
    classes.id cid,
    classes.name cname
  FROM students, classes;
To simplify:
  SELECT
      s.id sid,
      s.name,
      s.gentder,
      s.score,
      c.id cid,
      c.name cname
  FROM students s, classes c;
  
### Select Multiple Tables with WHERE
Multi-table Selection with WHERE
For example:
![](../pic/MySQL study notes/multitable%20with%20WHERE.jpg?raw=true)

### Select Multiple Tables from a Database Connection 
When connecting to multiple tables, you can only select a single table as a principle table to be a ResultSet, and then select rows from other tables which have relationship to the principle table connecting to the ResultSet. 

#### INNER JOIN
The syntax is `INNER JOIN`, 
1. Set the principle table first. 
2. Set the table needs to be connected by using `INNER JOIN`.
3. Set the condition by using `ON <condition>`. 
   `s.class_id = c.id` means the column of `class_id` from students and the column of `id` from classes need to connect with the same column number. 
4. `WHERE` `ORDER BY` can be added then. 
`SELECT s.id, s.class_id, c.name, s.name, s.gender, s.score FROM students s INNER JOIN classes c ON s.class_id=c.id;
Note: Though, select the both tables, classes c should be put `INNER JOIN`. `
Means the table will be joined to connect to the table of students when the number of s.class_id and c_id are same. 
`INNER JOIN` is the most common used, and returns the data exist on the both tables.
`INNER JOIN` isn't necessary to use, because it's same with `WHERE` syntax.
`select * from tablea inner join tableb on a.id=b.id` = 'select * from talbea, tableb where a.id=b.id'

#### OUTER JOIN
`RIGHT OUTER JOIN` returns the data exists on the right table(the table be compared with). When the data exist on the right table only, the return string will be `NULL` to make up. 
`LEFT OUTER JOIN` returns the data exist on the left table(the original table). When the data exists on the left table only, the return string will be `NULL` to make up.
`FULL OUTER JOIN` returns the data exists on the both table. When the data exists on the left or the right table only, the return string will be `NULL` to make up.

## Maintain Data
Maintaining data includes CRUD, there are Creat, Retrieve, Update and Delete. 
* INSERT
* DELETE
* UPDATE
* REPLACE

**Value and values are available for mysql syntax.**  

### INSERT
INSERT syntax is `INSERT INTO <table name> (string1, string2,...) VALUES (value1, value2,...)`.
* The sequence of strings can be casual, but the sequence of values must be consistant with strings. 
* Execpt for number strings, the string must add single quotes.
* More than one records can be added by using comma to connect. 
  `INSERT INTO students (class_id, name, gender, score) VALUES
   (1, '五五', 'M', 90),
   (2, '六六', 'F', 80);`
   OR
   `INSERT INTO students values  
   (1, '五五', 'M', 90),
   (2, '六六', 'F', 80);`
* All columns except for ID will be included, or it reports an error that is "Field xxx doesn't have a default value".
* If the row exists:
	* A duplicate (no including ID) inserts, the record acts as a new record at the last row whatever it is a duplicate or there is difference.
	* A duplicate (including ID) inserts, an error reports that is "Duplicate entry "12" for key 'students PRIMARY'.  
	* A duplicate (including ID) inserts but there is an difference execept for id, an error reports that is "Duplicate entry "12" for key 'students PRIMARY'.
* If the row doesn't exist:
	* No including ID, the record acts as a new record as the last row.
	* Including ID, if the ID is a vacancy, insert the record into the vacancy, if not, insert the record at the last row. 

### Replace 
* Replace syntax is to replace all values of the row of the data. 
* Update has two kinds of syntax, one is to update part column of one row of the data, another is to update part column of muti rows of data. 

#### Insert or Replace  
* Use `REPLACE INTO <table name> (string1, string2,...) VALUES (value1, value2,...)`. 
* All columns except for ID will be included, or it reports an error that is "Field xxx doesn't have a default value".
* If the row exists:
	* Including ID, and if the ID exists, the record replaces the existed one.
	* No including ID REPLACE syntax acts as **INSERT** to insert a new record at the last row.
* If the row doesn't exists:
	* No including ID, REPLACE syntax acts as **INSERT** to insert a new record.
	* Including ID, REPLACE syntax acts as **REPLACE** to replace the existed one.
* For example, `REPLACE INTO test.students (id, class_id, name, gender, score) VALUES (9, 1, '小默', 'M', 98);`, the record allocates at 9 which there is a vacancy of 9 in the original table.  

#### Update or Insert (can update more than one values)
Use `INSERT INTO <table name> (string1, string2, ...) VALUES (value1, values2, ...) ON DUPLICATE KEY UPDATE value=1, value=2, value=3...; to solve repeatibility, and the updated strings would be defined in `UPDATE`. The syntax is same with the replace syntax .
For example, `INSERT INTO test.students(id, class_id, name, gender, score) VALUE (4, 2, '小黄', 'M', 98) ON DUPLICATE KEY UPDATE name='小黄', gender='M', score=98;` to replace the original record 4.`

* String and Values should be corresponding, and all columns except for ID will be included, or it reports an error that is "Field xxx doesn't have a default value".
* The modified values put in `on duplicate key update`.
* Update:
Including id and other columns, the syntax acts as replace to replace the original record. If no including one of other clumns, it reports an error: Field xxx doesn't have a default value.
* Insert:
No including id but including other columns, the syntax acts as insert to add the record at the last row, and id number is incremented sequentially by default.  If no including one of other clumns, it reports an error: Field xxx doesn't have a default value.
* To update one of colunms:
For example, `insert into students (id, class_id, name, gender, score) value (10, 2, 'kk', 'M', 60) on duplicate key update score=50;` to  update one of columns only.

#### Insert or Ignore
Use`INSERT IGNORE INTO <table name> (string1, string2, ...) VALUES (value1, value2, ...) to mean if the record exists to ignore it direactly. 

### Delete
The syntax is `DELETE FROM <table> WHERE...;`
* Similar with UPDATE syntax, DELETE can delete more than one rows by using WHERE. 
* If no any row matches the condition, no error code reports, only show "0 row(s) afftected." instead. 
* If no WHERE conditions, all row will be deleted.
* When using MySQL that's the real relationship databash, also will show the number of rows affected.
* If two rows of records would be deleted, use `OR` instead of `AND` in WHERE condition. If use `AND`, 0 row would be affected. 
* If more than two rows of records would be deleted, use `id> or id<`.

### UPDATE (can update only one value)

UPDATE syntax is `UPDATE <table name> SET <string1>=<value1>, <string2>=<value2>,... WHERE...;`
* The sequence of strings can be casual, but the sequence of values must be consistant with strings. 
* Execpt for number strings, the string must add single quotes.
* More than one rows of records can be updated. 
  For example, `UPDATE students SET score=100 WHERE id>=5 AND id<=7;`
* UPDATE could have no WHERE condition. 
  For example, `UPDATE students SET score=100;` means all scores will be changed to be 100.
* If no WHERE conditions, all rows will be updated.
**First use SELECT... WHERE to check if the records are you expected.**
* If no any row matches the condition, no error code reports, only show "0 row(s) afftected." instead. 

#### Expression to be Used 
For example, add 10 score for each person who's score is under 80. 
`UPDATE students SET score=score+10 WHERE score<80;`

## MySQL
* Besides of MySQL Server the real server of MySQL, there is MySQL Client that's a client to entry the command after logging in.
* `mysql` is the command for MySQL Client, and `mysqld` is the command for MySQL Server to be performed on the backend.

### Manage MySQL
* To manage MySQL by using the Workbench which is in a visulized way to select, create, update data, but that's a graphical client and operate MySQL through SQL syntax. So they are all clients to interact with MySQL by using SQL which is the only interface between. 
* Though MySQL can be managed by MySQL Workbench, it is only uses SQL commands when remote connection by SSH for many times.

### Database
* Actually, it can be created more than one database on a server performming MySQL. 
* To show all databases to use `SHOW DATABASES`.
* 'information_schema', 'mysql', 'performance_schema' and 'sys' are all system databases. Don't touch them. Others are databases created by users. 

#### Create Databases
* Use `CREATE DATABASE <database name>;`

#### Check Database Using on
* Use `SELECT DATABASE();`

#### Delete Databases
* Use `DROP DATABASE <database name>;`

#### Show Databases
* Use `SHOW databases;`

#### Switch Databases
* Use `USE <database name>;`

### Tables
#### Show All Tables within A Database
* Use `SHOW TABLES;`. 
**If use this command in workbench, switch the database you expect first by using `USE <databse>.**

#### Drop Table and Delete Table
* Drop Table <table name> means to delete the table with the table structure.
* Delete xx from <table name> where means to delete the table only with the table content.

#### Create Table
##### Snapshot
Snapshot from the original table to a created table.
* Use `CREATE TABLE <table name> SELECT * FROM <original table name> WHERE <condition>;`.
* The database structure of snapshot is same with the original one.  

##### Write Select Results from Other Tables
Connect with `INSERT` and `SELECT`to insert the selected result into a resigned table. 
For example, create the table of `students3` first, and then input the average score for each class. 
`CREATE TABLE students3 (id BIGINT NOT NULL AUTO_INCREMENT,
class_id BIGINT NOT NULL, 
average DOUBLE NOT NULL,
PRIMARY key(id));
`INSERT INTO students3 (class_id, average) SELECET class_id, AVG(score) FROM students GROUP BY class_id ORDER by AVG(score) ASC;`.
**no include id, because the string of id in students3 duplicates the string of id in students.**
* Only one column to insert
For example, 
`Insert into rt (id, name) select id, name from students4 where id=5;`.
Get the result:
|id | name |
|-|------|
| 5 | 小白|

#### Check Tables Structure
* Use `DESC <table name>;` = `describe <table name>`
  The results:
	*	Filed: Filed name
	*	Type: Data type
	*	Null: IS NULL and IS NOT NULL
	*	Key: Priciple key
	*	Default: Default value
	*	Extra: Extra attribute
* Or use `SHOW CREATE TABLE <table name>;`
* Data type
	* https://www.runoob.com/mysql/mysql-data-types.html
	* Check "init-test-data" for the common types of strings. 
	* Number type
	|Type name|Des.|Byte requirement|
	|-------|---|---|
	|FLOAT|a single precision 32 bit|4 bytes|
	|DOUBLE|a double precision 64 bit, doulbe storage stored in memory than FLOAT|8 bytes|

#### Alter Tables
##### Add Column
* Use `ALTER TABLE <table name> ADD COLUMN <column name> <data type> <NULL or NOT NULL>;`.
  For example, `ALTER TABLE students ADD COLUMN birth VARCHAR(10) NOT NULL;`.
	* VARCHAR is available to define strings with variable length, which is a common type of string data type. 
	* CHAR is available to define strings with unvariable length.
  **VARCHAR is required.**
  *  char 表示定长，长度固定，varchar表示变长，即长度可变。当所插入的字符串超出它们的长度时，视情况来处理，如果是严格模式，则会拒绝插入并提示错误信息，如果是宽松模式，则会截取然后插入。如果插入的字符串长度小于定义长度时，则会以不同的方式来处理，如char（10），表示存储的是10个字符，无论你插入的是多少，都是10个，如果少于10个，则用空格填满。而varchar（10），小于10个的话，则插入多少个字符就存多少个。 

##### Delete Column
* Use `ALTER TABLE <table name> DROP COLUMN <column name>;`

### Force Index
For example, 
`SELECT * FROM students FORCE INDEX (idx_class_id) WHERE class_id = 1 ORDER BY id DESC;`.

## Transactions
Database transctions means to execute multi secentences as one unit, in where, all SQL sentences would be executed together, that means if the first SQL sentence executed but the second one failed, and the all process would be cancelled together. 
* ACID:
	* Atomic: To perform in Atomic units, that is all perform or all are not performed.
	* Consistent: All data status are consistent.
	* Isolation: This transaction is isolation from other transaction.
	* Duration: The modified data should be persisted.
* One SQL sentence is performed as one transaction which is called implicit transaction. 
* Perform SQL sentences manually into one transaction which is called explicit transaction, in which the perform needs to use `BEING` to start a transaction and use `COMMIT` to submit a transaction.
* Use `ROLLBACK` to make the transaction undo. 
* For two concurrent transactions, when they execute the same record, maybe some problems occur, because there is inconsistance caused by the concurrent transactions, including Dirty Read, Non Repeatable Read, Phantom Read. So, database supplies the following isolation level to avoid from data inconsistance. 
	* Read Uncommitted
	* Read committed
	* Repeatable Read
	* Serializable
* End the transaction use `response. end`

### Read Uncommitted
It is the lowest isolation level, in which a transaction can read another transaction updates before committed. If another transaction rolls back, the transaction Dirty Read the data.
Practise:
Open two MYSQL clients, one is command client, another is workbench. 
to perform as the following steps:
![](../pic/MySQL study notes/read%20committed%20level.png?raw=true)

### Read Committed
The isolation level can read another transaction upates after committed. 
Open two MYSQL Clients, one is command cliend, another is workbench, to perform as the following steps:
![](../pic/MySQL study notes/read%20uncommitted%20level.png?raw=true)

### Repeatable Read
Under the repeatable read isolation level, a transaction may meet Phantom Read.
A phantom read means one record cann't be select when the first selection, but when update the unexisted record and select the same one record, it succeeds.

### Serializable
It is the most higest isolation level, no Dirty Read, Unrepeatable Read and Phantom read, and suggest not to use this isolation level. 

## Important notes
* The sequence of using the key word to select:
 from -> where -> group by-> having ->order by
* `on` follows with conditons concerning with the related table.
* `where` follows with conditions concerning with the primary table.
* `INNER JOIN`=`JOIN`.
* `NATURAL JOIN` uses only `where` instead of `on`.

## Common Command Lines
### Check Constraint Foreign Keys
Use `show create table <table name>` to check the structure of the table including constratint foreign key.

### Delete Constraint Foreign Keys
Use 'alter table <table name> drop foreign key <constraint name>;'

### Unequal to 
Use `!=`

### Include with 
Use `like`
For exmaple, to find out someone with the name begining with "S", "A" or "B".
`select * from emp where ename like "A" or ename like "B" or ename like "S";`
`select * from emp where ename like 'A' or ename like 'B' or ename like 'S';`
**Double quotation marks or single quotation marks are available. **
Use `not like' to mean doesn't include something.

### Ordering more than one condistions
Use comma to connect more than one orderring conditions.
For example, to select informatoin in ascending name order and in descending salary order. 
`select * from ename order by ename desc, sal asc;`

### Distinct
`DISTINCT` clause is used to remove duplicate records from the table and fetch only the unique records.
**The DISTINCT clause is only used with the SELECT statement.**

## Mysql functions
### RANk() function
The RANK() function displays the rank of a row. This rank of a row is defined within its partition, and this rank has gaps in-between. 
#### Syntax
* The RANK() function is used along with the 'over' clause, 'partition by' clause, and 'order by' clause. 
* The 'partition by' clause is optional, when the RANK() function can be performed on the small set of the result, in this case, the 'partition by' clause is a must. 
* The syntax is as follows:
> Select column_name, 
> RANK() over (
> PARTITION BY {expression}[{,expression}]
> ORDER BY {expression} [ASC|DESC]) [{,expression}]
> ) from table_name;
* PARTITION BY {expression}-this part of the query does the partiton according to the expression provided in the clause. 
  
### DENSE_RANK() function
* Compare with the RANK() function, the DENSE_RANK() function to understand the ranking without gaps.

#### Syntax
The syntax of the DENSE_RANK() is same with the RANK() function.

### ROW_NUMBER() function 
The ROW_NUMBER() function is a function that returns a number for each row in sequence or serial, begining from 1. 
#### Syntax
> row_number() over (order by {expression} [ASC|DESC], [{,expression}]);

### Concat function （多个字段拼接）
The Concat function is used when dealing with string in a database that can be in any format, colmn values, variables or literal values in the string that helps to append two or more such string values to each other to ceate a new string value. 
























