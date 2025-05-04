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
<li><a href="#Employee_Bonus">Employee_Bonus</a></li>
<li><a href="#Students_and_Examinations">Students_and_Examinations</a></li>
<li><a href="#Managers_with_at_Least_5_Direct_Reports">Managers_with_at_Least_5_Direct_Reports</a></li>
<li><a href="#Confirmation_Rate">Confirmation_Rate</a></li>
<li><a href="#Not_Boring_Movies">Not_Boring_Movies</a></li>
<li><a href="#Average_Selling_Price">Average_Selling_Price</a></li>
<li><a href="#Project_Employees_I">Project_Employees_I</a></li>
<li><a href="#Percentage_of_Users_Attended_a_Contest">Percentage_of_Users_Attended_a_Contest</a></li>
<li><a href="#Queries_Quality_and_Percentage">Queries_Quality_and_Percentage</a></li>
<li><a href="#Monthly_Transactions_I">Monthly_Transactions_I</a></li>
<li><a href="#Immediate_Food_Delivery_II">Immediate_Food_Delivery_II</a></li>
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

     Immediate Food Delivery II
    




    'Immediate_Food_Delivery_II'



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

<a id='Employee_Bonus'></a>
# Employee_Bonus

```sql
/* Write your T-SQL query statement below */
SELECT name, bonus
FROM Employee e
LEFT JOIN Bonus s
ON e.empId = s.empId
WHERE bonus < 1000 OR bonus IS NULL
```

<a id='Students_and_Examinations'></a>
# Students_and_Examinations

```sql
/* Write your T-SQL query statement below */
SELECT Distinct s.student_id, s.student_name, sub.subject_name, COUNT(e.student_id) AS attended_exams
FROM Students s
CROSS JOIN Subjects sub
LEFT JOIN Examinations e
ON e.student_id = s.student_id AND e.subject_name = sub.subject_name
GROUP BY s.student_id, s.student_name, sub.subject_name

```

<a id='Managers_with_at_Least_5_Direct_Reports'></a>
# Managers_with_at_Least_5_Direct_Reports

```sql
/* Write your T-SQL query statement below */
SELECT m.name
FROM Employee AS e
INNER JOIN Employee AS m ON e.managerId = m.id
GROUP BY m.id, m.name
HAVING COUNT(e.managerId) >= 5;
```

```sql
SELECT name
FROM (SELECT mang.managerId, COUNT(mang.managerId) AS n_reports
        FROM Employee mang
        GROUP BY mang.managerId
        HAVING COUNT(mang.managerId) >= 5) t1
INNER JOIN Employee e
ON t1.managerId = e.id
```

<a id='Confirmation_Rate'></a>
# Confirmation_Rate

```sql
/* Write your T-SQL query statement below */
SELECT s.user_id, ROUND(AVG(CASE WHEN c.action = 'confirmed' THEN 1.0 ELSE 0.0 END), 2) AS confirmation_rate
FROM Signups s
LEFT JOIN Confirmations c
ON s.user_id = c.user_id
GROUP BY s.user_id
```

<a id='Not_Boring_Movies'></a>
# Not_Boring_Movies

```sql
/* Write your T-SQL query statement below */
SELECT id, movie, description, rating
FROM Cinema
WHERE id % 2 != 0 AND description != 'boring'
ORDER BY rating DESC
```

<a id='Average_Selling_Price'></a>
# Average_Selling_Price

```sql
/* Write your T-SQL query statement below */
SELECT p.product_id, ISNULL(ROUND(SUM(p.price * u.units) / CAST(SUM(u.units) AS FLOAT), 2), 0) AS average_price
FROM Prices p
LEFT JOIN UnitsSold u
ON p.product_id = u.product_id AND u.purchase_date BETWEEN p.start_date AND p.end_date
GROUP BY p.product_id
```

<a id='Project_Employees_I'></a>
# Project_Employees_I

```sql
/* Write your T-SQL query statement below */
SELECT project_id, ROUND(AVG(CAST(experience_years AS DECIMAL)), 2) average_years
FROM Project p
LEFT JOIN Employee e
ON p.employee_id = e.employee_id
GROUP BY project_id

```

<a id='Percentage_of_Users_Attended_a_Contest'></a>
# Percentage_of_Users_Attended_a_Contest

```sql
/* Write your T-SQL query statement below */    
SELECT r.contest_id, 
       ROUND(100.0 * COUNT(DISTINCT r.user_id) / (SELECT COUNT(*) FROM Users), 2) AS percentage
FROM Register r
GROUP BY r.contest_id
ORDER BY percentage DESC, contest_id;
```

<a id='Queries_Quality_and_Percentage'></a>
# Queries_Quality_and_Percentage

```sql
/* Write your T-SQL query statement below */
SELECT 
    query_name, 
    ROUND(AVG(1.0 * rating / position), 2) AS quality, 
    ROUND(AVG(CASE WHEN rating < 3 THEN 1.0 ELSE 0.0 END) * 100, 2) AS poor_query_percentage
FROM Queries
GROUP BY query_name
```

<a id='Monthly_Transactions_I'></a>
# Monthly_Transactions_I

```sql
/* Write your T-SQL query statement below */
SELECT 
    FORMAT(trans_date, 'yyyy-MM') AS month, 
    country, 
    COUNT(id) AS trans_count, 
    SUM(CASE WHEN state = 'approved' THEN 1 ELSE 0 END) AS approved_count,
    SUM(amount) AS trans_total_amount,
    SUM(CASE WHEN state = 'approved' THEN amount ELSE 0 END) AS approved_total_amount
FROM Transactions
GROUP BY FORMAT(trans_date, 'yyyy-MM'), country
```

<a id='Immediate_Food_Delivery_II'></a>
# Immediate_Food_Delivery_II

```sql
/* Write your T-SQL query statement below */
SELECT 
    ROUND(AVG(CASE WHEN d1.order_date = d1.customer_pref_delivery_date THEN 1.0 ELSE 0.0 END) * 100, 2) AS immediate_percentage
FROM Delivery d1
INNER JOIN (SELECT customer_id, MIN(order_date) AS first_order
            FROM Delivery
            GROUP BY customer_id) d2
ON d1.customer_id = d2.customer_id AND d1.order_date = d2.first_order
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
