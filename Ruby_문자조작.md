# Ruby 문자조작

### 배열 값 정렬

- `.sort`  or `.sort{|x, y| y<=>x}`: 내림차순 정렬

- `.sort!` or  `.sort!{|x, y| y<=>x}` : 내림차순 정렬, 기존 배열 안에 순서를 바꿈.

- `.sort_by` : 복수의 정렬을 할 수 있다.

  ```ruby
  [2, 1, 3].sort_by{ |i| i }
  #결과 => [1,2,3]
  [2, 1, 3].sort_by{ |i| -i }
  #결과 => [3, 2, 1]
  ```

  - (참고) `<=>` 은 다음과 같이 작동한다.

  ```ruby
  1 <=> 2 #=> -1  
  2 <=> 1 #=> 1  
  1 <=> 1 #=> 0  
  ```

  - 예) 다음과 같이 표가 있다고 하면

  | id   | date | priority |
  | ---- | ---- | -------- |
  | 1    | 5/8  | 4        |
  | 2    | 5/6  | 2        |
  | 3    | 5/7  | 3        |
  | 4    | 5/6  | 1        |

  - `work.sort_by{|t| t.date}` or `work.sort_by(&:date)`

  => 그러면 date가 내림차순으로 정렬됨

  | id   | date | priority |
  | ---- | ---- | -------- |
  | 1    | 5/6  | 2        |
  | 2    | 5/6  | 1        |
  | 3    | 5/7  | 3        |
  | 4    | 5/8  | 4        |

  - `work.sort_by{|t| [t.date, t.priority]}`

    => 이렇게 하면 date로 내림차순 후 priority로 내림차순하여 정렬됨

    | id   | date | priority |
    | ---- | ---- | -------- |
    | 1    | 5/6  | 1        |
    | 2    | 5/6  | 2        |
    | 3    | 5/7  | 3        |
    | 4    | 5/8  | 4        |



### .chars

: 문자를 배열로 변환

```ruby
str = "cbaCBA"
print str.chars
#결과=>["c","b","a","C","B","A"]
```



### .join

:배열 안의 값들을 연결하여 문자로 값을 변환

- `.join("-")` : join시 괄호안에 있는 문자로 연결되면서 합쳐짐

```ruby
arr = ["c","b","a","C","B","A"]
print arr.join
print arr.join("-")
#결과
#cbaCBA
#c-b-a-C-B-A
```



### .delete

:배열 안의 특정값을 제거

- `.delete(~)` : 괄호안에 입력된 값을 배열에서 찾아 제거함.



### .select

:배열 안의 특정값만 고름

- `.select(~)`: 괄호안에 입력된 값만 고름



### .empty?

:배열에 값이 들어있는지 없는지 판단.



### .map

: 배열 안에 있는 값을 code block 으로 변환할 수 있다.

```ruby
a = [ "1", "2", "3", "4" ]
a.map{ |x| x = x.to_i } #=> [1, 2, 3, 4]
a.map(&:to_i) #=>[1,2,3,4]
```



### .upto

:지정된 수까지 배열만들기



### Regex quick reference

| `[abc]`    | A single character of: a, b, or c            |
| ---------- | -------------------------------------------- |
| `[^abc]`   | Any single character except: a, b, or c      |
| `[a-z]`    | Any single character in the range a-z        |
| `[a-zA-Z]` | Any single character in the range a-z or A-Z |
| `^`        | Start of line                                |
| `$`        | End of line                                  |
| `\A`       | Start of string                              |
| `\z`       | End of string                                |

| `.`  | Any single character                            |
| ---- | ----------------------------------------------- |
| `\s` | Any whitespace character                        |
| `\S` | Any non-whitespace character                    |
| `\d` | Any digit                                       |
| `\D` | Any non-digit                                   |
| `\w` | Any word character (letter, number, underscore) |
| `\W` | Any non-word character                          |
| `\b` | Any word boundary                               |

| `(...)`  | Capture everything enclosed |
| -------- | --------------------------- |
| `(a|b)`  | a or b                      |
| `a?`     | Zero or one of a            |
| `a*`     | Zero or more of a           |
| `a+`     | One or more of a            |
| `a{3}`   | Exactly 3 of a              |
| `a{3,}`  | 3 or more of a              |
| `a{3,6}` | Between 3 and 6 of a        |





###  논리연산

: ruby에선 글자로 논리연산이 가능하다.

- `&&` : and
- `||` : or
- `!` : not 



### digits

:숫자를 숫자배열로 바꿔주는 명령어

```ruby
12345.digits      #=> [5, 4, 3, 2, 1]
12345.digits(7)   #=> [4, 6, 6, 0, 5]
12345.digits(100) #=> [45, 23, 1]
```

