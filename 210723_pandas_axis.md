(Source: https://datatofish.com/sum-columns-rows-dataframe/)

# df.sum(axis = 0) : sum_column
```
import pandas as pd

data = {'Month': ['Jan ','Feb ','Mar ','Apr ','May ','Jun '],
        'Bill Commission': [1500,2200,3500,1800,3000,2800],
        'Maria Commission': [3200,4100,2500,3000,4700,3400], 
        'Jack Commission': [1700,3100,3300,2700,2400,3100]
        }

df = pd.DataFrame(data,columns=['Month','Bill Commission','Maria Commission','Jack Commission'])
sum_column = df.sum(axis=0)
print (sum_column)
```

# df.sum(axis = 1) : sum_row
```
import pandas as pd

data = {'Month': ['Jan ','Feb ','Mar ','Apr ','May ','Jun '],
        'Bill Commission': [1500,2200,3500,1800,3000,2800],
        'Maria Commission': [3200,4100,2500,3000,4700,3400], 
        'Jack Commission': [1700,3100,3300,2700,2400,3100]
        }

df = pd.DataFrame(data,columns=['Month','Bill Commission','Maria Commission','Jack Commission'])
sum_row = df.sum(axis=1)
print (sum_row)
```
