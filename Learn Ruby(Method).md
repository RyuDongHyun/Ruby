# Learn Ruby

### Why Methods?

1. 코드의 오류를 찾기 쉽다.
2. 전체코드를 보다 간단하게 만들수 있다.



### Method Syntax

- 구조 

  1. header : `def`
  2. body : method 가 수행할 기능들
  3. end : `end`

- 사용

  : 정의한 함수의 이름을 쓴다.

```ruby
def print_1_to_10
  (1..10).each { |i| print i }
end

print_1_to_10
#결과
12345678910
```



### Parameters and Arguments

```ruby
def cubertino(n) #n=>parameter
  puts n ** 3
end

cubertino(8) #8=>argument
#결과
512

```

- Parameters(변수) : 함수 정의 시 괄호안에 쓴 것. 
- Arguments(인수) : 함수 사용 시 실제로 넣은 값



### Splat

:여러 개의 인수를 받을 수 있게끔 하는 argument

:앞에 `*`를 붙여 사용한다.

```ruby
def what_up(greeting, *friends)
  friends.each { |friend| puts "#{greeting}, #{friend}!" }
end

what_up("What up", "Ian", "Zoe")

#결과
What up, Iran!
What up, Zoe!
```



### Return

:값을 반환하고자 할때 사용

```ruby
def add(x, y)
  return x + y
end

output = add(1, 2)
puts output
#결과
3
```



### Sorting

:정렬하는 기능(숫자 => 작은수부터, 알파벳 => 순서대로)

```ruby
my_array = [3, 4, 8, 7, 1, 6, 5, 9, 2].sort!
puts my_array
#결과
[1, 2, 3, 4, 5, 6, 7, 8, 9]

```

### The Combined Comparison Operator

: `a <=> b` 

1. a == b 인경우 : return 0
2. a < b 인 경우 : return -1
3. a > b 인 경우 : return 1

