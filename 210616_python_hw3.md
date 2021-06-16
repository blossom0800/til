# count, sum, mean 등 계산하는 함수를 여러 개 쓰려면 >> agg를 써주면 됨
 - `df.groupby(['df1'])['df2'].agg(['count','mean', 'sum'])`

# Pivot Table
 - `pd.pivot_table(data=df, index="row값", values="컬럼")`
