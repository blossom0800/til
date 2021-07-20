# '>'로 구분된 카테고리 구분 나누기


```
0       [Hobbies ,  Model Trains & Railway Sets ,  Rai...
1       [Hobbies ,  Model Trains & Railway Sets ,  Rai...
2       [Hobbies ,  Model Trains & Railway Sets ,  Rai...
3       [Hobbies ,  Model Trains & Railway Sets ,  Rai...
4       [Hobbies ,  Model Trains & Railway Sets ,  Rai...
                              ...                        
9995    [Hobbies ,  Collectible Figures & Memorabilia ...
9996           [Characters & Brands ,  Star Wars ,  Toys]
9997    [Novelty & Special Use ,  Novelty ,  Accessori...
9998    [Hobbies ,  Collectible Figures & Memorabilia ...
9999           [Characters & Brands ,  Star Wars ,  Toys]
Name: amazon_category_and_sub_category, Length: 10000, dtype: object
```
# Input
category.str.split(">", n = None, expand = True).rename(columns = {0: 'Lv1', 1: 'Lv2', 2: 'Lv3', 3: 'Lv4', 4: 'Lv5'})

# Output
```
	  Lv1	   Lv2	  Lv3	                     Lv4	            Lv5
0	Hobbies	Model Trains & Railway Sets	Rail Vehicles	Trains	None
1	Hobbies	Model Trains & Railway Sets	Rail Vehicles	Trains	None
2	Hobbies	Model Trains & Railway Sets	Rail Vehicles	Trains	None
3	Hobbies	Model Trains & Railway Sets	Rail Vehicles	Trains	None
4	Hobbies	Model Trains & Railway Sets	Rail Vehicles	Trains	None
...	...	...	...	...	...
9995	Hobbies	Collectible Figures & Memorabilia	Collectible Props & Memorabilia	None	None
9996	Characters & Brands	Star Wars	Toys	None	None
9997	Novelty & Special Use	Novelty	Accessories	Buttons & Pins	None
9998	Hobbies	Collectible Figures & Memorabilia	Collectible Props & Memorabilia	None	None
9999	Characters & Brands	Star Wars	Toys	None	None
```
