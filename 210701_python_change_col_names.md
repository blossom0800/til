# 1. 결측치가 있는 df를 백분위로 나타내기
    `df.isnull().mean() * 100`
# 2. Series를 df 형태로 만들기
    `df_isnull = pd.DataFrame(df.isnull().mean() * 100)`
# 3. 0인 컬럼명에 이름 붙여주기
    `df_isnull = pd.DataFrame(df_isnull).rename(columns = {0:'Percentage'})`
# 4. Percentage라는 컬럼명 기준으로 정렬
    `df_isnull.sort_values(ascending = False, by = ['Percentage'])`
