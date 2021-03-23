/ 뒤에글자 sorting

조건

인형 이름이 word와 정확히 일치하는 인형을 가장 먼저 검색합니다.
인형 이름에 word가 많이 포함될수록 먼저 검색합니다.
인형 이름에 포함된 word 개수가 같으면 인형 이름 안에 word가 앞에 있을수록 먼저 검색합니다.
만약 첫 번째 word가 등장하는 위치가 같다면 계속해서 다음 word의 위치를 비교합니다.
예를 들어 word가 "AA"이고 인형 이름이 "AABAA", "AABBAA" 인 경우, "AABAA"를 먼저 검색합니다.
검색 순위가 같다면 ID 가 더 작은 인형을 먼저 나열합니다.
인형 이름에서 word를 찾을 때 알파벳은 한 번씩만 셉니다. 예를 들어, 인형 이름이 "AAA"이고 word가 "AA"이면 word가 맨 앞에 하나 포함되어있는 것입니다. 인형 이름의 2번째 A를 두 번 세어 word가 2번 포함되어 있는 것이 아님을 유의하세요.

```python
['ROOTA/AA', 'ROOTB/AA', 'ROOTA/BAAAAAAA', 'ROOTA/AAAAA', 'ROOTA/AAAA', 'ROOTA/AABAA', 'ROOTA/CAA', 'ROOTA/BBAA']

print(sorted(answers, key=lambda a: (
            -1 if a.split('/')[-1] == q else 1,
            -a.split('/')[-1].count(q),
            [a.split('/')[-1].index(q, i) for i in range(a.split('/')[-1].count(q))],
            idxs.index(a.split('/')[-1]),
        )))

발생한 인덱스 숫자
[[0], [0, 3], [0, 1], [0, 1], [1, 1, 2], [2], [1], [0]]
[[0], [0], [0, 1], [0, 1], [0, 3], [1], [1, 1, 2], [2]]
```

