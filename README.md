# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.
  # Name : SURYAMALARV
  # Reg : 212223230224

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
sns.lineplot(x=x,y=y)
```
![image](https://github.com/user-attachments/assets/6bde8131-398f-43a7-884c-f95b21668e9d)
```
df = sns.load_dataset("tips")
df
```
![image](https://github.com/user-attachments/assets/bc80c8a3-956b-4a4e-be0e-21170992eda7)
```
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")
```
![image](https://github.com/user-attachments/assets/916b7098-6b28-4db3-bd90-ae53cb5ccc56)
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
![image](https://github.com/user-attachments/assets/16d28d41-7e53-457d-bd0a-08fccee8947f)
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
![image](https://github.com/user-attachments/assets/27a001d2-7eca-47bb-9d62-f25b9282d40a)
```
avg_total_bill = tips.groupby('time')['total_bill'].mean() 
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)
```
![image](https://github.com/user-attachments/assets/c0d8acf8-ab12-4bce-b4b6-01d892556acb)

```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939] 
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
```
```
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```
![image](https://github.com/user-attachments/assets/b7a9b716-4974-4126-9058-1287bbeb7f59)
```
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')
```
![image](https://github.com/user-attachments/assets/4f47ba64-259c-44bd-bbc8-dfb1cb0e2191)
```
tit=pd.read_csv("titanic_dataset.csv")
tit
```
![image](https://github.com/user-attachments/assets/68e6da70-89e0-4b0b-9437-0ecf24cec7f6)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow') 
plt.title("Fare of Passenger by Embarked Town")
```
![image](https://github.com/user-attachments/assets/315a75dc-197d-43ee-a6f7-678931d85967)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass') 
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```
![image](https://github.com/user-attachments/assets/d8db1ec8-291f-47d3-8372-6fb7798ca73e)
```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![image](https://github.com/user-attachments/assets/b07e8c50-ffa9-4e26-808d-469d3621a16b)
```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```
![image](https://github.com/user-attachments/assets/a340301d-7b82-44ba-8713-4bab78d97e4e)
```
sns.histplot(data = num_var, kde = True)
```
![image](https://github.com/user-attachments/assets/2d175fad-8ecb-4a4a-88ba-16bab9e4c374)
```
df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```
![image](https://github.com/user-attachments/assets/ce6a84a4-e81e-4e04-9a0f-00cd000f53a8)
```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```
![image](https://github.com/user-attachments/assets/7a5f06d8-f86e-4f4f-8adf-fb5bae211d4f)
```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```
![image](https://github.com/user-attachments/assets/edf2bd40-3ef7-4b8a-a5d8-10fc04106a6f)
```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![image](https://github.com/user-attachments/assets/1a311175-31c5-4dbc-aaf9-d33b519ce7e3)
```
mart=pd.read_csv("titanic_dataset.csv")
mart
```
![image](https://github.com/user-attachments/assets/ed9b41bc-b256-4622-964b-371580872299)
```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']] 
mart.head(10)
```
![image](https://github.com/user-attachments/assets/1538a9cd-920c-4d3e-8e7f-af964ba75153)
```
sns.kdeplot(data=mart,x='PassengerId')
```
![image](https://github.com/user-attachments/assets/f0e0a70c-35e9-4ea8-8d9d-105fd80e78ff)
```
sns.kdeplot(data=mart,x='Age')
```
![image](https://github.com/user-attachments/assets/e4d5bf66-2b0c-4dbc-ae0f-9582345c6871)
```
sns.kdeplot(data=mart)
```
![image](https://github.com/user-attachments/assets/09014e01-23bb-4b59-a2d6-da4ed961554f)
```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```
![image](https://github.com/user-attachments/assets/3461babf-cd2f-4d1a-b98e-4db2e0d55b53)
```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```
![image](https://github.com/user-attachments/assets/7d0dec50-12a4-4333-835b-e3b6f61b51d1)
```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```
![image](https://github.com/user-attachments/assets/5a7607c2-2389-45b8-84bb-7fa3375708d5)
```
hm=sns.heatmap(data=data)
```
![image](https://github.com/user-attachments/assets/d22478d5-902b-409f-b82e-b01c41f8716f)

# Result:
 Thus, all the data visualization techniques of seaborn has been implemented.
