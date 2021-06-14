(Source: https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html)

# 새로운 Series를 만들 때
 - s = pd.Series([1, 3, 5, np.nan, 6, 8])
 - Series는 반드시 맨 앞이 대문자여야 함. series~로 입력하면 에러 발생

# date
 - dates = pd.date_range("20210614", periods = 6)
 - 결과 : 
   DatetimeIndex(['2021-06-14', '2021-06-15', '2021-06-16', '2021-06-17',
               '2021-06-18', '2021-06-19'],
              dtype='datetime64[ns]', freq='D')

# Creating a DataFrame by passing a NumPy array, with a datetime index and labeled columns;
 - df = pd.DataFrame(np.random.randn(6, 4), index=dates, columns=list("ABCD"))
 - 내가 이해한 것: Column 6개, Row 4개인 테이블을 랜덤하게 만들기 / Index는 date 순으로 / Column list는 "ABCD"로 넣기
 - 중간에 randn이라고 쓰여있는 부분 주의해서 타이핑할 것
 - 결과 : 
    A	B	C	D
    2021-06-14	1.144339	1.482703	1.248090	0.992554
    2021-06-15	-0.689066	-0.366935	0.450213	0.469397
    2021-06-16	-2.773640	0.858666	0.722833	0.188153
    2021-06-17	0.569096	-0.109229	1.531940	0.320308
    2021-06-18	-0.162143	-0.844427	-0.700371	-0.802430
    2021-06-19	1.017551	-1.158533	-0.506960	0.671127
    
# Dict 형태의 데이터를 series 형태의 DataFrame으로 바꾸기
 - df2 = pd.DataFrame(
    {
        "A": 1.0,
        "B": pd.Timestamp("20210614"),
        "C": pd.Series(1 , index=list(range(4)), dtype="float64"),
        "D": np.array([3] *4 , dtype="int64"),
        "E": pd.Categorical(["test", "train", "test", "train"]),
        "F": "foo"    
    })

   df2
 - 결과: (표 형태로)
   
    A	B	C	D	E	F
    0	1.0	2021-06-14	1.0	3	test	foo
    1	1.0	2021-06-14	1.0	3	train	foo
    2	1.0	2021-06-14	1.0	3	test	foo
    3	1.0	2021-06-14	1.0	3	train	foo
 - 실험: index=list(range(4))를 다른 숫자로 넣으면> 오류 발생, np.array([3]*4)의 4를 다른 숫자로 넣으면> 오류 발생
 - 
 - arrays must all be same length



















