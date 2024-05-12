# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:

Developed by : ROSHINI S

REG NO : 212223230174

```
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
sns.lineplot(x=x,y=y)
```

![image](https://github.com/23008859/EXNO-6-DS/assets/139117979/8598fca5-8f57-402c-923a-1ef0d0dffb1c)

```
df = sns.load_dataset("tips")
df
```

![image](https://github.com/23008859/EXNO-6-DS/assets/139117979/59da7d4c-17b3-43fe-af1e-d9c6b04ce4c2)
```
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")
```
![image](https://github.com/23008859/EXNO-6-DS/assets/139117979/b79399ed-b091-49dd-a45c-f16c4ecc163f)

```
x=[1, 2, 3, 4, 5]
y1=[3, 5, 2, 6, 1]
y2=[1, 6, 4, 3, 8]
y3=[5, 2, 7, 1, 4]
sns.lineplot(x=x, y=y1)
sns.lineplot(x=x, y=y2)
sns.lineplot(x=x, y=y3)
plt.title("Multi-Line Plot")
plt.xlabel('X Label')
plt.ylabel("Y Label")
```

![image](https://github.com/23008859/EXNO-6-DS/assets/139117979/e34c0d1e-4457-45b2-9b39-1f636135b952)
```
tips=sns.load_dataset('tips')
avg_total_bill = tips.groupby('day')['total_bill'].mean()
avg_tip = tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```
![image](https://github.com/23008859/EXNO-6-DS/assets/139117979/23103bf3-b9af-4abf-bb76-d74eb88dbb83)

```
avg_total_bill = tips.groupby('time')['total_bill'].mean() 
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)
```
![image](https://github.com/23008859/EXNO-6-DS/assets/139117979/7539e535-b39b-4ab1-a52e-6f6aa00231ae)
```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939] 
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
```
```
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```
![image](https://github.com/23008859/EXNO-6-DS/assets/139117979/cc9647df-8bc8-496e-be56-0018866bf05c)

```
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')
```
![image](https://github.com/23008859/EXNO-6-DS/assets/139117979/b0a44bc6-4400-43ed-afcc-094e814b055f)
```
tit=pd.read_csv("titanic_dataset.csv")
tit
```
![image](https://github.com/23008859/EXNO-6-DS/assets/139117979/9ee0894a-977b-468f-8b71-7ee9d940c56d)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow') 
plt.title("Fare of Passenger by Embarked Town")
```
![image](https://github.com/23008859/EXNO-6-DS/assets/139117979/5d8b603e-e83e-4f43-9a3c-edf525b0217f)

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass') 
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```
![image](https://github.com/23008859/EXNO-6-DS/assets/139117979/fa09ec90-bdca-4ed1-a226-961e59d79cc6)

```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![image](https://github.com/23008859/EXNO-6-DS/assets/139117979/a191548b-fa36-4268-9b7f-38c252ec7864)
```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
``
![image](https://github.com/23008859/EXNO-6-DS/assets/139117979/9948f72d-0e51-4421-a12d-290b42334518)
```
sns.histplot(data = num_var, kde = True)
```
![image](https://github.com/23008859/EXNO-6-DS/assets/139117979/69995175-421c-45c9-b79b-2e90c8970a08)

```
df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```
![image](https://github.com/23008859/EXNO-6-DS/assets/139117979/d2157ccf-6380-42df-8ca6-83b34968c678)
```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```
![image](https://github.com/23008859/EXNO-6-DS/assets/139117979/372c8e66-9f10-426e-925a-268d06107dd3)

```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```
![image](https://github.com/23008859/EXNO-6-DS/assets/139117979/e83b7879-bf96-4421-a0d6-072b8d5ee8b9)
```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![image](https://github.com/23008859/EXNO-6-DS/assets/139117979/79670d7c-3daa-455b-842c-9f31e443408a)

```
mart=pd.read_csv("titanic_dataset.csv")
mart
```
![image](https://github.com/23008859/EXNO-6-DS/assets/139117979/fac65f31-cf43-42f2-999e-10c869300c4f)

```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']] 
mart.head(10)
```
![image](https://github.com/23008859/EXNO-6-DS/assets/139117979/8f2a5210-75ba-47dd-976b-058bb97cd640)
```
sns.kdeplot(data=mart,x='PassengerId')
```
![image](https://github.com/23008859/EXNO-6-DS/assets/139117979/9d76d971-7519-44de-a234-e49a45353b9c)

```
sns.kdeplot(data=mart,x='Age')
```
![image](https://github.com/23008859/EXNO-6-DS/assets/139117979/39d3d856-7eeb-4a8d-b8df-a231e4c8cb75)

```
sns.kdeplot(data=mart)
```
![image](https://github.com/23008859/EXNO-6-DS/assets/139117979/4157d196-20b9-4a52-bf4e-26fffe1c9562)
```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```
![image](https://github.com/23008859/EXNO-6-DS/assets/139117979/eb005d45-0e84-4402-bd6d-9a2ef6000e2e)

```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```
![image](https://github.com/23008859/EXNO-6-DS/assets/139117979/a3256e75-841f-4461-b989-81f7dd53f328)

```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```
![image](https://github.com/23008859/EXNO-6-DS/assets/139117979/e3a17abe-556d-453f-8936-1a410c10eabf)
```
hm=sns.heatmap(data=data)
```
![image](https://github.com/23008859/EXNO-6-DS/assets/139117979/976139ec-5b13-4140-8cf7-50fab47750e5)

# Result:

 Thus, all the data visualization techniques of seaborn has been implemented.
