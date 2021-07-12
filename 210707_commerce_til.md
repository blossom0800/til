# Platform
  - Database : 상품데이터, 유저데이터, 판매자데이터, 플랫폼 카테고리 분류 데이터, 로그 데이터
  - 비즈니스 애널리틱스(리포트, 보고서), 상품 매입 전략 수립, 개인화 타겟 마케팅, 물류 배송 예측 모델링, 상품 검색 서비스, 개인화 추천 서비스

# 상품 매입 전략
  - 아소트 추정: 사이즈, 컬러, 품번 별 판매량 예측
  - 트렌드 예측: 시즌 유행할 상품, Google/Naver에서 제공하는 키워드 서비스, SNS 크롤링으로 트렌드 예측
  - 최대 마진 모델링

# 정형/비정형
  - 정형데이터 - 숫자로 정해놓고 쓸 수 있는 것
  - 비정형 - 영어문장..컴퓨터가 테이블 형태로 바로 인식할 수 없음

# 텍스트의 벡터 표현
  - Count-Dict
  - One hot 인코딩
  - Bag of words  
  - TF_IDF
  - Word2Vec

# 결측값의 처리 방법
  - 단순 삭제 - bias를 없앨 수 있는 장점이 있지만 질 좋은 데이터를 놓칠 수 있다는 단점도 존재함
  - 통계적 보충 - 평균값, 중앙값, 최빈값 등의 값으로 어림잡아 채워 넣음. bias가 생길 수 있다는 단점도 존재함
  - 추정값을 사용 - 회귀 분석, 혹은 더 정교한 모델링을 통해 값을 추정해서 채워넣는 방법으로 거의 안씀