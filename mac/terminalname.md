# 터미널 이름 변경하기

터미널을 시작하면

~~~bash
wooil-MacBookPro:~ wooil$ 
~~~

이런 화면을 볼 수 있다.
이 부분에서 콜론(:) 왼쪽이 이름이고 우측은 경로이다.
위의 예제의 경우 "wooil-MacBookPro" 이름이다.
이 이름을 변경하려면 터미널에 아래와 같은 명령어를 입력하면 된다.

~~~bash
scutil --set HostName 새로운이름
~~~

터미널을 재시작하면 이름이 바뀌어 있다.