### ----------SELECT-----------------
**选取单列**  
SELECT prod_name
FROM products;  

**选取多列**  
SELECT prod_id, prod_name, prod_price  
FROM products;

**检索所有列**  
SELECT *   
FROM products;  

### ----------DISTINCT----------------
**返回唯一值**
SELECT DISTINCT vend_id  
FROM products;

### ----------LIMIT-------------------
**限制结果**  
1)只返回5行  
SELECT prod_name  
FROM products  
LIMIT 5;

2)返回下一个5行  
SELECT prod_name  
FROM products  
LIMIT 5, 5;  

LIMIT 5, 5表示从行5开始的5行  
等价于LIMIT 5 **OFFSET** 5  

**在行数不够时，只返回它能返回的那么多行**  
