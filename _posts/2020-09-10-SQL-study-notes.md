---
layout: post
title: "SQL Study Notes "
date: 2020-09-10
excerpt: "SQL Study Notes"
tags: [sample post, images, test]
comments: true
mermaid: true
feature: /assets/img/SQL.jpg
---

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

## Relationship Model (关系模型)
* Each row calls Record（记录）.
* Each column calls Column(字段：整型、浮点型、字符串、日期等).
In relationship model, the relation is maintained by primary keys and foreign keys (主键和外键). 

### Primary Key
One Column  seperates two Records(they are same execpt one Column(字段) ) called a primary key(主键).
Better not to **change the primary key** when it inserted into the form. Because the primary key is only the Column to locate(确定) the record.

#### Principle
**The principle of selecting the primary key is**
* A primary key column doesn't relate to business. Because business is easy to be changed as to scenarios. These keys, such as ID, phone number and email address, which seems that they have unique properties, actually, they will be changed as to scenarios, cannot be assigned as primary keys.
* A primary key column cannot contain `NULL` value.
* A primary key is always defined as “id", the most common types are: 
	* BIGINT 自增整数类型 Data base will alocate one BIGINT when inserting data, which cannot be created in advance, and we don't wary the primary key will be repeated. This type of id can meet requirements for most applications. gi 
	* 全局唯一 GUID 类型

#### Composite Keys (联合主键)
Two or more than two columns are allowed to be set as primary keys called Composite Keys (**Try not to use associate keys**).

### Foreign Key (外键)
The Column associating to another form is called a foreign key. 
![](https://github.com/Kimwangqing/pictures/blob/master/foreign%20key.jpg?raw=true)

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
> `ALTER TALBE` students
> `ADD INDEX` index_name_score (name, score).
* If the more different about the column values, the higher inquery efficiency of the index.
* The index is senseless if the column values are same mostly, such as the value of gender.
* More than one index can be created in one table, but they make the speed slow down when the table inserts, deletes, updates records meanwhile the index should be modified simutaneously. 
* The relationship database creates the index to the primary key automatically. The efficiency is the highest to use the primary key index. 
#### Unique Index and Primary Key
**A column containing unique values, such as an identity ID and a mobile number which relates to business, cannot be defined as a primary key, but it can be added a unique index to make sure the uniqueness.**
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
![](https://github.com/Kimwangqing/pictures/blob/master/init-test-data.jpg?raw=true)
*  (To fix mess data)
    ![](https://github.com/Kimwangqing/pictures/blob/master/variable%20value.jpg?raw=true)
  * Use `show variables like 'char%'` (单引号） to check the variable value. 
  	* The source script use `CHARSET=utf8` 
  	* Find the inconsistance between `character_set_client | gbk` and ` character_set_server | utf8mb4`
  	* Run `set character_set_client = utf8` &  `set character_set_server = utf8` to make them consistant.
  	* Run `source d:\init-test-data;` to import the database again.
  	* Run `SELECT * FROM students`, and then the misdata is fixed. 
    ![](https://github.com/Kimwangqing/pictures/blob/master/fixinconsistance.jpg?raw=true)
    
## Query Data
* Query language: `SELECT * FROM <the name of the table>
	* `SELECT` means will perform a query.
	*  `*` means all columns.
	*  `FROM` means which table to be checked. 
	* `...`  means the name of the table.
	*  `SELECT` can perform calculation
       perform `select 100+200`
       get result `300`
   * Perform `SELECT 1` to check if the data base has been collected. 

## Query Conditions
* Run `SELECT * FROM <name of the talbe> WHERE <condition>`
  For example, `SELECT * FROM students WHERE score >= 80;`

### Query Conditions - AND
* Use `AND` to connect conditions.
  For example, `SELECT * FROM students WHERE score >= 80 AND gender = `M`; (the both is okay to use single quotes or not)

### Query conditions - OR
* TO select either condition A or condition B. 

### Query Conditions - NOT 
For example,  
`SELECT * FROM students WHERE score >= '80' AND NOT class_id = '2';`
(AND OR can use together.)
* `NOT class_id = 2` same as `class_id <> 2`, so `NOT` format is not often be used. 
`SELECT * FROM students WHERE score >= 80 AND class_id <> 2;`

### Query Conditions - ()
For example, `SELECT * FROM students WHERE (score < 80 OR score > 90) AND gender = 'M';`

### Query Conditions - Priority
If don't use brackets (), consitions to be performed by the priority from `NOT`, `AND` to `OR`, but the brackets () can break the priority. 

### Query Conditions - LIKE
`LIKE` means similarity. For example, `name LIKE 'ab%'`, `%` means any character. 

### Practice
![](https://github.com/Kimwangqing/pictures/blob/master/query-practice.jpg?raw=true)

## Query Projections
* Use query projections to select specified column. 
* Use comma to seleprate each column query. 
  For example, `SELECT id, score, name FROM students;`

### Give Another Name to Column
  *  Give another name to the column by putting another name besides of the original one. 
  For example, `SELECT id, score points, name FROM students;` `points` is the alias of score. 
  
### Query Projections with WHERE conditions
Query projections can combine with WHERE conditions to perfom complex query. 
For example, `SELECT id, score, name FROM students WHERE gender = 'M';

## Query Order
* Query results in an order of  by default. 
* Use `ORDER BY` to sort in other conditions. 
  For example, `SELECT id FROM students ORFER BY score;`
  
### Descending Order
* Query results in a reverse order by using `ORDER BY ... DESC. 

### Ascending Order
* Query results in a normal order by using `ORDER BY ... ASC`, which is same with `ORDER BY ...`.
* If same data occourred, to order them by adding column name. 
  For example, `SELECT id, name, gender score FROM students ORDER BY score DESC;` 
  ![](https://github.com/Kimwangqing/pictures/blob/master/score%20order%20without%20gender.jpg?raw=true)
  (Male is prior to Female by default.)
  ![](https://github.com/Kimwangqing/pictures/blob/master/score%20order%20with%20gender.jpg?raw=true)
  (Female is prior to Male by adding gentder column.)

### ORDER BY with WHERE
* Put `ORDER BY` behind of `WHERE`. 