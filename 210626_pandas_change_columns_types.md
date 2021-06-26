# 우선 type을 바꾸고 싶은 컬럼명(e.g.년도)를 컬럼으로 놓는다. index 값이라면 df.T로 바꿔줌
# 그 다음 df.columns.astype(int)로 바꿔주고  df.columns로 재할당!! (꼭 columns를 붙여줘야 원래 df 그대로 쓰되 컬럼 타입만 바꿀 수 있음)
