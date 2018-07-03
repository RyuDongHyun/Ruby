# DB association

: 데이터베이스 관계



### Association type

1. 관계없음

2. 1 : 1

3. 1 : N 

   => 1 많은 N을 가지고 있다.

   => N은 반드시 1에 속한다.

   #### - Primary key(1쪽에 있는)

   : 어떤 레코드를 찾을 때 중요한 단서, 고유값

   #### - Foreign key(N쪽에 있는)

   :  고유값을 지정하기 위한 값(ex 교복 명찰)

4. M : N

   => 강의는 많은 학생을 가지고 있다.

   => 학생은 반드시 여러 강의에 속한다.



### How?

: models 폴더 안에 있는 .rb파일을 서로 연관시켜준다.

ex) Post(게시글), User(사용자), Reply(댓글) model이 있다고 할 때 

1. model파일들의 관계설정

```ruby
class Post < ActiveRecord::Base
    belongs_to :user   #Post는 한 User에 속한다.
    has_many :replies  #Post는 많은 Reply를 가지고 있다.
end
#영어문법에서의 단수, 복수를 주의
#Model파일들의 관계를 보고 어떤 것이 단수고 어떤 것이 복수인지 확인!
```

2. 소속의 Primary key(고유값)을 받기 위한 Foreign key(지정값) 설정(ex 교복명찰 달기)

```ruby
class CreatePosts < ActiveRecord::Migration
  def change
    create_table :posts do |t|
      t.string :title
      t.string :content
      
      #Post는 User의 속하기 때문에 Primary key값을 받기위한 Foreign key 설정 
      t.integer :user_id 
      t.timestamps null: false
    end
  end
end

```

3. Foreign key(지정값)에 소속 Primary key(고유값)을 대입

```ruby
  def create
      Post.create(
      title: params[:title],
      content: params[:content],
      user_id: session[:id] #Foreign key(지정값)에 소속 Primary key(고유값)을 대입
      )
      redirect_to '/'
  end
```

4. 참조해서 사용하기

```html
<% @post.replies.reverse.each do |p|%> #Reply 참조, .replies
<p><%= p.user.name%> : <%= p.comment%></p> #User 참조, .user
<% end %>
```





# Rails CRUD

- `rails g controller posts index new create show edit update destroy`
- `rails g model Post title:string content:text`
- `root 'posts#index'` 
- `<input type="hidden" name="authenticity_token" value="<%= form_authenticity_token%>">`



### Restful

```ruby
  root 'posts#index'

  #Create
  get 'posts/new' 
  post 'posts' => 'posts#create'

  #Read
  get 'posts/:id' =>'posts#show'

  #Update
  get 'posts/:id/edit' => 'posts#edit'
  put 'posts/:id' => 'posts#update'

  #Delete
  delete 'posts/:id' => 'posts#destroy'

#`posts/:id` 가 똑같은 url요청이지만 앞부분의 get,put,delete verb의 차이로 다르게 요청이 보내집니다.

```



### form에서 post요청 보내기

```html
<form action="/posts/create" method="post">
    제목 : <input type="text" name="title" placeholder="제목을 입력하시오."><br>
    내용 : <input type="text" name="content" placeholder="내용을 입력하시오."><br>
    <input type="submit" value="저장">
    <input type="hidden" name="authenticity_token" value="<%= form_authenticity_token%>">
</form>
```



### form에서 put요청 보내기

```html
<!--form은 get과 post만 지원한다.-->
<form action="/posts/<%= @post.id%>" method="post">
    <input type="hidden" name="_method" value="put">
    제목 : <input type="text" name="title" value="<%= @post.title%>"><br>
    내용 : <input type="text" name="content" value="<%= @post.content%>"><br>
    <input type="submit" value="수정">
    <input type="hidden" name="authenticity_token" value="<%= form_authenticity_token%>">
</form>
```



### a태그에 delete 방식 추가하기

```html
<a href='/posts/<%= @post.id%>'  data-method="delete" >삭제하기</a>
```



