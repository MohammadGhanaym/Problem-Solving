## Table of Contents
<li><a href="#Unique_Users_Per_Client_Per_Month">Unique_Users_Per_Client_Per_Month</a></li>
<li><a href="#Number_of_Shipments_Per_Month">Number_of_Shipments_Per_Month</a></li>
<li><a href="#Most_Lucrative_Products">Most_Lucrative_Products</a></li>
<li><a href="#Number_Of_Bathrooms_And_Bedrooms">Number_Of_Bathrooms_And_Bedrooms</a></li>
<li><a href="#MacBookPro_User_Event_Count">MacBookPro_User_Event_Count</a></li>
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

     MacBookPro User Event Count
    




    'MacBookPro_User_Event_Count'



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

<a id='Number_Of_Bathrooms_And_Bedrooms'></a>
# Number_Of_Bathrooms_And_Bedrooms


```python
airbnb_search_details.groupby(['city', 'property_type'], as_index=False).agg(n_bedrooms_avg = ('bedrooms', 'mean'),
                                                             n_bathrooms_avg = ('bathrooms', 'mean'))
```

```SQL
SELECT city, 
       property_type, 
       AVG(CAST(bathrooms AS FLOAT)) AS n_bathrooms_avg, 
       AVG(CAST(bedrooms AS FLOAT)) AS n_bedrooms_avg
FROM airbnb_search_details
GROUP BY city, property_type
```

<a id='MacBookPro_User_Event_Count'></a>
# MacBookPro_User_Event_Count


```python
# Import your libraries
import pandas as pd

# Start writing code
mackbookpro_users = playbook_events[playbook_events['device'] == 'macbook pro']
mackbookpro_users.event_name.value_counts().reset_index(name='event_count').rename(columns={'index': 'event_name'})
```

```sql
select event_name, COUNT(*) AS event_count
FROM playbook_events
WHERE device = 'macbook pro'
GROUP BY event_name
ORDER BY event_count DESC
```


```python
<a id='Refer_to'></a>
# Refer_to
```


```python
<a id='Refer_to'></a>
# Refer_to
```


```python
<a id='Refer_to'></a>
# Refer_to
```


```python
<a id='Refer_to'></a>
# Refer_to
```


```python
<a id='Refer_to'></a>
# Refer_to
```


```python
<a id='Refer_to'></a>
# Refer_to
```


```python
<a id='Refer_to'></a>
# Refer_to
```


```python
<a id='Refer_to'></a>
# Refer_to
```


```python
<a id='Refer_to'></a>
# Refer_to
```
