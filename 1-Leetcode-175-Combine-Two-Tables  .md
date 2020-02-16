# Leetcode 175: Combine Two Tables  

**表1: Person**  

| 列名         | 类型     |
--------------|------------
| **PersonId**| int       |
| FirstName   | varchar   |
| LastName    | varchar   |

PersonId 是上表主键  

**表2: Address**  

| 列名         | 类型     |
---------------|----------
| **AddressId**| int     |
| PersonId     | int     |
| City         | varchar |
| State        | varchar |

AddressId 是上表主键
 

编写一个 SQL 查询，满足条件：无论 person 是否有地址信息，都需要基于上述两表提供 person 的以下信息：
FirstName, LastName, City, State

来源：力扣（LeetCode）  
链接：<https://leetcode-cn.com/problems/combine-two-tables>

## Solution  
```mysql
SELECT FirstName, LastName, City, State  
FROM Person LEFT JOIN Address
ON Person.PersonId = Address.PersonId;
```  

## Relational Database  

An application that supports data stored across multiple related tables.  
In a relation model, **each table typically holds data on one entity**.  
**Each row** in the table _**described one of those entities**_.  

> The concept of relational databases came from the British computer
scientist Edgar F. Codd. While working for IBM in 1970, he published a paper called _**A Relational Model of Data for Large Shared Data Banks**_.  

**Using Relational model, you can**:   
1. build tables that eliminate dupicate data;  
2. easy to maintain and provide for queries to get just the data you want.  



## Linking Tables Using JOIN  

To **connect tables in a query**, we use a `JOIN ... ON` statement.  

The syntax takes this form:  
```mysql
SELECT *
FROM table_a JOIN table_b
ON table_a.key_column = table_b.foreign_key_column
```

Matching based on **equality** between values is the **most common** use of the ON clause, 
but you can use **any _Boolean_ results** _true_ or _false_.  

For example,  
```mysql
ON table_a.key_column >= table_b.foreign_key_column  
```  


## Relating Tables with Key Columns  

**Problem**:  


