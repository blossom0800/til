# Input

```
rank_a = df_company_a.groupby(['category'])['amount'].sum().sort_values(ascending = False).reset_index()
rank_a['rank'] = rank_a.index # a에 index를 부여해서 rank라는 열을 만듦
rank_a['card_company'] = 'a' # card_company라는 열에 전부 'a'라고 넣어줌
rank_a
```

# Output

```
	category	amount	rank	card_company
0	식음료	2,520,099,387.00	0	a
1	도매업	924,283,436.00	1	a
2	패션	871,291,290.00	2	a
3	교육	820,076,631.00	3	a
4	미용	416,082,168.00	4	a
5	스포츠_취미	362,751,410.00	5	a
6	쇼핑	332,585,103.00	6	a
7	기타서비스업	285,513,889.00	7	a
8	자동차	246,811,661.00	8	a
9	기타	113,655,016.00	9	a
10	여행	92,957,553.00	10	a
11	통신_전자	91,344,342.00	11	a
12	가정_생활	67,201,315.00	12	a
13	의료	60,428,962.00	13	a
14	웨딩	48,247,910.00	14	a
15	제조업	42,667,807.00	15	a
16	유아_아동	33,510,103.00	16	a
```

