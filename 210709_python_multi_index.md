# Multi Index의 예시
## Input
`df.index`

## Output
`MultiIndex([('고시원', '강남구')\
              ('고시원', '강동구')\
              ...
              ('학원-입시', '중랑구')`
              
## Note
 - 이 때 MultiIndex는 컬럼보다 접근하기 어려움으로 시각화 하기 전에 reset_index를 해주는게 좋음

## Input - 1
`df.reset_index()`

## Output - 1
 - 숫자 인덱스가 다시 생김
