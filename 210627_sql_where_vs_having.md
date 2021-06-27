# 집계함수 외의 조건은 where절
# 집계함수가 반환하는 값에 대한 조건은 having 절

e.g.)


`SELECT TO_CHAR(a.order_date, 'YYYY-Q') quarter

        ,d.brand_name
        
        ,SUM(b.quantity * b.list_price) order_amt
        
 FROM orders
 
 (JOIN절 생략)

 WHERE a.order_date BETWEEN TO_DATE('2018-01-01', 'YYYY-MM-DD') AND TO_DATE('2018-12-31', 'YYYY-MM-DD'), d.brand_name

 GROUP BY TO_CHAR(a.order_date, 'YYYY-Q')
 
 HAVING SUM(b.quantity * b.list_price) >= 10000;`
