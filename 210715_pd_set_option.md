# `7.047700e-01` 이런 식으로 describe 할 때 알 수 없는 숫자로 나온하면 -> `pd.set_option`
`pd.set_option('display.float_format', lambda x: '%.3f' % x)`
