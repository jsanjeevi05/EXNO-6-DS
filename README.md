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
```
DEVELOPED BY : SANJEEVI J
REG.NO: 212222110040
```
```
import seaborn as sns
import matplotlib.pyplot as plt
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
```
![Screenshot 2024-05-06 155911](https://github.com/Anusharonselva/EXNO-6-DS/assets/119405600/49d9b1ca-f56c-4a3c-9f69-2fd60595a9bd)
```
df=sns.load_dataset('tips')
df
```
![Screenshot 2024-05-06 160004](https://github.com/Anusharonselva/EXNO-6-DS/assets/119405600/fd6d7841-8c38-4994-9fbf-85db4897edf7)
```
sns.lineplot(x='total_bill',y='tip',data=df,hue='sex',linestyle='solid',legend='auto')
```
![Screenshot 2024-05-06 160044](https://github.com/Anusharonselva/EXNO-6-DS/assets/119405600/9f5e55e3-a87f-4db0-b679-c7f2f6299e9e)
```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi-Line Plot')
plt.xlabel('X Label')
plt.ylabel('Y Lbel')
```
![Screenshot 2024-05-06 160128](https://github.com/Anusharonselva/EXNO-6-DS/assets/119405600/be2634bf-e69f-4bd7-80c2-961e8e985caa)
```
import seaborn as sns
import matplotlib.pyplot as plt
tips=sns.load_dataset('tips')
avg_total_bill=tips.groupby('day')['total_bill'].mean()
avg_tip=tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill')
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title("Average Total Bill and Tip by Day")
plt.legend()
```
![Screenshot 2024-05-06 160210](https://github.com/Anusharonselva/EXNO-6-DS/assets/119405600/d6e12d89-00ee-4020-9052-95353c75ddfc)
```
avg_total_bill=tips.groupby('time')['total_bill'].mean()
avg_tip=tips.groupby('time')['tip'].mean()
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill',width=0.4)
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip',width=0.4)
plt.xlabel('Time of Day')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Time of Day')
plt.legend()
```
![Screenshot 2024-05-06 160302](https://github.com/Anusharonselva/EXNO-6-DS/assets/119405600/8b6cf167-f1b1-4125-a1bf-893d015466d2)
```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939] 
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```
![Screenshot 2024-05-06 160410](https://github.com/Anusharonselva/EXNO-6-DS/assets/119405600/23c58270-fd80-48b7-b389-f17c79e31534)
```
import seaborn as sns
dt= sns.load_dataset('tips')
# Bar plot with hue parameter
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the week')
plt.ylabel('Total Bill')
plt.title('Total Bill by Day and Gender')
```
![Screenshot 2024-05-06 160531](https://github.com/Anusharonselva/EXNO-6-DS/assets/119405600/552ea7af-f178-4ee3-a995-3cea86a3d517)
```
tit=pd.read_csv("titanic_dataset.csv")
tit
```
![Screenshot 2024-05-06 160632](https://github.com/Anusharonselva/EXNO-6-DS/assets/119405600/85bbe2e0-26d9-48f4-a525-dba9676dec9e)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow') 
plt.title("Fare of Passenger by Embarked Town")
```
![Screenshot 2024-05-06 201319](https://github.com/Anusharonselva/EXNO-6-DS/assets/119405600/04aef0b1-40bc-4ed1-8712-39b11bc5c8de)

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass') 
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```
![Screenshot 2024-05-06 160848](https://github.com/Anusharonselva/EXNO-6-DS/assets/119405600/3abb21a9-8a8f-4e3f-869c-817cd65f372f)
```
import seaborn as sns
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill',y='tip',hue='sex',data=tips)
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![Screenshot 2024-05-06 160953](https://github.com/Anusharonselva/EXNO-6-DS/assets/119405600/69a6d3bd-7a4c-4f22-9ec0-0a395db5bfe5)

```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```
![Screenshot 2024-05-06 161412](https://github.com/Anusharonselva/EXNO-6-DS/assets/119405600/9afb2c33-4183-424b-9f6f-a759713f8dff)
```
sns.histplot(data = num_var, kde = True)
```
![Screenshot 2024-05-06 161458](https://github.com/Anusharonselva/EXNO-6-DS/assets/119405600/23c94a65-4311-4ee7-9b6e-7a363ebab670)
```
df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```
![Screenshot 2024-05-06 161547](https://github.com/Anusharonselva/EXNO-6-DS/assets/119405600/d13a9418-892a-453d-b72f-30ac8e87bcbd)
```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```
![Screenshot 2024-05-06 161629](https://github.com/Anusharonselva/EXNO-6-DS/assets/119405600/e20337b2-2b14-495f-a52f-0af4cf6c1caa)

```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```
![Screenshot 2024-05-06 161720](https://github.com/Anusharonselva/EXNO-6-DS/assets/119405600/5beeead7-5e71-44b9-9f4d-1757c08b717e)
```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6,
palette="Set3", inner="quartile")
plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![Screenshot 2024-05-06 161804](https://github.com/Anusharonselva/EXNO-6-DS/assets/119405600/60486938-8a31-476b-9a03-82f02e229ce1)

```
mart=pd.read_csv("titanic_dataset.csv")
mart
```
![Screenshot 2024-05-06 161850](https://github.com/Anusharonselva/EXNO-6-DS/assets/119405600/8fde639d-a3b9-4768-b4d7-fe7ccc6318fb)
```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']] 
mart.head(10)
```
![Screenshot 2024-05-06 201504](https://github.com/Anusharonselva/EXNO-6-DS/assets/119405600/047ec4fb-77ef-4904-9336-4c36470af5ca)
```
sns.kdeplot(data=mart,x='PassengerId')
```
![Screenshot 2024-05-06 201559](https://github.com/Anusharonselva/EXNO-6-DS/assets/119405600/f5e857ca-4b90-4797-9921-009d3801bd42)
```
sns.kdeplot(data=mart,x='Age')
```
![Screenshot 2024-05-06 201644](https://github.com/Anusharonselva/EXNO-6-DS/assets/119405600/08ccbb17-85df-44f2-af62-231d19053113)
```
sns.kdeplot(data=mart)
```
![Screenshot 2024-05-06 201729](https://github.com/Anusharonselva/EXNO-6-DS/assets/119405600/a3a4a863-dafb-4267-be4f-89f875c8594a)
```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```
![Screenshot 2024-05-06 201824](https://github.com/Anusharonselva/EXNO-6-DS/assets/119405600/3464c54e-9040-42dd-8bdc-4e8307ea657c)
```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```
![Screenshot 2024-05-06 201911](https://github.com/Anusharonselva/EXNO-6-DS/assets/119405600/af4205be-34da-4900-968d-dcd16a430976)
```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```
![Screenshot 2024-05-06 201946](https://github.com/Anusharonselva/EXNO-6-DS/assets/119405600/39c01876-fb2e-41e1-8e58-49e786960738)
```
hm=sns.heatmap(data=data)
```
![Screenshot 2024-05-06 202023](https://github.com/Anusharonselva/EXNO-6-DS/assets/119405600/01ef62a5-40a0-4c78-aaac-d2183ea2609b)

# Result:
Thus, all the data visualization techniques of seaborn has been implemented.
