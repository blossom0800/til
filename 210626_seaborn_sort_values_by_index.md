# Seaborn에서 빈도수 순으로 그래프를 보이게 하고 싶을 경우
  - 빈도수를 기준으로 정렬한 series를 먼저 만들고 .index를 붙여 인덱스값만 추출 -> 변수 할당
  - `df[df["컬럼명"].isin(위에서 정렬한 series)]`를 붙여서 새로운 df를 만들어줌
  - sns.countplot(data = 새로 만든 df, y = "~", order = 할당한 변수 명)
