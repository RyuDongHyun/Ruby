## CSS

: 꾸미는 기능, Style Sheet

## HTML

: 많은 정보가 담겨 있는 문서, 정보의 구조만 담고있다.



## 정적 웹사이트, Static Website

:한가지 정보만을 주는 웹사이트, 비유) 정수기



## 동적 웹사이트, Dynamic Website

:다양한 정보를 요청에 따라 주는 웹사이트, 비유)생각하는 사람

- 여러가지 툴, 프레임워크 : rails 루비, django 파이썬 , symfony php,  node js express

css 옷을 입지 않으면 못생김



head : 문서의 성격을 알려줌



## HTML(Hyper Text Markup Language) 

### <!DOCTYPEhtml> : html이라는 문서다라는 것을 알려줌

### `<head></head>` : 문서의 성격을 알려줌

- `<title></title>` : 웹사이트 창 이름
- `<meta charset = "utf-8">`  : 한글사용을 위한 코드

### `<body></body>` : 문서의 내용

- `<h1>`~`<h6>`: 글자 크기

- `<a></a>` : 링크기능

- `<p></p>`: 글을 넣을 때

- `<div></div>`: 일반적인 개념으로 콘테츠를 넣을 수 있는 요소

    			구분할 때 씀

- `<img>(</img>)` : 이미지

- `<table></table>`: 표(요즘에는 잘 안쓰이는 추세, 커스터마이징 어려움)

- `<ul>`  `<li>해물파전</li>` `<li>피자</li>` `</ul>`  : 한 줄로 쓸 때



선택자와 선언

ex : p{color:red; padding : 5px}



### `<style></style>`

- 전체선택자 : *{  }

- 태그선택자 : 태그안에 직접, 조잡할 수 있다.

- Class 선택자 :  .으로 이름지정, 집합으로 공통적으로 설정할 때

- ID선택자 : 태그 안에 id를 설정 ex) `<p id="welcom">`, string 형태로 해야함. "" 잊지말 것!

  ​		#으로 이름지정,  특정 한 부분을 지정, 중복ㄴㄴ



​       





### HTML에 스타일 입히기

1. tag단위
2. css  `<style>`
3. css 파일 만들기
   - `<link rel = "stylesheet" type ="text/css" href="style.css">`
     - rel : relation(관계), type : 유형, href : hyper reference(참조)



# 코딩 원칙(DRY)

: Do not Repeat Yourself 



### 배경색깔 지정하기



margin

border

padding

content



### /

루트



## erb

: embedded ruby

: ruby code를 삽입할 수 있다.(html은 문서파일이기 때문에)

- `<%=   %>`사용
- @(변수이름) : 다른 클래스에서도 변수를 사용할 수 있도록



## Sinatra 웹 프로그래밍

글자 안에 따옴표를 넣을 시

"" 안에 '' 또는 '' 안에 ""





### Routing 라우팅

:route(길) 내주기



### params 

:Hash, sinatra에서 만든



### /:(변수이름)

: params[:(변수이름)]

- /다음에 들어오는 값을 String(문자)형태로 받는다.









