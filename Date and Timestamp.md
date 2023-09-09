## Exercise:

##### Question: Get me all the employees above 60, use the appropriate date functions

```python
SELECT AGE(birth_date) FROM employees
WHEREWHERE (
            EXTRACT (YEAR FROM AGE(birth_date))
) > 60;
```
-- alternative
```python
SELECT COUNT(emp no) FROM employees
WHERE birth_date NOW() - intervel '61'years; 
```



##### Question: How many employees where hired in February?


```python
SELECT COUNT(emp no) FROM employees
WHERE EXTRECT(MONTH FROM hire_date) = 2;
```



##### Question: How many employees were born in november?


```python
SELECT COUNT(emp no) FROM employees
WHERE EXTRACT(MONTH FROM birth_date) = 11;
```


##### Question: Who is the oldest employee? (Use the analytical function MAX)


```python
SELECT AGE(birth_date) FROM employees;
```


##### Question: How many orders were made in January 2004?


```python
SELECT COUNT(orderID) FROM orders
WHERE DATE_TRUNC('MONTH',order_date) = date '2004-01-01';
```