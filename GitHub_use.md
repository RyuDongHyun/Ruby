# GitHub 사용

1. Git_base 이용
2. `cd`로 폴더로 이동 (업로드하고자 하는 파일들)



### Git

: 파일들을 버전관리해주는 프로그램

- 버전관리? 

  => 해당 파일들이 언제 어떻게 변했는 지를 기록해서 관리한다는 뜻.



### Work Flow_작업순서도

![workflow](https://user-images.githubusercontent.com/40014912/41513855-07c20664-72dd-11e8-8b76-b78f5a7a9245.png)

1. 현재 작업하고 있는 폴더(Working Directory) 안에 있는 내용들을 버전관리하겠다.

   => 현재 폴더의 위치로 이동하여 `git init` 명령을 한다.

2. 작업 후 변경사항들을 Staging Area에 저장한다.(Staging : Repository에 저장하기 전 대기장소)

   => `git add` 명령을 한다. 

   - `git status` : 현재 폴더에 상태를 알 수 있다.

3. 변경사항 Repository에 저장, 버전관리!! 메세지를 기록할 수 있다.

   => `git commit -m "~"` 

   - `git log`: 현재까지 변경사항들을 볼 수 있다.

   - `git config --global user.email "you@example.com"` : 이메일 등록

   - `git config --global user.name "you"` : 이름 등록

     

### Git_hub 이용

: global repository(원격저장소)와 버전관리를 연동
1. global repository(원격저장소) 주소 등록

   - `git remote add origin http://github.com/RyuDongHyun/Ruby.git`

     => git아~ 원격저장소 등록해라 이름은 origin으로 주소는 `http://github.com/Ryu~~`

   ![git-address](https://user-images.githubusercontent.com/40014912/41513867-227461aa-72dd-11e8-8748-a0c213d08f71.png)

   - `git remote` :  등록된 원격저장소의 이름을 알 수 있다.
   - `git remote -v` : 등록된 원격저장소의 주소를 알 수 있다.


2. 업로드
   - `git push` : `git commit`으로 local repository에 저장된 파일들을 github에 업로드



### 협업 또는 여러대의 컴퓨터에서 사용

- `git fetch` : 원격 저장소에 저장된 변경사항들을 다운로드
- `git merge` : 다운로드 받은 변경사항들을 원래 파일에 합치기
- `git pull` : fetch + merge기능, 변경사항들 다운로드 합치기



