# HTML

### What is HTML?

: 웹페이지의 뼈대, 아무 웹페이지에 우클릭>>검사를 클릭하면 HTML 문서를 확인할 수 있다.

: Hyper Text Markup Language

- Markup language : 텍스트로 구조나 표현을 할 수 있다.
- Hyper Text : 하이퍼링크처럼 다른 텍스트로 링크해준다.



### HTML Anatomy

: HTML 구조

ex) `<p>Hello World!</p>`

- `<p>Hello World!</p>` : HTML element, HTML을 이루는 구성요소

- `<p>` : opening tag 
- `</p>`: closing tag
- `Hello World!` : content

** HTML Tag의 종류는 `<` 과 `>` 안의 내용으로 설정한다.



### The Body

:HTML의 핵심부분 중 하나. 오직 이 `<body></body>` 태그 안에 있는 부분만 화면에 나옴.



### HTML Structure

: parent - child (부모 - 자녀) 관계, 태그 안에 태그가 있을 때 안에 있는 태그를 child 바깥을 parent

: child tag는 한칸 씩 안쪽으로 들여쓰기를 하는 것이 가독성에 좋다.



### Headings

: 글자 크기설정, :`<h1> ~ <h6>`까지 6단계가 있다.



### Divs

: division(구분), section을 나눈 일명 박스, 비슷한 기능들을 Group시킬 때 유용.



### Attributes

: tag(태그)를 확장할 때사용.

: 종류(name, value)

- id : 해당 내용을 특정구분할 때.



### Displaying Text

: HTML에 글자를 입력할 때 `<p></p>` 또는 `<span>`를 사용한다.

- `<p>` : 일반적인 평문
- `<span>`: 짧은 단어 또는 다른 HTML, 문장내 특정부분을 지정하고자 할 때 유용



### Styling Text

- `<em>` :이탈릭 채,  italic emphasis
- `<strong>` : 문자 굵게, bold



### Line Breaks

- `<br>`: 줄 바꿈, close tag가 없다. 문장 앞 또는 뒤에 붙인다.



### Unordered Lists

: 내용을 정리할 때 유용

- `<ul></ul>` : unordered lists, 정리되지 않은 리스트, 점으로 정리
- `<li></li>` : 리스트 정리할 것 앞에 붙이는 태그



### Ordered Lists

- `<ol></ol>` : unordered lists과 비슷, 정리된 리스트, 숫자로 정리
- `<li></li>` : 리스트 정리할 것 앞에 붙이는 태그



### Images

- `<img>` : 웹상의 이미지를 불러올 수 있다.
- `<img src = "url" width = "" height "">` : 소스, 가로, 세로



### Image Alts

- 이미지를 웹상에서 불러오는 데 실패했을 경우, 이미지에 대한 간략한 설명
- 이미지 읽기 가능
- SEO(Search Engine Optimization), 검색어에 설정한 text로 검색 가능
- `<img src = "url" alt = "something">` : 소스, 가로, 세로



### Videos

- `<video src = "#" width = "#" height ="" controls></video>` 
- controls는 기본적인 재생, 일시정지, 건너뛰기 기능











