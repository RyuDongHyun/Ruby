# HTML DOCUMENT STANDARDS

:HTML 문서 표준



### Preparing for HTML

: `<!DOCTYPE html>` 로 시작,  HTML문서 가장 첫줄에 써야 함.(현재는 HTML5를 쓰고있음)

:  파일 형식은 `.html` 

: 문서type과 HTML버전을 알려줌



### The `<html>` tag

: HTML 문서를 만들기 위해선 `<!DOCTYPE html>` 다음으로 반드시 `<html></html>`을 써야 함.

: `<html></html>` 사이에 있는 모든 코드는 HTML라고 간주.



### The Head

: 페이지 정보를 알려주는 기능

: `<head></head>` 태그 사용. `<body>`태그 위에 써야함.



### Page Titles

: 페이지의 이름을 알려줌

: `<title></title>` 태그 사용.



### Linking to Other Web_pages

: HTML의 강력한 기능! 웹페이지 링크

:`<a></a>` 태그 사용, 여기 `<a>` 태그 안에 `href="url"` 삽입

ex) `<a href = "url">This is a Link To Naver</a>`



### Opening Links in a New Window

:`target`  삽입, 링크가 어떻게 열릴 지 설정

: `<a href = "url" target ="_blank">This is a Link To Naver</a>`, 링크_새 창에서 열기



### Linking to Relative Page

: 내부 사이트 링크, ex) Contact, About, Home

: 먼저 각 파일들이 어디에 저장되어있는지 지정

(개발자들은 통상 HTML파일을 모든 파일이 저장된 root directory 즉 주 폴더에 저장함)

: `html` 파일은 보통 같은 폴더에 저장함.

ex) `<a href = "./contact.html">Contact</a>`

:`./` 은 현재 폴더에서 찾는다는 의미.



### Linking At Will







