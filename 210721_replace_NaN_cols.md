(Source: https://stackoverflow.com/questions/18689823/pandas-dataframe-replace-nan-values-with-average-of-columns)

# Input
```
df_price
```

# Output
```
	   1	  3
0	3.42	None
1	16.99	None
2	9.99	None
3	39.99	None
4	32.19	None
...	...	...
9995	22.95	None
9996	39.99	None
9997	43.99	None
9998	49.81	None
9999	21.20	None
```

# Input
```
df_price[3].fillna(df_price[1], inplace = True)
df_price
```
*Note - df_price[3].fillna(df_price[1], inplace = True)을 df_price[3]에 담으면 다시 NaN이 되었음

# Output
```
	  1	   3
0	3.42	3.42
1	16.99	16.99
2	9.99	9.99
3	39.99	39.99
4	32.19	32.19
...	...	...
9995	22.95	22.95
9996	39.99	39.99
9997	43.99	43.99
9998	49.81	49.81
9999	21.20	21.20
```
