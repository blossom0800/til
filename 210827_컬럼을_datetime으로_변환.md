`pd.to_datetime(df['컬럼명'])`

## 참고
### Error Message
 - `ValueError: Tz-aware datetime.datetime cannot be converted to datetime64 unless utc=True`
 - 해결 : `df_res['DateTime'] = pd.to_datetime(df_res['DateTime'], utc=True)`

(Source: https://stackoverflow.com/questions/55385497/how-can-i-convert-my-datetime-column-in-pandas-all-to-the-same-timezone)
