# Hugo + github 블로그 생성

- Repository 생성
  - 배포용
    - "[github 계정이름].github.io"라는 이름을 가진 repository 생성시 [github 계정이름].github.io 라는 주소의 블로그가 생성된다. ex) wooilkim.github.io
  - 블로그 구축 파일 관리
    - 블로그 구축 파일을 관리할 repository를 생성. ex) blog

- 테마
  - Jekyll, Hexo, Hugo 등 여러 가지 테마가 존재 하고, 각각의 장단점이 있다.
  - hugo 테마를 사용하기로 결정

- hugo 설치
  - Mac

~~~
Brew install hugo
~~~

- hugo 블로그 생성하기
~~~
hugo new site [blog 폴더 이름]
ex) hugo new site blog
~~~

- blog Repository 연결하기
git 연결은 Atlassian의 Sourcetree 프로그램을 이용했다.

<img src="./img/01.png" width="400">