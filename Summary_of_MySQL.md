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