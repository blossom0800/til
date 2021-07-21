# str.split 상세
  >> `df.str.split(" >", n = None, expand = True)`
  >> '>'을 기준으로 숫자 제한 없이(n = None) 나눠줘, Df 형태로 반환해줘(expand = True)

# 평점 컬럼에서 숫자만 빼내기
  >> `df['average_review_rating'].str.split(' out', n = None, expand = True)[0]`
  >> `review_rating = review_rating.astype(float)`
