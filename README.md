# Data-Visulization-Using-Matplotlib-and-Seaborn
Data Visulization Using Matplotlib and Seaborn

Data Visulization using matplotlib and Seaborn
Matplotlib py library
import seaborn as sns
import matplotlib.pyplot as plt
# Line plot graph
x = [1,2,3,4,5,6,7,8,9,10]
y = [10,23,45,65,23,12,46,78,89,90]
plt.figure(figsize=(8,4)) # Changing image size 
plt.title("My Graph",fontsize=14,color='blue')
plt.xlabel("Days",fontsize = 14, color = 'blue')
plt.ylabel("Sales", fontsize = 14, color = 'blue')

plt.xticks(x,color = 'purple')
plt.yticks(color = 'purple')
plt.grid()

plt.plot(x,y, color = 'Red', linestyle='dashed', lw = 3, label = 'Line Bar Graph') # solid, dashed and dotted these are the line color
# LW shows the line width
plt.legend()
plt.show()

# Scatter plot graph
import numpy as np
np.random.seed(1)
x = np.random.randint(1,100,50)
y = np.random.randint(1,100,50)
plt.figure(figsize=(8,4))
plt.title("Scatter Graph", fontsize=14, color="purple")

plt.xlabel("Days",fontsize = 14, color = 'black')
plt.ylabel("Sales", fontsize = 14, color = 'black')

plt.xticks(color="Purple")
plt.yticks(color="purple")


plt.scatter(x,y,color="purple",s=50,label="scattered plot graph", marker="o") #<,>,*,.
plt.legend()
plt.show()

# Bar Plot Graph
x=[1,2,3,4,5,6,7,8,9,10]
y=[10,20,30,40,50,60,70,80,90,100]
plt.figure(figsize=(8,5))
plt.title("Bar Plot Graph",fontsize=14,color='Black')

plt.xlabel("Days",fontsize=14,color='Black')
plt.ylabel("Sales",fontsize=14,color='Black')

plt.xticks(x,color="Red")
plt.yticks(y,color="Red")

plt.bar(x,y,color='purple',label="Bar plot graph",width=.5)
plt.legend()
plt.show()

# Histogram
np.random.seed(1)
data = np.random.randint(1,100,50)
plt.hist(data,color='orange',rwidth=0.9)
plt.show()
data

array([38, 13, 73, 10, 76,  6, 80, 65, 17,  2, 77, 72,  7, 26, 51, 21, 19,
       85, 12, 29, 30, 15, 51, 69, 88, 88, 95, 97, 87, 14, 10,  8, 64, 62,
       23, 58,  2,  1, 61, 82,  9, 89, 14, 48, 73, 31, 72,  4, 71, 22])
# Comparison all
x = [1,2,3,4,5,6,7,8,9,10]
y = [10,23,45,65,23,12,46,78,89,90]
plt.figure(figsize=(8,4)) # Changing image size 
plt.title("My Graph",fontsize=14,color='blue')

plt.bar(x,y,color='black',label="Bar plot graph",width=.5)
plt.scatter(x,y,color="blue",s=50,label="scattered plot graph", marker="o") #<,>,*,.
plt.plot(x,y, color = 'Red', linestyle='dashed', lw = 3, label = 'Line bar Graph') # solid, dashed and dotted these are the line color
# LW shows the line width
plt.legend()
plt.show()

# Pie Charts
slices=[100,70,80,78]
names=['science','pak110','comp302','math110']
plt.figure(figsize=(5,5))
plt.pie(slices,labels=names,autopct="%0.2f%%",explode=(0,0,0.3,0), shadow=True)# Utopct format like this
plt.legend()
plt.show()

x = [1,2,3,4,5,6,7,8,9,10]
y = [10,23,45,65,23,12,46,78,89,90]
plt.barh(x,y,color='purple',label="Barh plot graph",height=.5)
plt.legend()
plt.show()

# SubPlot 
x = [1,2,3,4,5,6,7,8,9,10]
y = [10,23,45,65,23,12,46,78,89,90]
 
    
plt.figure(figsize=(10,5))
plt.subplot(2,3,1)
plt.plot(x,y, color = 'Red', linestyle='dashed', label = 'Line bar Graph')
         
plt.subplot(2,3,2)   
plt.scatter(x,y,color="blue",s=50,label="scattered plot graph", marker="o") #
     
plt.subplot(2,3,3)   
plt.bar(x,y,color='purple',label="Bar plot graph",width=.5)

plt.subplot(2,3,4) 
plt.barh(x,y,color='purple',label="Barh plot graph",height=.5)
     
plt.subplot(2,3,5)     
data = np.random.randint(1,100,50)
plt.hist(data,color='orange',rwidth=0.9)
     
plt.subplot(2,3,6)
slices=[100,70,80,78]
names=['science','pak110','comp302','math110']
plt.pie(slices,labels=names,autopct="%0.2f%%",explode=(0,0,0.3,0), shadow=True)# Utopct format like this
plt.show()

Seaborn py Library
import seaborn as sns
a=['male','female','male','male','male','female','male','female','male','female']
job =['manager','developer','manager','developer','manager','manager','manager','developer','manager','developer']
sns.countplot(x=a,hue=job)
plt.show()

data=sns.load_dataset('tips')
data
total_bill	tip	sex	smoker	day	time	size
0	16.99	1.01	Female	No	Sun	Dinner	2
1	10.34	1.66	Male	No	Sun	Dinner	3
2	21.01	3.50	Male	No	Sun	Dinner	3
3	23.68	3.31	Male	No	Sun	Dinner	2
4	24.59	3.61	Female	No	Sun	Dinner	4
...	...	...	...	...	...	...	...
239	29.03	5.92	Male	No	Sat	Dinner	3
240	27.18	2.00	Female	Yes	Sat	Dinner	2
241	22.67	2.00	Male	Yes	Sat	Dinner	2
242	17.82	1.75	Male	No	Sat	Dinner	2
243	18.78	3.00	Female	No	Thur	Dinner	2
244 rows × 7 columns

sns.countplot(data['sex'],hue=data['smoker'])
plt.show()
C:\Users\Ch Usman\anaconda3\lib\site-packages\seaborn\_decorators.py:36: FutureWarning: Pass the following variable as a keyword arg: x. From version 0.12, the only valid positional argument will be `data`, and passing other arguments without an explicit keyword will result in an error or misinterpretation.
  warnings.warn(

sns.relplot(x=data['total_bill'],y=data['tip'],kind='scatter',s=200,hue=data['day'],col=data['day'],col_wrap=2)
plt.show()

# Heat map
np.random.seed(1)
samples = np.random.randint(1,100,(10,10))
samples
array([[38, 13, 73, 10, 76,  6, 80, 65, 17,  2],
       [77, 72,  7, 26, 51, 21, 19, 85, 12, 29],
       [30, 15, 51, 69, 88, 88, 95, 97, 87, 14],
       [10,  8, 64, 62, 23, 58,  2,  1, 61, 82],
       [ 9, 89, 14, 48, 73, 31, 72,  4, 71, 22],
       [50, 58,  4, 69, 25, 44, 77, 27, 53, 81],
       [42, 83, 16, 65, 69, 26, 99, 88,  8, 27],
       [26, 23, 10, 68, 24, 28, 38, 58, 84, 39],
       [ 9, 33, 35, 11, 24, 16, 88, 26, 72, 93],
       [75, 63, 47, 33, 89, 24, 56, 66, 78,  4]])
plt.figure(figsize=(10,5))
sns.heatmap(samples,annot=True,cmap='Blues') # Cmap changing the color and annot showing the values on each
plt.savefig("heatmap.png")
plt.show()

 
