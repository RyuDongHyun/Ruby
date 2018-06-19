# Database

:엑셀과 비교했을 때 DataBase = File, Table = Sheet



### .csv

:Comma Separated Values , 엑셀의 가장 간단한 버전, 콤마로 이루어지는 데이터

- `require 'csv'`
- `CSV.open("파일이름.csv", "뭘할지")`
- `<<`  은 `.push` 와 같다.
- 배열과 같다.`[["yerim", 1], ["changwon", 1], ...]`

:쓰고 읽기는 수월, 하지만 수정 삭제가 어렵다. 따라서 아래의 언어를 다룬다.



### RDMS

:Relational Database Management System

그전까지는 SQL이라는 언어를 따로 배워야 했다.

:ORM(object relations mapping)

#### Oracle DB, MySQL, MSSQL,.....

#### SQLite=>mobile.app(경량형 데이터베이스 메니지먼트 프로그램)



### Bundler

:패키지 매니지먼트(설치 할 gem들을 한 파일에 저장해 놓고 한번 에 설치!!)

- `gem install bundler` 로 설치

- Gemfile 파일 생성

  ```ruby
  source 'https://rubygems.org'
  
  gem 'sinatra'
  gem 'sinatra-contrib'
  gem 'json', '~> 1.6'
  gem 'data_mapper'
  gem 'bcrypt'
  gem 'dm-sqlite-adapter'
  ```

  자주쓰는 gem들을 기입하고 맨 위에 그것을 가져올 주소를 적는다.

- `bundle` 명령어로 Gemfile내의 gem들을 설치

  => Gemfile.lock 이라는 파일이 생성되며 설치된 gem들의 리스트를 보여준다.

- (참고_ 서버 생성시)`bundle exec ruby app.rb -o $IP -p $PORT` 



### data_mapper





















