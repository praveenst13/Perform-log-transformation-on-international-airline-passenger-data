# Perform-log-transformation-on-international-airline-passenger-data
## AIM:
To Write a Program to log transformation on international airline passenger data

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Procedure:


## Program:
```
/*4
log transformation on international airline passenger data

Developed by: Praveen s
RegisterNumber:  212222240077
*/
import pandas as pd
import numpy as np
import matplotlib.pylab as plt
%matplotlib inline
from matplotlib.pylab import rcParams
from datetime import datetime
data=pd.read_csv(r'/content/AirPassengers.csv')
data.head()

data.tail()

data.shape

data['Month']=pd.to_datetime(data['Month'], infer_datetime_format=True)
data=data.set_index(['Month'])
data

plt.figure(figsize=(20,10))
plt.xlabel("Month")
plt.ylabel("Air Passengers Count")
plt.plot(data)

trend = data['#Passengers'].rolling(window=12).mean()

# Plot the trend
plt.plot(trend)
plt.xlabel('Month')
plt.ylabel('Trend')
plt.show()

seasonality = data['#Passengers'] - trend
# Plot the seasonality
plt.plot(seasonality)
plt.xlabel('Month')
plt.ylabel('Seasonality')
plt.show()

# @title
# Apply log transformation to the data
log_data = np.log(data)

# Plot the original data and the log-transformed data
import matplotlib.pyplot as plt
#plt.hist(data, bins=50, label='Original Data')

plt.plot(log_data)
plt.legend()
plt.show()

```
## Output:




## Result:

