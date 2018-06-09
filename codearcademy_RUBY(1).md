# INTRODUCTION TO RUBY

## Overview &Sneak Peek

- High-level : 읽고 쓰기 쉽다
- Interpreted : compiler가 필요없다.
- Object-oriented : Object를 다루기 쉽다.
- Easy to use : 사람이 쓰는 언어와 유사하다.



## Data Types

1. Numbers : 숫자
2. Strings : 문자 
3. Booleans : 참 / 거짓



## Variables

: 값을 담는 상자, 변수 선언 시 `=` 을 사용.

ex) `my_num = 100` my_num이라는 변수에 100이라는 값을 대입해라!



## Math

1. Addition( 더하기) : `+`
2. Subtraction(빼기) : `-`
3. Multiplication(곱하기) : `*`
4. Division(나누기) : `/`
5. Exponentiation(지수 곱) : `**`
6. Modulo(나머지) : `%`



## 'puts' and 'print'

1. print : 화면에 값을 출력하는 명령어
2. puts : print와 같이 화면에 값을 출력하나 한 줄 띄어짐



## Everything in Ruby is an Object

- Object(객체) : 기능을 수행하는 것

  

- methods(메소드) : Object(객체)가 할 수 있는 기능들

: 'Object' + 'methods' == 주어' + '동사' 의 관계

ex) my_string.length (my_string == object, . == +, length == methods)

=> (my_string 의 길이를 가져와라), (길이 재자, my_string을)



- interpreter(번역기) : 사람이 쓴 코드를 컴퓨터가 알아듣도록 번역하는 기능을 함.

ex) 사람이 editor에 code를 씀 => interpreter가 번역 => 컴퓨터가 console창에 띄움.



## Comments

: 주석처리

1. `#` : 한 줄 주석처리
2. `=begin` ~~ `=end` : 여러 줄 주석처리



## Naming Conventions

: 이름짓기 규칙

: local variables(지역변수들)의 이름은 소문자로 

: 또는 `_` 사용, ex) `masterful_method`

: `$` , `@` 으로 시작하면 다른 기능을 수행하기 때문에 

 변수이름 지을 땐 사용하지 않는다.



## Getting Input

: `gets` 라는 명령어를 이용해서 사용자로 부터 값을 입력받는다.

: `.chomp` ,  `gets` 로 값을 입력받으면 뒤에 빈칸까지 입력을 받는데 

  이 빈칸들을 없애주는 기능을 함.

 ex) `gets.chomp` : 값을 입력받고 뒤에 빈칸을 없애라.



## Printing the Output

: `#{ }` 을 이용하여 변수 안에 들어있는 값을 출력한다.

ex) 

`monkey="curious"`

`puts "I took #{monkey} to the zoom`

==> `I took curious to the zoom`



## Method example

1. `.length` : 문자의 길이를 알려줌.

   => ex) `"I love espresso".length` ==> 15, 빈칸까지 길이에 포함.

2. `.reverse` : 문자를 거꾸러함.

   => ex) `"Ryu".reverse` ==> `"uyR"`

3. `.upcase`& `.downcase` : 대문자 & 소문자로 바꿔줌.

   ex) `"ryu".upcase` => `"RYU" ` 또는` "RYU".downcase` => `"ryu"`

1. `downcase.reverse.upcase` : 겹쳐서도 사용 가능

   => 소문자로 바꾸고 거꾸로 뒤집어서 다시 대문자로 바꿔라

1. `.capitalize` : 문자의 첫 글자를 대문자로 바꾸고 나머지는 소문자로 바꿔줌.

2. `.capitalize!` : 메소드 뒤에 붙은 `!` 은 해당 변수의 값을 바꿈

   ex) `print = "What's your name?"` 

   ​      `answer=gets.chomp` => `"ryu" `입력

   ​      `answer2 = answer.capitalize` => `answer=="ryu"` , `answer2 == "Ryu"`

   ​      `answer.capitalize!` => `answer=="Ryu"` , `answer2 == "Ryu"`