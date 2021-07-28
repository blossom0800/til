# category의 리스트에는 들어있고 "기타"는 뺀 df_city 찾기

`df_city = df_city[(df_city["category"].isin(category_list))&(df_city["city"] != "기타")]`
