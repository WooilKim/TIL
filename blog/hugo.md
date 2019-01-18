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

## Hugo template syntax

~~~toml
 {{ .Site.Data.xxx.yyy }}
 ~~~
 theme를 수정하기 위해 코드를 보다보면 위와같은 구조의 문법이 많이 보인다. 
 Data는 블로그 폴더 안의 data폴더를 의미하고 xxx라는 파일의 yyy항목을 가져온다.
 예를 들어 현재 사용하고 있는 Icarus theme를 처음 사용할 때 좌측 profile에서 (모바일에서는 보이지 않는다) follow 버튼에 follow라는 글씨가 써지지 않았다.
 데모 페이지에서는 뜨는데 왜 안뜨는지 살펴보기 위해 테마 폴더 안의 examplesite 폴더를 살표보았다.
 
 examplesite 폴더에 들어가 보니 data 폴더가 있고 이 안에 l10n.toml파일이 있었다.
 내 블로그 폴더 안의 data 폴더에 l10n.toml파일을 복사 붙여넣기 하니 제대로 작동한다.

theme/icarus/layout/profile.html을 살표보면

~~~html
{{ with .Site.Params.profile.follow_button }}
    <a id="follow" href="{{ . }}">
        {{with $.Site.Data.l10n.profile.follow_button}}{{.}}{{end}}
    </a>
{{ end }}
~~~

이 부분이 follow 버튼을 그리는 부분인데, l10n파일 안의

~~~toml
 [profile]
    follow_button = "Follow"
    tags = "Tags"
    posts = "Posts"
~~~

에서 ".Site.Params.profile.follow_button"는 config.toml 파일의 

~~~toml
[params.profile]
    follow_button = "https://github.com/wooilkim"
~~~
내용을, 

~~~toml
{{with $.Site.Data.l10n.profile.follow_button}}{{.}}{{end}}
~~~
는 l10ml파일안의 내용을 가져온다.

{{ . }}는 앞에 with에서 가져온 내용을 의미하는 것 같다.

