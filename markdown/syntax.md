# 마크다운

## 문법

마크다운 새로운 문법을 검색할 때 마다 추가한다.

### 수평선

#### 코드
~~~makrdown
---
~~~
#### 사용 결과
---

### 코드블럭

#### 코드

~~~markdown
    ~~~[사용언어]
    내용
    ~~~
~~~


> [사용언어]에 들어갈 수 있는 언어 종류 [Linguist](https://github.com/github/linguist/blob/master/lib/linguist/languages.yml)

#### - 예제

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

### 링크

~~~markdown
    [링크내용](링크주소)
~~~

[링크내용](링크주소)

### 취소선

~~~markdown
    ~~취소할내용~~
~~~

~~취소할내용~~

### 이미지

다른 방법도 있지만 사이즈 지정을 위해 이 방식을 택한다.

~~~markdown
    <img src="./img/01.png" width="400">
~~~

- Todo
  - 코드블럭 전체가 들여쓰기 될 수 없을까?