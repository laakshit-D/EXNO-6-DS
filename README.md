# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

## Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

## EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

## Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

## Coding and Output:
```
NAME : LAAKSHIT D
REG NO : 212222230071
```
```py
import seaborn as sns
import matplotlib.pyplot as plt
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
```

![Screenshot 2024-05-04 100012](https://github.com/Harsayazheni/Expt06-Introduction-to-Data-Science/assets/118708467/1c8ab253-15f0-4b45-8caa-13ab87b620d0)

```py
df=sns.load_dataset("tips")
df
```

![Screenshot 2024-05-04 100022](https://github.com/Harsayazheni/Expt06-Introduction-to-Data-Science/assets/118708467/95a2ed6d-ef61-4344-be6d-175b073b5192)

```py
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle='solid',legend="auto")
```

![Screenshot 2024-05-04 100028](https://github.com/Harsayazheni/Expt06-Introduction-to-Data-Science/assets/118708467/99b1f75a-f56a-48fe-91c7-4b6d4cca4c62)

```py
x = [1, 2, 3, 4, 5]
y1 = [3, 5, 2, 6, 1]
y2 = [1, 6, 4, 3, 8]
y3 = [5, 2, 7, 1, 4]

sns.lineplot(x=x, y=y1, label='Line 1')
sns.lineplot(x=x, y=y2, label='Line 2')
sns.lineplot(x=x, y=y3, label='Line 3')

plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.title('Multiple Line Plot')

plt.show()
```

![image](https://github.com/laakshit-D/EXNO-6-DS/assets/119559976/65760c83-1d21-4d34-9883-5a7bb4dbc9fe)

**BAR PLOT**
```py
import seaborn as sns
import matplotlib.pyplot as plt

tips = sns.load_dataset('tips')

sns.barplot(x='day', y='total_bill', hue='sex', data=tips)
plt.title('Total Bill by Day and Gender')
plt.xlabel('Day')
plt.ylabel('Total Bill')
plt.show()
```

![image](https://github.com/laakshit-D/EXNO-6-DS/assets/119559976/f57dee54-b821-4087-b7c6-7c6cc4df10ce)

```py
tit=pd.read_csv("/content/titanic_dataset.csv")
tit
```

![image](https://github.com/laakshit-D/EXNO-6-DS/assets/119559976/bf2035d1-4bd5-499c-81d8-0817cd5abcf7)

```py
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow')
plt.title('Fare of Passengers by Embarked Town')
plt.xlabel('Embarked Town')
plt.ylabel('Fare')
plt.show()
```

![image](https://github.com/laakshit-D/EXNO-6-DS/assets/119559976/44489042-e5f2-4af6-96c7-50d80755d310)

```py
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass')
plt.title('Fare of Passengers by Embarked Town, Divided by Class')
plt.xlabel('Embarked Town')
plt.ylabel('Fare')
plt.show()
```

![image](https://github.com/laakshit-D/EXNO-6-DS/assets/119559976/fd72127b-fe11-4c7e-982b-84553fc8ef55)

**SCATTER PLOT**
```py
import seaborn as sns

tips = sns.load_dataset('tips')

sns.scatterplot(x= 'total_bill', y='tip', hue='sex',data=tips)

plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```

![image](https://github.com/laakshit-D/EXNO-6-DS/assets/119559976/96af5dba-0d1b-49d4-84b0-a77d7b793bc1)

**VIOLIN PLOT**
```py
sns.violinplot(x='Age', y='Fare', data=tit)
plt.title('Violin Plot of Age vs. Fare')
plt.xlabel('Age')
plt.ylabel('Fare')
plt.show()
```

![image](https://github.com/laakshit-D/EXNO-6-DS/assets/119559976/a1981834-fb3b-430c-8498-1941fd312502)

**HISTOGRAM**
```py
import seaborn as sns
import numpy as np
import pandas as pd

np.random.seed(0)
marks = np.random.normal(loc=70, scale=10, size=100)

# Generating dataset of random numbers
np.random.seed(1)
num_var = np.random.randn(1000)
num_var = pd.Series(num_var, name = "Numerical Variable")
num_var
```

![image](https://github.com/laakshit-D/EXNO-6-DS/assets/119559976/96b4d67d-10e9-463d-b054-654d134f502d)

```py
sns.histplot(num_var, kde=True)
plt.title('Histogram of Numerical Variable')
plt.xlabel('Value')
plt.ylabel('Frequency')
plt.show()
```

![image](https://github.com/laakshit-D/EXNO-6-DS/assets/119559976/588a1b19-be05-497c-8c1f-c6fb36ce256b)

```py
sns.histplot(data=tit, x='Pclass', hue='Survived', kde=True)
plt.title('Histogram of Pclass with Survived as Hue')
plt.xlabel('Pclass')
plt.ylabel('Frequency')
plt.show()
```

![image](https://github.com/laakshit-D/EXNO-6-DS/assets/119559976/aece92b0-6dc7-4027-b424-9109701967cc)

## Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
