# 2회차 과제 풀이

# Seaborn에서는 dataset을 불러올 수 있음
 - pd.read_csv("URL")로 불러오는 방법도 있음

# 결측치를 찾을 때는 반드시 df.isnull()
 - df == np.nan을 사용할 수는 없음. 값이 왜곡되어서 나옴.

# df[“alive”].value_counts() 
 - 한 개의 빈도수에 대해 그룹값을 구할 때에는 groupby보다 value_counts를 사용하는 것을 추천함.

# object 타입의 요약값
 - df.describe(include = 'object)
 - top은 unique 값 중 빈도수가 가장 많은 것 / freq는 최빈값(top)에 대한 빈도수를 센 것

# fare가 500보다 큰 값 계산하기
 - df[df[“fare”] > 500][“fare”] / df.loc[df[“fare”] > 500, “fare”]
 - 둘 다 동일한 결과값이 나오지만 후자가 훨씬 빠름, 앞에 %timeit 을 붙여보면 실행하는데 소요되는 시간이 나옴.
 - **LOC를 자주 활용할 것

# 변수에 담아서 계산하기
`Pclass_3 = df[“pclass”] == 3
embarked_q = df[“embarked”] == “Q”
df.loc[pclass_3 & embarked_q, “fare”].mean()` >> 나중에 오류가 발생해도 빨리 찾을 수 있음

# 결측치를 0으로 채우면 평균이 확 낮아짐
`Df[“age_fill”] = Df[“age”].fillna(0)
Df[“age_fill”].mean()`

# 컬럼 그룹화 & 갯수 카운트
`Df[“deck”].value_counts().sort_index()` >> groupby보다 훨씬 쉽게 구할 수 있음

# 역순 정렬
`df[“age”].sort_values(ascending = False).head()`
