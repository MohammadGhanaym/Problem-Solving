## Table of Contents
<li><a href="#Unique_Users_Per_Client_Per_Month">Unique_Users_Per_Client_Per_Month</a></li>
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

     Unique Users Per Client Per Month
    




    'Unique_Users_Per_Client_Per_Month'



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
