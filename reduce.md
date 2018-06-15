# reduce

- `reduce(initial, sym)`
- `reduce(sym)`
- `reduce(initial){|memo,obj|block}`
- `reduce{|memo, obj|block}`

```ruby
# Sum some numbers
(5..10).reduce(:+)                             #=> 45

# Same using a block and inject
(5..10).inject { |sum, n| sum + n }            #=> 45, inject: 특성을 더하다

# Multiply some numbers
(5..10).reduce(1, :*)                          #=> 151200

# Same using a block
(5..10).inject(1) { |product, n| product * n } #=> 151200

# find the longest word
longest = %w{ cat sheep bear }.inject do |memo, word|
   memo.length > word.length ? memo : word
end
longest                                       
```

# 





