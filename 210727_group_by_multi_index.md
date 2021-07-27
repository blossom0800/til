(Source: https://stackoverflow.com/questions/35414625/pandas-how-to-run-a-pivot-with-a-multi-index)

# pivot table에서 multi index를 입력하려고 함 -> You can group and then unstack.

```
>>> df.groupby(['year', 'month', 'item'])['value'].sum().unstack('item')
item        item 1  item 2
year month                
2004 1          33     250
     2          44     224
     3          41     268
     4          29     232
     5          57     252
     6          61     255
     7          28     254
     8          15     229
     9          29     258
     10         49     207
     11         36     254
     12         23     209
```


# OR use `pivot_table`

```
>>> df.pivot_table(
        values='value', 
        index=['year', 'month'], 
        columns='item', 
        aggfunc=np.sum)
item        item 1  item 2
year month                
2004 1          33     250
     2          44     224
     3          41     268
     4          29     232
     5          57     252
     6          61     255
     7          28     254
     8          15     229
     9          29     258
     10         49     207
     11         36     254
     12         23     209
```
