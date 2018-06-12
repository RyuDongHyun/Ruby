# 웹상의 정보 가져오는 방법

### 1. 노가다  -> 손수 직접 옮기기

- 시간 많이 걸림, 큰 데이터 옮기는 데 부적합



### 2. API 방식 (가장 선호) 

- 정보제공자가 기꺼이 정보를 내놓는 경우
- 가져가기 쉽게 만들어 놓음(프로그래밍을 통해서)
- 프로그램으로 조작할 수 있는 방식



### 3. 스크랩/ 크롤링 

- 정보제공자가 기꺼이 정보를 내놓지 않은 경우
- 하지만 웹상에는 있는 경우
- 긁어, 뺏어 올 수 있음

=> 웹에 올라온 정보는 모두 자동화하여 가져올 수 있다.



### .json

: HASH와 같다.

: key => value(이름표 => 값)

: =>을 : 으로 바꾼 것.

: 구글 확장프로그램으로 viewer 다운로드 가능



### httparty

: 웹페이지에 요청, `HTTParty.get(url)` 



### .json , hash로 바꾸기

- : 을 =>로 바꾸면 됨





# ☆프로그래밍 하는 방법(개발방법론)

### 1. 일단 돌아가게 만든다.(엄청 무식한 방법이라도 상관x)

### 2. 테스트를 한다.

### 3. 리팩토링을 한다.(코드의 악취제거)

1. 악취1 : 반복되는 코드(DRY_Do not Repeat Yourself)
2. 악취2 : 보기 힘든 코드
3. 악취3 : 비효율적인 코드

### 참고 - TDD(Test Driven Development) : 2 -> 1-> 3



### Partial render sinatra




