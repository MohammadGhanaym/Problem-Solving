## Table of Contents
<li><a href="#Unique_Users_Per_Client_Per_Month">Unique_Users_Per_Client_Per_Month</a></li>
<li><a href="#Number_of_Shipments_Per_Month">Number_of_Shipments_Per_Month</a></li>
<li><a href="#Most_Lucrative_Products">Most_Lucrative_Products</a></li>
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

     Most Lucrative Products
    




    'Most_Lucrative_Products'



<a id='Unique_Users_Per_Client_Per_Month'></a>
# Unique_Users_Per_Client_Per_Month


```python
# Import your libraries
import pandas as pd

# Start writing code
fact_events['month'] = fact_events['time_id'].dt.month
fact_events.groupby(['client_id', 'month'])['user_id'].nunique().reset_index(name='users_num')
```

```sql
SELECT DISTINCT client_id, MONTH(time_id) AS month, COUNT(DISTINCT user_id) users_num
FROM fact_events
GROUP BY client_id, MONTH(time_id)
```

<a id='Number_of_Shipments_Per_Month'></a>
# Number_of_Shipments_Per_Month


```python
# Import your libraries
import pandas as pd

# Start writing code
amazon_shipment['year_month'] = amazon_shipment['shipment_date'].dt.strftime('%Y-%m')
amazon_shipment['shipment_unique_key'] =  amazon_shipment['shipment_id'] + amazon_shipment['sub_id']
amazon_shipment.groupby('year_month')['shipment_unique_key'].count().reset_index(name='count')
```

```sql

SELECT FORMAT(shipment_date, 'yyyy-MM') AS year_month, COUNT(DISTINCT CONCAT(shipment_id, '_' , sub_id)) AS [count]
FROM amazon_shipment
GROUP BY FORMAT(shipment_date, 'yyyy-MM')
```

<a id='Most_Lucrative_Products'></a>
# Most_Lucrative_Products


```python
# Import your libraries
import pandas as pd

# Start writing code

orders_first_half = online_orders[online_orders['date_sold'].between('2022-01-01', '2022-06-30')]
orders_first_half['revenue'] = online_orders['units_sold'] * online_orders['cost_in_dollars']
orders_first_half.groupby('product_id' ,as_index=False)['revenue'].sum().sort_values(by='revenue', ascending=False).iloc[:5, :]
```

```sql
SELECT TOP(5) product_id, SUM(units_sold * cost_in_dollars) AS revenue
FROM online_orders
WHERE date_sold BETWEEN '2022-01-01' AND '2022-06-30'
GROUP BY product_id
ORDER BY revenue DESC
```


```python
<a id='Refer_to'></a>
# Refer_to
```


```python
<a id='Refer_to'></a>
# Refer_to
```
