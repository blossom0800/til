# Input
`order_df.groupby('city').agg({'order_id' : ['count'], 'lat' : ['mean'], 'lng' : ['mean']})`


# Output
```
                     order_id	lat	lng
                     count	mean	mean
city			
* cidade	          2	  -25.572	-49.334
...arraial do cabo	37	-22.969	-42.030
abadia dos dourados	78	-18.474	-47.408
abadiania	          17	-16.194	-48.708
abadiânia	          7	  -16.194	-48.712
...	...	...	...
álvaro de carvalho	4	  -22.079	-49.721
áurea	              4	  -27.695	-52.055
ângulo	            16	-23.195	-51.917
érico cardoso	      1	  -13.393	-42.134
óleo	              4	  -22.940	-49.340
```
