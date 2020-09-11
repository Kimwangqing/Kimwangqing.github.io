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

## Relationship Model (关系模型)
* Each row calls Record（记录）.
* Each column calls Column(字段：整型、浮点型、字符串、日期等).
In relationship model, the relation is maintained by primary keys and foreign keys (主键和外键). 

### Primary Keys
The Column can seperate two Records(they are same execpt one Column(字段) ) called a primary key(主键).
Better not to **modify the primary key** when it inserted into the form. Because a primary key is the only key to locate the record.

#### Principle
**The principle of selecting the primary key is**
* Do not use the key relating to any business Colume.Because the business key is easy to change as to scenarios. 
* Do not use NULL.
The Column without relating with business is defined as id", the following types of id are common used:
* BIGINT 自增整数类型  
* 全局唯一 GUID 类型

#### Associate Keys (联合主键)
Two or more than two columns are allowed to be set as primary keys called associate keys. 

### Foreign Keys (外键)
The key associating to another form is called foreign keys. 
![](https://github.com/Kimwangqing/pictures/blob/master/foreign%20key.jpg?raw=true)

### 