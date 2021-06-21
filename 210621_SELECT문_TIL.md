`SELECT a.employee_id, a.first_name || ' ' || a.last_name emp_names, b.*
FROM employees a,
job_history b
WHERE a.employee_id(+) = b.employee_id
ORDER BY 1;`

b.* >> b 테이블의 전체 컬럼을 선택하는 것
