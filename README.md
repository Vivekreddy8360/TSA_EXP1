# Ex.No: 01 PLOT A TIME SERIES DATA
###  Date: 

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

## POPULATION:
```
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("POPTHM.csv",parse_dates=["DATE"],index_col="DATE")
df.head()
df["2015"].mean()
df.resample('Y').mean()
mean=df.resample('Y').mean().plot(kind='line')
plt.xlabel("Year")
plt.ylabel("Population(in Thousands)")
plt.show()
```
## MARKET PRICE
```
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("trainset.csv",parse_dates=["Date"],index_col="Date")
df.head()
df.Close.resample('M').mean()
mean=df.Close.resample('M').mean().plot(kind='line')
plt.xlabel("Month")
plt.ylabel("Price")
plt.show()
mean=df.Close.resample('Y').mean().plot(kind='line')
plt.xlabel("Year")
plt.ylabel("Price")
plt.show()
```
## TEMPERATURE
```
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("DailyDelhiClimateTrain.csv",parse_dates=["date"],index_col="date")
df.head()
mean=df["meantemp"].resample('M').mean().plot(kind='line')
plt.xlabel("Month")
plt.ylabel("Temperature")
plt.show()
```








# OUTPUT:
## Population
![image](https://github.com/Vivekreddy8360/TSA_EXP1/assets/94525701/2637f26d-1aa9-408a-ba5b-0c26a21f4ac9)

## Stock price
![image](https://github.com/Vivekreddy8360/TSA_EXP1/assets/94525701/0aac82a4-e928-4739-8d89-469c0167340a)

![image](https://github.com/Vivekreddy8360/TSA_EXP1/assets/94525701/4447b6d7-bdd1-4763-b93f-664d78d199d4)

## Temperature
![image](https://github.com/Vivekreddy8360/TSA_EXP1/assets/94525701/743bc474-2ace-4710-a5d6-dc6e8dad7c8c)


# RESULT:
Thus we have created the python code for plotting the time series of given data.
