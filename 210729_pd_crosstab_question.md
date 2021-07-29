# Pandas 설명에 다르면 pd.crosstab은 두 변수의 빈도수를 나타낸다고 함

# Input
`len(df_company_a['category'] == '식음료') / len(df['category'] == '식음료')`

# Output
`0.27888728524925904`

# Input
`pd.crosstab(df.card_company, df.category, normalize = 1) * 100`

# Output
`29.77` (전체가 df로 나오지만 해당 값은 29.77)
