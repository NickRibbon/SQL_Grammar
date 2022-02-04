## SQL IN 操作符
### IN 操作符

IN 操作符允许我们在 WHERE 子句中规定多个值。

### SQL IN 语法

> SELECT column_name(s)
> FROM table_name
> WHERE column_name IN (value1,value2,...)

### 原始的表 (在实例中使用：)

Persons 表:

| Id | 	LastName |	FirstName |	Address |	City |
| --------:   | :-----:  | :----:  |:----:  |----:  |
| 1	| Adams	| John	| Oxford | Street	| London |
| 2	| Bush	| George	| Fifth | Avenue	| New York |
| 3	| Carter |Thomas	| Changan | Street	| Beijing |

### IN 操作符实例
现在，我们希望从上表中选取姓氏为 Adams 和 Carter 的人：

我们可以使用下面的 SELECT 语句：
> SELECT * FROM Persons
> WHERE LastName IN ('Adams','Carter')

### 结果集：

| Id | 	LastName |	FirstName |	Address |	City |
| --------:   | :-----:  | :----:  |:----:  |----:  |
| 1 |	Adams	| John | Oxford | Street | London |
| 3	| Carter |Thomas	| Changan | Street	| Beijing |
