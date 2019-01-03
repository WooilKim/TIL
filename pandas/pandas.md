# pandas

## merge

- parameter
  - DataFrame A
  - DataFrame B
  - on : key columns
  - how : outer, inner, left, right

~~~python
pd.merge(df, tmp[left_keys],
                  on=['yearID', 'playerID'], how='outer')
~~~
겹치는 컬럼이 있을 때는 column_x, column_y로 생기게 된다.
이 때는 combine_first 함수를 사용한다.
~~~python
for c in columns:
    df[c + '_x'] = df[c + '_x'].combine_first(df[c + '_y'])
    df = df.drop(columns=[c + '_y'])
    df = df.rename(columns={c + "_x": c})
return df
~~~