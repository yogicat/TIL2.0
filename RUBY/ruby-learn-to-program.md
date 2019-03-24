### ch 4.



`puts` - put string

`gets` - get string (only retrieve strings) from input

`chomp` - similart to `gets` but it removes enter



### ch 5.

**Methods**

- like verbs

- puts, gets, chomp, to_i, to_f, to_s, +, -, *, /, ...
- every method needs an object



### ch 7.

```ruby
3.times do
	puts 'oh'
end

food = ['pizza', 'burrito', 'salad']
food.each do |menu|
	puts 'my favorite food is ' + menu
end
```





### ch 8.



```ruby
def sayHi num
	puts 'Hi!' * num
end

sayHi 3
# => Hi! Hi! Hi!
```

