# css 선택자

## #name

id 속성을 가져온다.

## .name

class 속성을 가져온다.

## 짝수 홀수 선택자

~~~css
table tr:nth-child(odd) {
  background: red;
}

table tr:nth-child(even) {
  background: blue;
}
~~~

빨강 파랑 번갈아가며 색칠해진 표