# Inline 쿼리로 From 절 이하에 해당 조건을 만족하는 테이블 생성 후(이 경우엔 쿼터 별 대륙 별 확진자), 본 SELECT 문에서 연산함수+CASE WHEN을 같이 써줌
```
SELECT CONTINENT,
        SUM(CASE WHEN QUARTER = '1' THEN CASES ELSE 0 END) Q1,
        SUM(CASE WHEN QUARTER = '2' THEN CASES ELSE 0 END) Q2,
        SUM(CASE WHEN QUARTER = '3' THEN CASES ELSE 0 END) Q3,
        SUM(CASE WHEN QUARTER = '4' THEN CASES ELSE 0 END) Q4
FROM (SELECT TO_CHAR(dates, 'q') quarter, 
      continent,
      NVL(SUM(new_cases),0) cases,
      NVL(SUM(new_deaths),0) death_num
      FROM covid19_test
      WHERE TO_CHAR(dates, 'YYYY') = '2020'
      AND continent IS NOT NULL
      GROUP BY TO_CHAR(dates, 'q'), continent)
GROUP BY CONTINENT;
```
