# 마크다운 문법

마크다운 새로운 문법을 검색할 때 마다 추가한다.

- 수평선
~~~makrdown
    ---
~~~
---

- 코드블럭
~~~markdown
    ~~~[사용언어]
    내용
    ~~~
~~~
ex)
~~~markdown
    ~~~python
    def hello_world():
        print 'hello world!'
    ~~~
~~~
~~~python
    def hello_world():
        print 'hello world!'
~~~

- 코드블럭 전체가 들여쓰기 될 수 없을까?


- 취소선
~~~markdown
    ~~취소할내용~~
~~~
~~취소할내용~~

- 이미지
  - 다른 방법도 있지만 사이즈 지정을 위해 이 방식을 택한다.
~~~markdown
    <img src="./img/01.png" width="400">
~~~