# 종목명이 0XXXXX로 시작해야 하는데(object type) 숫자형으로 인식해서 XXXXX만 불러올 경우
 - pd.read_csv로 읽어올 때 object type을 지정
 - e.g.) `pd.read_csv("파일명.csv", dtype = {"대상컬럼" : object})
