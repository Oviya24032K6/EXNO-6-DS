# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY
### REG NO : 212223110033
### NAME : OVIYA P
### DATE : 08/05/2025
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

 ```
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
```
![image](https://github.com/user-attachments/assets/77a517de-6e1e-40f4-88f3-ce2ebbdac9b8)

```
df = sns.load_dataset("tips")
df
```
![image](https://github.com/user-attachments/assets/af0ba9b9-95ee-4ea0-aa4c-552278caf671)
```
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")

```
![image](https://github.com/user-attachments/assets/9b00a75c-80fd-426f-bfa6-c73f3c70eedf)
```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title("Multi-line Plot")
plt.xlabel('X Label')
plt.ylabel('Y Label')
```
![image](https://github.com/user-attachments/assets/71d237a0-193a-43a3-89e0-dd916b31b677)
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
![image](https://github.com/user-attachments/assets/5d85a818-5602-4139-9adc-6adca3f3fb53)
```
avg_total_bill = tips.groupby('time')['total_bill'].mean()
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)
```
![image](https://github.com/user-attachments/assets/9fcd1f07-9580-4b13-b95d-26410e6165f5)
```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939]
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```
![image](https://github.com/user-attachments/assets/2236a738-76ea-49ef-b949-75f8ed23b3d7)
```
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')
```
![image](https://github.com/user-attachments/assets/d004a293-1042-4713-8349-3e088aa44f76)

```
tit=pd.read_csv("drive/MyDrive/DS2024/titanic_dataset.csv")
tit
```
![image](https://github.com/user-attachments/assets/d883ec9e-aa04-4c19-bb52-bd7539d34396)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow')
plt.title("Fare of Passenger by Embarked Town")
```

![image](https://github.com/user-attachments/assets/7fe9a09f-c433-402e-b79d-e3e3ede45d94)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass')
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```
![image](https://github.com/user-attachments/assets/1cf013d4-8891-469e-8496-bdaed42279da)
```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![image](https://github.com/user-attachments/assets/6d4ce706-6fc3-41ff-9b20-4b574529f735)

```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```
![image](https://github.com/user-attachments/assets/2ec0f3da-dd9d-4b3c-b134-71d4d610200f)
```
sns.histplot(data = num_var, kde = True)
```
![image](https://github.com/user-attachments/assets/fb64854c-6f7c-49b6-92e1-a955824512e5)
```
df=pd.read_csv("drive/MyDrive/DS2024/titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```
![image](https://github.com/user-attachments/assets/a77dff7a-d07a-44e1-a7e7-798f27a086b9)
```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```
![image](https://github.com/user-attachments/assets/a5c729f5-d290-44ab-b09a-36f4240e45c7)
```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```
![image](https://github.com/user-attachments/assets/21646288-c16d-4e78-b8f7-0ec4a12093d4)
```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![image](https://github.com/user-attachments/assets/d46a75bf-dcfb-4e27-95ba-f7278b85fac0)

```
mart=pd.read_csv("drive/MyDrive/DS2024/titanic_dataset.csv")
mart
```
![image](https://github.com/user-attachments/assets/9f22f502-69d5-4e11-8e59-13e2c6a15619)
```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']]
mart.head(10)
```
![image](https://github.com/user-attachments/assets/2e83d125-b5cc-46cd-b299-9a8a22bb5e46)
```
sns.kdeplot(data=mart,x='PassengerId')
```
![image](https://github.com/user-attachments/assets/34594ada-e9ca-429f-8af1-94525eb72788)
```
sns.kdeplot(data=mart,x='Age')
```
![image](https://github.com/user-attachments/assets/c006fc81-cb5e-4a55-a85d-c842752eec51)
```
sns.kdeplot(data=mart)
```
![image](https://github.com/user-attachments/assets/47cd7eef-13f0-492d-88eb-4f45fc2dd220)
```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```
![image](https://github.com/user-attachments/assets/9710fb67-5213-4168-a79c-dcf102981ab9)
```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```
![image](https://github.com/user-attachments/assets/2644ee39-63e9-4b10-af6d-aa122d107e66)
```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```
![image](https://github.com/user-attachments/assets/15cd2c30-7881-431f-8258-92a8fc3a6401)
```
hm=sns.heatmap(data=data)
```
![image](https://github.com/user-attachments/assets/52b4a724-fcb3-4d93-8462-3e8aa583f21c)

# Result:
 Thus the program has done and executed succesfully
