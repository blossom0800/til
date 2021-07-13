# NUMBER OF ROWS
`SELECT COUNT(*) FROM 테이블명;`

# NUMBER OF COLUMNS
```
SELECT COUNT(*)
  FROM INFORMATION_SCHEMA.COLUMNS
 WHERE table_catalog = 'DB 이름' -- the database
   AND table_name = '테이블 이름'
```
(Source: https://stackoverflow.com/questions/658395/find-the-number-of-columns-in-a-table)
