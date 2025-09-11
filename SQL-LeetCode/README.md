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
<li><a href="#Game_Play_Analysis_IV">Game_Play_Analysis_IV</a></li>
<li><a href="#Number_of_Unique_Subjects_Taught_by_Each_Teacher">Number_of_Unique_Subjects_Taught_by_Each_Teacher</a></li>
<li><a href="#User_Activity_for_the_Past_30_Days_I">User_Activity_for_the_Past_30_Days_I</a></li>
<li><a href="#Classes_With_at_Least_5_Students">Classes_With_at_Least_5_Students</a></li>
<li><a href="#Biggest_Single_Number">Biggest_Single_Number</a></li>
<li><a href="#Customers_Who_Bought_All_Products">Customers_Who_Bought_All_Products</a></li>
<li><a href="#The_Number_of_Employees_Which_Report_to_Each_Employee">The_Number_of_Employees_Which_Report_to_Each_Employee</a></li>
<li><a href="#Primary_Department_for_Each_Employee">Primary_Department_for_Each_Employee</a></li>
<li><a href="#Triangle_Judgement">Triangle_Judgement</a></li>
<li><a href="#Consecutive_Numbers">Consecutive_Numbers</a></li>
<li><a href="#Product_Price_at_a_Given_Date">Product_Price_at_a_Given_Date</a></li>
<li><a href="#Last_Person_to_Fit_in_the_Bus">Last_Person_to_Fit_in_the_Bus</a></li>
<li><a href="#Count_Salary_Categories">Count_Salary_Categories</a></li>
<li><a href="#Write_Here">Write_Here</a></li>
<li><a href="#Write_Here">Write_Here</a></li>
<li><a href="#Write_Here">Write_Here</a></li>


```python
input().replace(' ', '_')
```

     Count Salary Categories
    




    'Count_Salary_Categories'



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

<a id='Game_Play_Analysis_IV'></a>
# Game_Play_Analysis_IV

```sql
/* Write your T-SQL query statement below */
SELECT 
    ROUND(
        SUM(
        CASE WHEN DATEDIFF(DAY, a2.first_date, a1.event_date) = 1 
        THEN 1.0 ELSE 0.0 END
            ) / COUNT(DISTINCT a1.player_id),
        2) AS fraction
FROM Activity a1
INNER JOIN (SELECT player_id, MIN(event_date) first_date
            FROM Activity
            GROUP BY player_id) a2
ON a1.player_id = a2.player_id
```

<a id='Number_of_Unique_Subjects_Taught_by_Each_Teacher'></a>
# Number_of_Unique_Subjects_Taught_by_Each_Teacher

```sql
/* Write your T-SQL query statement below */
SELECT teacher_id, COUNT(DISTINCT subject_id) cnt
FROM Teacher
GROUP BY teacher_id
```

<a id='User_Activity_for_the_Past_30_Days_I'></a>
# User_Activity_for_the_Past_30_Days_I

```sql
/* Write your T-SQL query statement below */
SELECT activity_date day, COUNT(DISTINCT user_id) active_users
FROM Activity
WHERE activity_date > DATEADD(DAY, -30, '2019-07-27') 
AND activity_date <= '2019-07-27'
GROUP BY activity_date

```

<a id='Product Sales Analysis III'></a>
# Product Sales Analysis III

```sql
/* Write your T-SQL query statement below */
SELECT S.product_id, T.first_year, S.quantity, S.price
FROM Sales S
INNER JOIN
        (SELECT product_id, MIN(year) first_year
        FROM Sales
        GROUP BY product_id) T
ON S.product_id = T.product_id
WHERE T.first_year = S.year
```

<a id='Classes_With_at_Least_5_Students'></a>
# Classes_With_at_Least_5_Students

```sql
/* Write your T-SQL query statement below */
SELECT class
FROM courses
GROUP BY class
HAVING COUNT(student) >= 5
```

<a id='Find_Followers_Count'></a>
# Find_Followers_Count

```sql
/* Write your T-SQL query statement below */
SELECT user_id, COUNT(*) followers_count
FROM Followers
GROUP BY user_id
ORDER BY user_id
```

<a id='Biggest_Single_Number'></a>
# Biggest_Single_Number

```sql
/* Write your T-SQL query statement below */

SELECT TOP(1) t2.num
FROM MyNumbers t1
LEFT JOIN
(
    SELECT num, COUNT(*) n_count
    FROM MyNumbers
    GROUP BY num
    HAVING COUNT(*) = 1
) t2
ON t1.num = t2.num
ORDER BY t2.num DESC
```

<a id='Customers_Who_Bought_All_Products'></a>
# Customers_Who_Bought_All_Products

```sql
SELECT customer_id
FROM Customer
GROUP BY customer_id
HAVING COUNT(DISTINCT product_key) = (SELECT COUNT(*) FROM Product)
```

<a id='The_Number_of_Employees_Which_Report_to_Each_Employee'></a>
# The_Number_of_Employees_Which_Report_to_Each_Employee

```sql
SELECT employee_id, name, reports_count, average_age
FROM Employees e
INNER JOIN (
            SELECT reports_to, COUNT(*) AS reports_count, ROUND(AVG(age * 1.0), 0) average_age
            FROM Employees
            WHERE reports_to IS NOT NULL
            GROUP BY reports_to
            ) m
ON e.employee_id = m.reports_to
```

<a id='Primary_Department_for_Each_Employee'></a>
# Primary_Department_for_Each_Employee

```sql
/* Write your T-SQL query statement below */
SELECT employee_id, department_id
FROM Employee e1
WHERE primary_flag = 'Y' 
        OR employee_id IN (
                            SELECT employee_id
                            FROM Employee
                            GROUP BY employee_id
                            HAVING COUNT(employee_id) = 1)
```

<a id='Triangle_Judgement'></a>
# Triangle_Judgement

```sql
SELECT x, y, z,
    CASE WHEN ((x + y > z) AND (x + z > y) AND (y + z > x)) THEN 'Yes' ELSE 'No' END AS triangle
FROM Triangle
```

<a id='Consecutive_Numbers'></a>
# Consecutive_Numbers

```sql
/* Write your T-SQL query statement below */
SELECT DISTINCT num AS ConsecutiveNums 
FROM (SELECT num,
        CASE WHEN (num = LEAD(num, 1) OVER(ORDER BY id)) AND 
                  (num = LEAD(num, 2) OVER(ORDER BY id)) THEN 1 ELSE 0 END AS mark_3
        FROM Logs) t
WHERE mark_3 = 1
```

<a id='Product_Price_at_a_Given_Date'></a>
# Product_Price_at_a_Given_Date

```sql
SELECT DISTINCT p3.product_id, CASE WHEN p4.new_price IS NULL THEN 10 ELSE p4.new_price END price
FROM Products p3
LEFT JOIN (SELECT p1.product_id, new_price
            FROM Products p1
            INNER JOIN (SELECT product_id, MAX(change_date) last_change_date
                        FROM Products
                        WHERE change_date <= '2019-08-16'
                        GROUP BY product_id) p2
            ON p1.product_id = p2.product_id AND change_date = last_change_date) p4
ON p3.product_id = p4.product_id
```

##### Another Solution
```sql
SELECT product_id,
    FIRST_VALUE(new_price) OVER(PARTITION BY product_id ORDER BY change_date DESC) AS price
FROM Products
WHERE change_date <= '2019-08-16'
UNION
SELECT product_id, 10 AS price
FROM Products
GROUP BY product_id
HAVING MIN(change_date) > '2019-08-16'
```

<a id='Last_Person_to_Fit_in_the_Bus'></a>
# Last_Person_to_Fit_in_the_Bus

```sql
WITH ranked AS (SELECT person_id, person_name, weight, turn,
                    SUM(weight) OVER(ORDER BY turn) total_weight
                FROM [Queue])

SELECT TOP(1) person_name
FROM ranked
WHERE total_weight <= 1000
ORDER BY total_weight DESC
```

<a id='Count_Salary_Categories'></a>
# Count_Salary_Categories

```sql
/* Write your T-SQL query statement below */
WITH accounts_cat AS (
    SELECT account_id, income, CASE WHEN income < 20000
        THEN 'Low Salary'
        WHEN income BETWEEN 20000 AND 50000
        THEN 'Average Salary'
        ELSE 'High Salary' END AS category
    FROM accounts
)

SELECT b.category, COUNT(account_id) accounts_count
FROM accounts_cat ac
RIGHT JOIN (VALUES('Low Salary'), ('High Salary'), ('Average Salary')) AS b(category)
ON ac.category = b.category
GROUP BY b.category
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
