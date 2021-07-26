(Source: https://stackoverflow.com/questions/13413590/how-to-drop-rows-of-pandas-dataframe-whose-value-in-a-certain-column-is-nan)
# 오늘의 교훈: `Don't drop, just take the rows where EPS is not NA:`

`df = df[df['EPS'].notna()]`

