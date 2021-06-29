# 스칼라 / 인라인 서브쿼리로 같은 결과값 출력하기

 1) 스칼라 서브쿼리
    `SELECT EMPLOYEE_ID, FIRST_NAME, LAST_NAME, JOB_ID, SALARY,
    (SELECT AVG(SALARY) FROM EMPLOYEES B WHERE A.JOB_ID = B.JOB_ID GROUP BY JOB_ID) AVG
    FROM EMPLOYEES A;`
    
 2) 인라인 서브쿼리
    `SELECT * FROM EMPLOYEES WHERE ROWNUM < 5;
    SELECT A.EMPLOYEE_ID, A.FIRST_NAME, A.LAST_NAME, A.JOB_ID, A.SALARY, B.AVG_SALARY
    FROM EMPLOYEES A, (SELECT JOB_ID, AVG(SALARY) AVG_SALARY FROM EMPLOYEES  GROUP BY JOB_ID) B
    WHERE A.JOB_ID = B.JOB_ID;`
    
 3) 오늘의 TIL
    -- FROM 절의 서브쿼리 안에 WHERE 조건을 쓰지 않는다!!
    -- 스칼라 서브쿼리와 다르게 인라인 서브쿼리 절 안에는 일치시킬 컬럼'도' 들어가야 함 / 스칼라에는 SELECT문에 단일 컬럼만
