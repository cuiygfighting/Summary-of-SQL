# Summary-of-MySql

```c++
*******************************************************************
Copyright(c) 2020, Alex Tsui
All rights reserved.

Distributed under the BSD license.
(See accompanying file LICENSE.txt at
https://github.com/cuiygfighting 
*******************************************************************

//==================================================================
// 《数据库知识总结》
// 作者：崔玉贵
//email:cuiyg@pku.edu.cn
//==================================================================
```

## SQL常用语法

### SELECT

select用于从一个或多个表(视图)中检索数据

```c++
SELECT columnname,...
FROM tablename,...
[WHERE ...]
[UNION ...]
[GROUP BY ...]
[HAVING ...]
[ORDER BY ...];
```

### INSERT

INSERT给表增加一行

```
INSERT INTO tablename [(columns, ...)]
VALUE(values, ...)

//INSERT SELECT插入SELECT的结果到一个表
INSERT INTO tablename [(columns, ...)]
SELECT columns, ... FROM tablename, ...
[WHERE ...];
```

### UPDATE

UPDATE更新表中一行或多行

```
UPDATE tablename
SET column=value,...
[WHERE ...];
```

### DELETE

DELETE从表中删除一行或多行

```
DELETE FROM tablename
[WHERE ...];
```

### CREATE

```
//CREATE TABLE用于创建新数据库表
CREATE TABLE tablename
{
columnname1 datatype [NULL|NOT NULL] [CONSTRAINTS],
columnname2 datatype [NULL|NOT NULL] [CONSTRAINTS],
...
};

//CREATE INDEX用于在一个或多个列上创建索引
CREATE INDEX indexname
ON tablename(column [ASC|DESC],...);

//CREATE PROCEDURE用于创建存储过程
CREATE PROCEDURE procedurename([parameters])
BEGIN
...
END;

//CREATE USER用于向系统中添加新的用户账号
CREATE USER username[@hostname]
[IDENTIFIED BY [PASSWORD]'password'];

//CREATE VIEW用来创建一个或多个表上的新视图
CREATE [OR REPLACE] VIEW viewname
AS
SELETE ...;
```

