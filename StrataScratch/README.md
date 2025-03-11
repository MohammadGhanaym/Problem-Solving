## Table of Contents
<li><a href="#Unique_Users_Per_Client_Per_Month">Unique_Users_Per_Client_Per_Month</a></li>
<li><a href="#Number_of_Shipments_Per_Month">Number_of_Shipments_Per_Month</a></li>
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

     Number of Shipments Per Month
    




    'Number_of_Shipments_Per_Month'



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
