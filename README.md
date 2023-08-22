# EX-3 Perform-log-transformation-on-international-airline-passenger-data
## AIM:
To Write a Program to log transformation on international airline passenger data

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Procedure:
    1.import the numpy ,pandas and matplotlib.pyplot modules
    2.read the dataset using pandas
    3.applying log transformation for dataset
    4.Plot the trend dataset 
    5.plot the log transformation data


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

### data.head()

![s1](https://github.com/praveenst13/Perform-log-transformation-on-international-airline-passenger-data/assets/118787793/9056b407-96a2-4a7b-bc0b-a70cc5c764bd)
### data.tail()


![s2](https://github.com/praveenst13/Perform-log-transformation-on-international-airline-passenger-data/assets/118787793/217dde8b-6f82-422d-aedd-a111a7ad9b4f)
### data.shape

![s3](https://github.com/praveenst13/Perform-log-transformation-on-international-airline-passenger-data/assets/118787793/477f6b91-f630-4bac-9bcc-7d612ef580f0)

###  data
![s4](https://github.com/praveenst13/Perform-log-transformation-on-international-airline-passenger-data/assets/118787793/087386e1-93c0-4b22-8c66-265df824f5ab)

### Graph for datasets

![s5](https://github.com/praveenst13/Perform-log-transformation-on-international-airline-passenger-data/assets/118787793/71aaa752-885d-4d3c-9e06-0ed830324d10)


### Trend graph

![s6](https://github.com/praveenst13/Perform-log-transformation-on-international-airline-passenger-data/assets/118787793/f16acb98-34b4-4403-bee0-6ec0574b1056)
### seasonality graph
![s7](https://github.com/praveenst13/Perform-log-transformation-on-international-airline-passenger-data/assets/118787793/ce508465-5bed-44aa-a9b2-97cc1d162b96)

###  log-transformed data
![s8](https://github.com/praveenst13/Perform-log-transformation-on-international-airline-passenger-data/assets/118787793/55f5199e-e9b6-4e10-b399-d0dd0d7cd4d9)




























## Result:
Thus the program to t log transformation on international airline passenger data is written and
verified using python programming.
