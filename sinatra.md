# 자주 사용하는 것들

### 한글인식 가능하게 하기

```html
<head>
     <title>투표앱</title>
     <meta charset = "utf-8"> #한글인식을 위한 코드
</head>
```



### 페이지 요청

1. Route 페이지 요청

   ```ruby
   get '/' do
       erb :index
   end 
   #의미 : route페이지가 나오면 index.erb파일을 실행해라.
   ```

   : / 로 route 페이지를 요청한다.

   : `erb` 는 Ruby코드를 입력가능한 HTML파일이다.

   : sinatra에선 views폴더 안에 .erb파일들을 저장해야 한다.



### 사용자로부터 입력받기

: HTML파일에서  사용자로부터 입력을 받기위해선 `<form> ~ </form>`태그를 이용한다.

예시)

```html
<form action = "/register">
      <h3>이름</h3>
      <input type = "text" name = "input">
      <input type = "submit">
</form>
```

- `<form action = "/()">`

  : submit 버튼을 눌렀을 때 이동하는 페이지를 설정한다.

- `<input type="()" name="()" value="()">`

  - type 종류 

    1. text : 글자 입력

    2. submit : 제출버튼

    3. radio : 선택

       ```html
       <form>
         <input type="radio" name="gender" value="male" checked> Male<br>
         <input type="radio" name="gender" value="female"> Female<br>
         <input type="radio" name="gender" value="other"> Other
       </form>
       ```

       : 변수이름은 같게설정, 변수 값만 다르게 설정.

  - name

    : 변수 이름지정

  - value

    : 변수 값 지정, 없다면 입력된 값이 넘어감.



### params[:name]

: 사용자로부터 입력받은 값을 저장하여 Hash처럼 기능하는 명령어

예시)

```html
<form action = "/register">
      <h3>이름</h3>
      <input type = "text" name = "input">
      <input type = "submit">
</form>
#입력받은 값을 /register 페이지로 보내라.
```

```ruby
get '/register' do
    @input = params[:input]
end

```

- `@input` : 앞에 @를 붙여줌으로써 전역변수로써 기능. 
- `params[:input]` : 입력받을 때 지정했던 변수이름을 넣으면 String형태로 값이 들어옴.





### .erb파일에 Ruby 코드넣기

```html
    <body>
        <% @file.each_line do |line| %>
        <p><%= line %></p>
        <% end %>
    </body>
```

- `<%= (ruby_code) %>`: `=` 은 출력을 하고자 할 때 쓰고 출력하지 않는다면 쓰지않는다.



### "(   )" 따옴표 안에 변수값 나오게 하기

```ruby
 f.write("#{@me}랑 #{@you}가 될 확률은 99%\n")
```

- #{(변수이름)} : " " 안에서 변수에 들어있는 값을 나오게 하기위한 형식



### Layout 파일

:매번 .erb파일에 똑같이 들어가는 것들을 따로 만들어 코드의 악취를 제거한다.

1. `layout.erb` 파일 생성

2.  

   ```html
   <!DOCTYPE html>
   <html>
       <head>
           <title>게시판</title>
           <meta charset="utf-8">
       </head
       <body>
           <%= yield %>
       </body>
   </html>
   ```

   : 반복되는 코드를 넣는다.

   : .erb 파일들이 들어갈 곳에 `<%= yield %>`를 삽입해 놓는다.



