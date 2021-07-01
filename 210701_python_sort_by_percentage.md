# 1. 결측치가 있는 df를 백분위로 나타내기
    `df.isnull().mean() * 100`
# 2. Series를 df 형태로 만들기
    `pd.DataFrame(df.isnull().mean() * 100)`
# 3. 백분위 기준으로(내림차순) 정렬하기
    `pd.DataFrame(df.isnull().mean() * 100).sort_values(ascending = False, by = ['percentage'])`
# TIL
    - sort_values() 안에 들어가는 by는 index나 columns만 되는 줄 알았는데 ['percentage']로 정렬하는 방법도 있었음`
