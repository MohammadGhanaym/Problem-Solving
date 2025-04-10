# LeetCode SQL 50

<li><a href="#Recyclable_and_Low_Fat_Products">Recyclable_and_Low_Fat_Products</a></li>
<li><a href="#Find_Customer_Referee">Find_Customer_Referee</a></li>
<li><a href="#Big_Countries">Big_Countries</a></li>
<li><a href="#Article_Views_I">Article_Views_I</a></li>
<li><a href="#Invalid_Tweets">Invalid_Tweets</a></li>
<li><a href="#Replace_Employee_ID_With_The_Unique_Identifier">Replace_Employee_ID_With_The_Unique_Identifier</a></li>
<li><a href="#Product_Sales_Analysis_I">Product_Sales_Analysis_I</a></li>
<li><a href="#Customer_Who_Visited_but_Did_Not_Make_Any_Transactions">Customer_Who_Visited_but_Did_Not_Make_Any_Transactions</a></li>
<li><a href="#Rising_Temperature">Rising_Temperature</a></li>
<li><a href="#Average_Time_of_Process_per_Machine">Average_Time_of_Process_per_Machine</a></li>
<li><a href="#Write_Here">Write_Here</a></li>
<li><a href="#Write_Here">Write_Here</a></li>
<li><a href="#Write_Here">Write_Here</a></li>
<li><a href="#Write_Here">Write_Here</a></li>
<li><a href="#Write_Here">Write_Here</a></li>
<li><a href="#Write_Here">Write_Here</a></li>
<li><a href="#Write_Here">Write_Here</a></li>
<li><a href="#Write_Here">Write_Here</a></li>
<li><a href="#Write_Here">Write_Here</a></li>
<li><a href="#Write_Here">Write_Here</a></li>
<li><a href="#Write_Here">Write_Here</a></li>
<li><a href="#Write_Here">Write_Here</a></li>
<li><a href="#Write_Here">Write_Here</a></li>
<li><a href="#Write_Here">Write_Here</a></li>
<li><a href="#Write_Here">Write_Here</a></li>
<li><a href="#Write_Here">Write_Here</a></li>
<li><a href="#Write_Here">Write_Here</a></li>
<li><a href="#Write_Here">Write_Here</a></li>
<li><a href="#Write_Here">Write_Here</a></li>


```python
input().replace(' ', '_')
```

     Average Time of Process per Machine
    




    'Average_Time_of_Process_per_Machine'



<a id='Recyclable_and_Low_Fat_Products'></a>
# Recyclable_and_Low_Fat_Products

```sql
/* Write your T-SQL query statement below */
SELECT product_id
FROM Products
WHERE low_fats = 'Y' AND recyclable = 'Y'
```

<a id='Find_Customer_Referee'></a>
# Find_Customer_Referee

```sql
/* Write your T-SQL query statement below */
SELECT name
FROM Customer
WHERE referee_id != 2 OR referee_id IS NULL
```

<a id='Big_Countries'></a>
# Big_Countries

```sql
/* Write your T-SQL query statement below */
SELECT name, population, area
FROM World
WHERE area >= 3000000 OR population >= 25000000
```

<a id='Article_Views_I'></a>
# Article_Views_I

```sql
/* Write your T-SQL query statement below */
SELECT DISTINCT author_id AS id
FROM Views
WHERE author_id = viewer_id
ORDER BY id 
```

<a id='Invalid_Tweets'></a>
# Invalid_Tweets

```sql
/* Write your T-SQL query statement below */
SELECT tweet_id
FROM Tweets
WHERE LEN(content) > 15
```

<a id='Replace_Employee_ID_With_The_Unique_Identifier'></a>
# Replace_Employee_ID_With_The_Unique_Identifier

```sql
SELECT unique_id, name
FROM Employees e
LEFT JOIN EmployeeUNI eUNI
ON e.id = eUNI.id
```

<a id='Product_Sales_Analysis_I'></a>
# Product_Sales_Analysis_I

```sql
/* Write your T-SQL query statement below */
SELECT product_name, year, price
FROM Sales s
INNER JOIN Product p
ON s.product_id = p.product_id
```

<a id='Customer_Who_Visited_but_Did_Not_Make_Any_Transactions'></a>
# Customer_Who_Visited_but_Did_Not_Make_Any_Transactions

```sql
/* Write your T-SQL query statement below */
SELECT customer_id, COUNT(*) AS count_no_trans
FROM Visits v
LEFT JOIN Transactions t
ON v.visit_id = t.visit_id
WHERE t.visit_id IS NULL
GROUP BY customer_id
```

<a id='Rising_Temperature'></a>
# Rising_Temperature

```sql
/* Write your T-SQL query statement below */
SELECT w1.id
FROM Weather w1
CROSS JOIN Weather w2
WHERE w1.temperature > w2.temperature AND DATEDIFF(DAY, w2.recordDate, w1.recordDate) = 1
```

```sql
/* Write your T-SQL query statement below */
SELECT id
FROM (SELECT id, recordDate, temperature, LAG(temperature) OVER(ORDER BY recordDate) AS pre_temp,
      LAG(recordDate) OVER(ORDER BY recordDate) AS pre_date
FROM Weather) t2
WHERE temperature > pre_temp AND DATEDIFF(DAY, pre_date, recordDate) = 1

```

<a id='Average_Time_of_Process_per_Machine'></a>
# Average_Time_of_Process_per_Machine

```sql
/* Write your T-SQL query statement below */
SELECT a1.machine_id, ROUND(AVG(a2.timestamp - a1.timestamp), 3) AS processing_time
FROM Activity a1
CROSS JOIN Activity a2
WHERE a1.machine_id = a2.machine_id 
      AND a1.process_id = a2.process_id 
      AND a1.activity_type = 'start'
      AND a2.activity_type = 'end'
GROUP BY a1.machine_id
```


```python
<a id='Refer_to'></a>
# Refer_to
```


```python
```sql

```
```


```python
<a id='Refer_to'></a>
# Refer_to
```


```python
```sql

```
```


```python
<a id='Refer_to'></a>
# Refer_to
```


```python
```sql

```
```


```python
<a id='Refer_to'></a>
# Refer_to
```


```python
```sql

```
```


```python
<a id='Refer_to'></a>
# Refer_to
```


```python
```sql

```
```


```python
<a id='Refer_to'></a>
# Refer_to
```


```python
```sql

```
```


```python
<a id='Refer_to'></a>
# Refer_to
```


```python
```sql

```
```
