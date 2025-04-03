# LeetCode SQL 50

<li><a href="#Recyclable_and_Low_Fat_Products">Recyclable_and_Low_Fat_Products</a></li>
<li><a href="#Find_Customer_Referee">Find_Customer_Referee</a></li>
<li><a href="#Big_Countries">Big_Countries</a></li>
<li><a href="#Article_Views_I">Article_Views_I</a></li>
<li><a href="#Invalid_Tweets">Invalid_Tweets</a></li>
<li><a href="#Write_Here">Write_Here</a></li>
<li><a href="#Write_Here">Write_Here</a></li>
<li><a href="#Write_Here">Write_Here</a></li>
<li><a href="#Write_Here">Write_Here</a></li>
<li><a href="#Write_Here">Write_Here</a></li>


```python
input().replace(' ', '_')
```

     Invalid Tweets
    




    'Invalid_Tweets'



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


```python
<a id='Refer_to'></a>
# Refer_to
```

```sql

```


```python
<a id='Refer_to'></a>
# Refer_to
```

```sql

```


```python
<a id='Refer_to'></a>
# Refer_to
```

```sql

```


```python
<a id='Refer_to'></a>
# Refer_to
```

```sql

```


```python
<a id='Refer_to'></a>
# Refer_to
```

```sql

```
