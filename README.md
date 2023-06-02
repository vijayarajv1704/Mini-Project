## Covid---Analysis
## Aim: 
To implement data science techniques in covid dataset
## Algorithm:
```
1.Import necessary packages.
2.Implement univariate techniques.
3.Implement bivariate techniques.
4.Implement data visualization techniques.
5.Close the program.
```
## Program with output:
```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
df=pd.read_csv("Covid Live.csv")
df
```
<img width="618" alt="image" src="https://user-images.githubusercontent.com/94185707/202077632-601dfe55-90ae-4f67-aad6-12e9b0a4c89d.png">

df.head()

<img width="577" alt="image" src="https://user-images.githubusercontent.com/94185707/202077939-2918a221-9f7d-4fc4-888e-3069d4b20cdd.png">

df.info()

<img width="227" alt="image" src="https://user-images.githubusercontent.com/94185707/202078074-749c6658-ba2b-44f2-9fd2-1ecf421453f6.png">

df.describe()

<img width="191" alt="image" src="https://user-images.githubusercontent.com/94185707/202078171-2f48d506-ade9-4996-8b06-32a451ccdc28.png">


### UNIVARIATE ANALYSIS

### BOXPLOT

sns.boxplot(y="newdeaths",data=df)

<img width="274" alt="image" src="https://user-images.githubusercontent.com/94185707/202078327-7c1ad33f-dcad-4724-966f-afe2f2205436.png">

df.boxplot()

<img width="349" alt="image" src="https://user-images.githubusercontent.com/94185707/202078494-862c8b01-7ec7-4226-8a8e-bb0a38d2fcf2.png">

### COUNTPLOT

sns.countplot(y="newdeaths",data=df)

<img width="285" alt="image" src="https://user-images.githubusercontent.com/94185707/202078539-ff425826-9200-4953-9013-7960b9959fef.png">

### HISTPLOT

sns.histplot(y="newdeaths",data=df)

<img width="281" alt="image" src="https://user-images.githubusercontent.com/94185707/202078613-386f1f1d-ada5-42c9-b124-db70a59219cf.png">


### MULTIVARIATE ANALYSIS

SCATTERPLOT

sns.scatterplot(df['country'],df['active cases'])

<img width="375" alt="image" src="https://user-images.githubusercontent.com/94185707/202078831-51d1e648-d529-4aa8-ae62-7c0b6b9d95f3.png">

plt.figure(figsize=(17,7))
sns.scatterplot(df['country'],df['active cases'],hue=df['Population'])

<img width="674" alt="image" src="https://user-images.githubusercontent.com/94185707/202078939-9d675d13-8b6d-4d2f-8322-3cbb3b34a955.png">

df.corr()

<img width="198" alt="image" src="https://user-images.githubusercontent.com/94185707/202079029-53a759e8-5f1f-4ab4-a8d4-f8354f518339.png">

### HEATMAP

sns.heatmap(df.corr(),annot=True)

<img width="289" alt="image" src="https://user-images.githubusercontent.com/94185707/202079105-2316e98c-3d68-4631-bd64-37290be8fe5d.png">


### data visualization

### POINTPLOT

sns.pointplot(x=df['totaldeaths'],y=df['newdeaths'])

<img width="281" alt="image" src="https://user-images.githubusercontent.com/94185707/202079932-e3370781-9686-449b-b494-d4084e7b6587.png">

### LINEPLOT

sns.lineplot(x=df['totalcases'],y=df['active cases'])

<img width="273" alt="image" src="https://user-images.githubusercontent.com/94185707/202080037-d205b110-84e8-4871-b4c8-b1051101d661.png">

### COUNTPLOT

sns.countplot(x=df['totaldeaths'])

<img width="278" alt="image" src="https://user-images.githubusercontent.com/94185707/202080164-1bc9dd9d-53a1-435b-adf5-376dd7cfac20.png">

### HISTPLOT

sns.histplot(x=df['totaldeaths'],data=df)

<img width="304" alt="image" src="https://user-images.githubusercontent.com/94185707/202080208-eece1b98-22b1-477a-9641-d2738a98f9ba.png">

### KDE PLOT

sns.kdeplot(x=df['newdeaths'],data=df)

<img width="293" alt="image" src="https://user-images.githubusercontent.com/94185707/202080259-31bdf3ca-16b6-4886-abf3-fdf761676a29.png">

## Result:
Thus above program is required for covid analysis and analyzed successfully.






