# FROM 절 아래에 들어가는 SELECT 문에는 ;가 들어가면 안됨
# FROM 이하의 하위 테이블에는 각각의 변수 명을 설정해주어야 상위 SELECT문에서 a.변수명, b.변수명 이런 식으로 쓸 수 있음. 이렇게 해야 돌아감.
  . TO_CHAR('DATES', 'YYYY-MM') (X) -> TO_CHAR('DATES', 'YYYY-MM') YEAR_MON으로 지정 후 맨 상단 SELECT 문에서 a.YEAR_MON 이런 식으로 지정해줘야 함
# DECODE 함수 remind
  . DECODE(조건대상, 조건 A, 반환 A, 조건 B) -> 반환 B를 쓰지 않아도 그대로 조건 B가 반환됨
  . e.g. `DECODE(B.CONTINENT_NEW, 0, 0, A.COUNTRY_NEW/B.CONTINENT_NEW)`
