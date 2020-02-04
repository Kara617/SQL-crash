### --------- ORDER BY -------------------
**排序使用ORDER BY语句**  

### 单列排序   
SELECT prod_name  
FROM products  
ORDER BY prod_name;  

### 多列排序  
SELECT prod_id, prod_price, prod_name  
FROM products  
ORDER BY prod_price, prod_name;  

### 指定排序方向DESC  
SELECT prod_id, prod_price, prod_name  
FROM products  
ORDER BY prod_price DESC;  

SELECT prod_id, prod_price, prod_name  
FROM products  
ORDER BY prod_price DESC, prod_name;  

### ------------ WHERE ------------------  

SELECT prod_name, prod_price  
FROM products  
WHERE prod_price = 2.50;  

**WHERE子句操作符号**  
小于< 大于>  

| 操作符        | 说明           | 
| ------------- |:-------------: | 
| =             | 等于           |  
| <>            | 不等于         |  
| !=            | 不等于         |    
| BETWEEN       | 在指定两个值之间|    

SELECT vend_id, prod_name  
FROM products  
WHERE vend_id <> 1003; 

SELECT prod_name, prod_price  
FROM products  
WHERE prod_price BETWEEN 5 AND 10;  

### ----------------IS NULL----------------  
SELECT prod_name  
FROM products  
WHERE prod_name IS NULL  
