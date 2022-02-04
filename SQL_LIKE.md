# SQL LIKE 操作符
### LIKE 操作符用于在 WHERE 子句中搜索列中的指定模式。
## LIKE 操作符
LIKE 操作符用于在 WHERE 子句中搜索列中的指定模式。
### SQL LIKE 操作符语法
> SELECT column_name(s)
> FROM table_name
> WHERE column_name LIKE pattern
## 原始的表 (用在例子中的)：
Persons 表:

| Id | 	LastName |	FirstName |	Address |	City |
| --------:   | :-----:  | :----:  |:----:  |----:  |
| 1	| Adams	| John	| Oxford | Street	| London |
| 2	| Bush	| George	| Fifth | Avenue	| New York |
| 3	| Carter |Thomas	| Changan | Street	| Beijing |

## LIKE 操作符实例

### 例子 1
现在，我们希望从上面的 **"Persons"** 表中选取居住在以 "N" 开始的城市里的人：

我们可以使用下面的 **SELECT** 语句：

> SELECT * FROM Persons
> WHERE City LIKE 'N%'

<font color=orange size=5>提示</font>："%" 可用于定义通配符（模式中缺少的字母）。
### 结果集：
| Id | 	LastName |	FirstName |	Address |	City |
| --------:   | :-----:  | :----:  |:----:  |----:  |
| 2 |	Bush |	George |	Fifth | Avenue |	New | York |

### 例子 2
接下来，我们希望从 **"Persons"** 表中选取居住在以 **"g"** 结尾的城市里的人：

我们可以使用下面的 **SELECT** 语句：

> SELECT * FROM Persons
> WHERE City LIKE '%g'

### 结果集：
| Id | 	LastName |	FirstName |	Address |	City |
| --------:   | :-----:  | :----:  |:----:  |----:  | 
| 3 |	Carter | Thomas |	Changan | Street	| Beijing |

### 例子 3
接下来，我们希望从 **"Persons"** 表中选取居住在包含 **"lon"** 的城市里的人：

我们可以使用下面的 **SELECT** 语句：
> SELECT * FROM Persons
> WHERE City LIKE '%lon%'
### 结果集：
| Id | 	LastName |	FirstName |	Address |	City |
| --------:   | :-----:  | :----:  |:----:  |----:  |
| 1 |	Adams	| John | Oxford | Street | London |

### 例子 4
通过使用 NOT 关键字，我们可以从 **"Persons"** 表中选取居住在不包含 **"lon"** 的城市里的人：

我们可以使用下面的 **SELECT** 语句：
> SELECT * FROM Persons
> WHERE City NOT LIKE '%lon%'
### 结果集：
| Id | 	LastName |	FirstName |	Address |	City |
| --------:   | :-----:  | :----:  |:----:  |----:  |
| 2	| Bush	| George	| Fifth | Avenue	| New York |
| 3	| Carter |Thomas	| Changan | Street	| Beijing |


