# CRUD

:Create, Read, Update, Destroy(쓰고 읽고 수정하고 지우기)

0. model.rb 파일생성(생성후 실행할 .rb파일에 require ./model 로 불러옴) => 준비단계

```ruby
# data_mapper의 시작(엑셀로 치면 파일)
DataMapper::setup(:default, "sqlite3://#{Dir.pwd}/tweet.db")

# table 생성,(엑셀로 치면 sheet)
class Tweet
    # table의 리소스 가져오기
    include DataMapper::Resource
    # table의 각 항목 설정, 각 항목으로 들어오는 값 형태 설정
    property :id , Serial
    property :name , String
    property :content , Text
    property :create_at , DateTime
end

class User
    include DataMapper::Resource
    property :id , Serial
    property :email , String
    property :password , String
    property :your_name , String
    property :created_at , DateTime
end

# data_mapper의 마무리, tweet.db파일 생성(엑셀로 치면 파일)
DataMapper.finalize

#만든 table 자동 업그레이드!
Tweet.auto_upgrade!
User.auto_upgrade!
```



1. Create(생성)

   ```ruby
   get '/create' do
       Tweet.create( #.create로 입력받은 값을 각 테이블의 항목들에 대입
           name: params[:name], #name:, Tweet table의 항 / params[:name]
           content: params[:content]
           )
      redirect '/' 
   end
   ```



2. Read(읽기)

```ruby
get '/' do
    @tweets = Tweet.all #변수에 Tweet에 담긴 모든 내용을 해쉬와 같은 형태로 대입한다.
    
    erb :index
end
    
```

```html
<table class="table">
  <thead>
    <tr>
      <th scope="col">이름</th>
      <th scope="col">트윗</th>
    </tr>
  </thead>
  <tbody>
      <!--hash와 같은 형태로 넘어온 것의 각 항을 돌며 출력-->
     <% @tweets.reverse.each do |t| %> 
    <tr>
      <th scope="row"><%= t.name%></th> <!--t의 name항목 값-->
      <td><%= t.content%></td> <!--t의 content항목 값-->
    </tr>
    <% end %>
  </tbody>
</table>
```



3. Update(수정)

- 수정버튼 생성 후 링크

```html
<a href="/replace/<%=p.id%>"></a> <!--수정항목의 id 저장-->
```

- 변수에 수정할 항목의 정보 대입

```ruby
get '/replace/:id' do
    @user=Tweet.get(params[:id]) #넘어온 아이디의 해당항목들의 정보를 담는다.
    erb :re_write
end
```

- re_write 화면에서 입력받기(/replace_password/:id 로 넘김 )

- 넘어온 값으로 수정하기

```ruby
get '/replace_password/:id' do
    user=User.get(params[:id])
    user.update(
        password: params[:password] #수정해야할 항목 입력된 값으로 변경
        )
    redirect '/admin'
end
```



4. Destroy(삭제)

- 삭제버튼 생성 후 링크

```html
<a href="/delete/<%=p.id%>"></a> <!--삭제항목의 id 저장-->
```

- 삭제하기

```ruby
get '/delete/:id' do
    user=Tweet.get(params[:id])
    user.destroy #해당 아이디 모든 항에 있는 내용 삭제
    redirect '/' 
end
```

