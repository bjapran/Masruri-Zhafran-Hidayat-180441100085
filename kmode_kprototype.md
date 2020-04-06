# Data Clustering

Analisa data dengan k-modes dan k-prototype diimplementasikan dengan bahasa python

Nama : Masruri Zhafran Hidayat

NIM : 180441100085

##### **K-Modes**

source data : https://www.kaggle.com/llopesolivei/blackfriday

source code python :

```python
import os
print(os.listdir("../input"))
from scipy import stats
from sklearn import metrics
from sklearn.preprocessing import MinMaxScaler
import matplotlib.pyplot as plt
from kmodes.kmodes import KModes
df_allData=pd.read_csv('../input/BlackFriday.csv')
print(df_allData.sample(n=2))
```

output : 

```
 User_ID Product_ID   ...    Product_Category_3 Purchase
287098  1002156  P00146142   ...                  15.0     8243
498007  1004656   P0097242   ...                   NaN    19509

```

##### **K-Prototype**

source data : https://gist.github.com/armgilles/194bcff35001e7eb53a2a8b441e8b2c6

source code :

```python
library(ggplot2)
library(readr)
system("ls ../input")
pokemon <- read.csv('../input/Pokemon.csv', header = T)
head(pokemon)
colnames(pokemon) <- c("number", "name", "type1", "type2", "total", "hp", 
                       "attack", "defense", "sp.atk", "sp.def", "speed", 
                       "generation", "legendary")
sum(is.na(pokemon))
```

output :

| X.   | Name                  | Type.1 | Type.2 | Total | HP   | Attack | Defense | Sp..Atk | Sp..Def | Speed | Generation | Legendary |
| :--- | :-------------------- | :----- | :----- | :---- | :--- | :----- | :------ | :------ | :------ | :---- | :--------- | :-------- |
| 1    | Bulbasaur             | Grass  | Poison | 318   | 45   | 49     | 49      | 65      | 65      | 45    | 1          | False     |
| 2    | Ivysaur               | Grass  | Poison | 405   | 60   | 62     | 63      | 80      | 80      | 60    | 1          | False     |
| 3    | Venusaur              | Grass  | Poison | 525   | 80   | 82     | 83      | 100     | 100     | 80    | 1          | False     |
| 3    | VenusaurMega Venusaur | Grass  | Poison | 625   | 80   | 100    | 123     | 122     | 120     | 80    | 1          | False     |
| 4    | Charmander            | Fire   |        | 309   | 39   | 52     | 43      | 60      | 50      | 65    | 1          | False     |
| 5    | Charmeleon            | Fire   |        | 405   | 58   | 64     | 58      | 80      | 65      | 80    | 1          | False     |