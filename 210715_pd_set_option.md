# `7.047700e-01` 이런 식으로 describe 할 때 알 수 없는 숫자로 나온다면 -> `pd.set_option`
 - `pd.set_option('display.float_format', lambda x: '%.3f' % x)`
 - 소수점으로 바꿔줌 / 소수점 셋째자리까지 나옴 `0.705`
