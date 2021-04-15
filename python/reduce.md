# Why different value is returned????

```python
ans = reduce(lambda a, b: a * b, [v + 1 for v in divs.values()])
ans = reduce(lambda a, b: (a+1) * (b+1), divs.values())
```
[2,1]은 같은 값
[2,2,3,1,1,1,1]은 다른 값 리턴함

이유 : a+1 + b+1 => ((a*1)*(b+1)+1)*(c+1)이 되어버림