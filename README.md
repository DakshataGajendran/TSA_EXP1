# Ex.No: 01A PLOT A TIME SERIES DATA
## Developed by: DAKSHATA G
## Registe no: 212223240021
###  Date: 21-04-26

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:
# DATASET:https://www.kaggle.com/datasets/rakannimer/air-passengers

```
from matplotlib import pyplot as plt
import pandas as pd
df = pd.read_csv("AP.csv")
df['Month'] = pd.to_datetime(df['Month'])
df.set_index('Month', inplace=True)
df_resampled = df['#Passengers'].resample('D').interpolate()
df_resampled.plot(kind='line', label='Total Passengers', color='black')
plt.title('Time Series Plot of Number of Passengers Each Day')
plt.xlabel('Day')
plt.ylabel('Number of Passengers')
plt.legend()
plt.grid(True)
plt.show()
```

# OUTPUT:
<img width="767" height="583" alt="image" src="https://github.com/user-attachments/assets/420b5731-3b2d-4016-baea-88770ba48d6b" />







# RESULT:
Thus we have created the python code for plotting the time series of given data.
