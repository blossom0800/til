# order by는 select 구문의 alias에서 정의된 이름으로 작성되어야 함
 - 예시
    ```
    SELECT department_id, job_id jobs
    FROM employees
    WHERE department_id = 60
    UNION 
    SELECT department_id, job_id
    FROM employees
    WHERE department_id = 90
    ORDER BY JOBS;
    ``` << 여기에서 job_id가 되면 오류 발생
