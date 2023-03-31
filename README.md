# workshop-Multivariate-analysis\

## AIM:
  To Perform Multivariate Analysis
## ALGORITHM:

1.Read the given data

2.Get information from the data

3.Perform the Multivariate Analysis

4.Save the clean data to file
PROGRAM:

## Types of Bivariate Analysis:

(i) Numerical & Numerical

## Scatter plot

import pandas as pd

import numpy as np

import seaborn as sns

import matplotlib as plt

df = pd.read_csv("/content/FlightInformation.csv")

sns.scatterplot (df['Price'],df['Arrival_Time'])

## ii) Numerical & Categorical

Bar Plot

import pandas as pd

import seaborn as sns

sns.barplot (x=df['Duration'],y=df['Price'])
![image](https://user-images.githubusercontent.com/121285701/229036719-41342eae-9bf2-45ed-a9e2-d23076888850.png)
sns.barplot(x=df["Arrival_Time"],y=df["Price"],data=df)
![image](https://user-images.githubusercontent.com/121285701/229037177-f308bb00-2728-4ae5-b016-c2328d9fbe12.png)
states=df.loc[:,["Duration","Price"]]

states=states.groupby(by=["Duration"]).sum().sort_values(by="Price")

import matplotlib.pyplot as plt

sns.barplot(x=states.index,y="Price",data=states)

plt.xticks(rotation = 90)

plt.xlabel=("Duration")

plt.ylabel=("Price")

plt.show()
![image](https://user-images.githubusercontent.com/121285701/229037358-a976640d-1137-4227-994b-5bd8c2bbac76.png)
## Multivariate analysis
## Categorical & Categorical Heatmap

import numpy as np

import seaborn as sn

import matplotlib.pyplot as plt

data=pd.read_csv("/content/FlightInformation.csv")

data = np.random.randint(low = 1, high = 100, size = (10, 10))

print("The data to be plotted:\n")

print(data)

hm = sn.heatmap(data = data)

plt.show()





