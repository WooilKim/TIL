동일한 개수로 이루어진 iterable한 객체들을 인수로 받아 묶어서 iterator로 반환

```python
z = zip([1, 2, 3], ('A', 'B', 'C'))
print(next(z)) # (1, 'A')
print(next(z)) # (2, 'B')
print(next(z)) # (3, 'C')
```

리스트( lists/tuples/iterables ) 를 연결
```python
from itertools import chain

c1 = [1, 2]
ca = ['A', 'B']
c = chain(c1, ca)
print(next(c)) # 1
print(next(c)) # 2
print(next(c)) # A
print(next(c)) # B
```