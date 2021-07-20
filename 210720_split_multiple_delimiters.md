# Input
`df['price']`

# Output
```
0        £3.42
1       £16.99
2        £9.99
3       £39.99
4       £32.19
         ...  
9995    £22.95
9996    £39.99
9997    £43.99
9998    £49.81
9999    £21.20
Name: price, Length: 10000, dtype: object
```

# Input
`df['price'] = df['price'].str.replace('-', '£')` # 중간의 범위값 '-'까지 '£'로 통일함 >> 한번에 '£'로 split 하기 위해

# Output
```
0        £3.42
1       £16.99
2        £9.99
3       £39.99
4       £32.19
         ...  
9995    £22.95
9996    £39.99
9997    £43.99
9998    £49.81
9999    £21.20
Name: price, Length: 10000, dtype: object
```

# Input
```
df_price = df['price'].str.split('£', n = None, expand = True)
df_price
```

# Output
```
0	    1   	2	    3
0		3.42	None	None
1		16.99	None	None
2		9.99	None	None
3		39.99	None	None
4		32.19	None	None
...	...	...	...	...
9995		22.95	None	None
9996		39.99	None	None
9997		43.99	None	None
9998		49.81	None	None
9999		21.20	None	None
10000 rows × 4 columns
```





