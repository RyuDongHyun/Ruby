#  Ruby Basic

## 조건문

1. `if` / `elsif` / `else`  : 조건이 `true` 일 때 실행

2. `unless` : if not, 만약 그렇지 않으면, 조건이  `false` 일 때 실행

   

## 반복문

1. `while` : 조건이 `true` 면 실행, `false` 면 중단.

2. `until` : 해당 조건 까지 실행, `while` 과 비슷.

3. `for` : 반복 횟수를 지정

   (ex: `for num in 1...10 do ~ end `), `...`는 `<` `..` 는 `<=` 과 같다.

4. `loop` : 특정 조건 시 `break` 를 걸고 나옴

   (ex : `loop do ~ break if (조건) end`)

5. `.each` : 배열 반복문, 배열 안에 있는 값을 반복적으로 사용할 때 사용

   (ex : `array.each do |anything| do ~ end` )

   => 배열의 처음 값 부터 `anything` 이라는 변수에 담겨 순서대로 실행됨.

   

6. `(횟수).times do ~ end`  : 특정 횟수 만큼 반복 시키고 싶을 때

7. `next if` : 반복문 속에서 건너뛰고 싶을 때 사용.

   

## 연산자

- 대입 연산자 : `=` 

  => 오른쪽 값을 왼쪽에 넣어줌.

- 산술 연산자 : `+`, `-` , `*` , `**` , `/` ,`%`

  => 더하기, 빼기, 곱하기, 지수곱, 나누기, 나머지

- 복합 대입 연산자 : `+=` , `-=`  등등

  => 더해서 대입, 빼서 대입 등등

- 관계 연산자 또는 비교 연산자 : `>`, `<` ,`<=` , `>=` , `!=` 

  => 크다, 작다, 작거나같다, 크거나같다, 같지않다

  => 결과값은 Boolean값(`true` or `false`)으로 return.

- 논리 연산자 : `&&` ,`||` ,`!` 

  => `&&`(AND)  : 두 조건 모두 `true` 일 때 `true`, 나머지 `false`

  => `||`(OR) : 두 조건 모두 `false` 일 때 `false` , 나머지 `true`

  => `!`  (NOT) :  `true` => `false` 또는 `false`=> `true`



## Multiple Values(배열)

1. 배열 : `변수이름 = []` , 대괄호 사용

   - 숫자, 문자, 숫자+문자 : 문자값을 넣을 시 '' 또는 "" 사용

2. 이중 배열 : 배열 속의 배열

   

3. 해쉬 : `변수이름 = {}`, 중괄호 사용, 배열의 각 위치에 이름표를 붙인 것과 같음 

   (만드는 방법)

   - `my_hash = {"name" => "Eric", "age" => 26}`

   - `my_hash = Hash.new` `my_hash["name"] = "Eric"`

     

   (`.each` 반복문 사용)

   - `my_hash.each do |x, y| ~ end`
   - 해쉬는 순서가 없다. 뒤죽박죽. 따라서 `.sort` 기능이 없다.



** ''

## Method example

1. `(string).include? "s"`   : (string)에 s라는 문자가 있는 지 체크해주는 기능

   ​					      : 있으면 `true`  없으면  `false`  return.

   (`?` : Ruby에서 `?`로 끝나는 메소드는 `true` 또는 `false` 값을 출력함.)

2. `.gsub!(/s/, "th")` : global substitution

   => 모든 s값을 th로 바꿔라.(`.gsub` 뒤에`!`가 붙었으므로 변수에 들어있는 값을 바꿈)

3. `.split()` : 입력된 값을 ()안에 있는 것으로 나누어 배열로 저장

4. .to_i : 정수로 변환

5. .to_s : 글자로 변환











