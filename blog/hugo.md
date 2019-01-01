# Hugo

- Static Web Generator의 한 종류 (Jekyll, Hexo, ...)

##  Hugo site 생성
~~~
hugo new site [site name]
~~~
이렇게 하면 []안의 이름을 가진 사이트 폴더가 생성된다. 이 폴더 안을 살펴보면, 크게
- content 폴더 : 내용이 작성된다.
- themes 폴더 : hugo 테마가 저장된다.
- config.toml : hugo 설정 파일

로 구성된다.

## Hugo 테마 적용
hugo 테마를 검색해서 다운 받는다. 나는 https://themes.gohugo.io 사이트에서 받았다.
테마별로 자세한 사용방법이 명시되어있다.
theme 폴더 안에 저장하고 config.toml파일을 수정하는 방식이다.
