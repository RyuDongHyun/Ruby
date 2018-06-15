# Prime 구하기

1. Prime 클래스를 몰라서 다음과 같이 일일이 짠 경우

```ruby
def solution(n)
    answer = 0
    count = 0    
    arr = (1..n).to_a
    arr.each do |x|
        arr2 = (1..x).to_a
        arr2.each do |y|
            if x%y==0               
                count =count + 1  
            end
        end
        if count == 2
            answer += 1 
        end
        count = 0
    end
    return answer
end
    
puts solution(10) #결과 => 4
```

2. `prime` 클래스를 가져와서 쓰면!!

```ruby
require 'prime'

def solution(n)
  Prime.each(n).count
end
```

.... 4줄만에 끝남.



