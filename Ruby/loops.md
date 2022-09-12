# Loops in Ruby

## the `loop` loop

An infinite loop unles you request if to stop with `break`

This type isn't used much - there's probably a better option.

## While loop

declare the break condition right up front

## Until loop

This is just the opposite of the while loop, so depending on what your break condition is, choose the one that makes the code more readable.

## Ranges

Good for when we know how many times we need a loop to run.

```ruby
(1..5)    #inclusive range: 1,2,3,4,5
(1...5)   #exclusive range: 1,2,3,4
```

## For loop

```ruby
for i in 0..5
  puts "#{i} zombies incoming!"
end
```

## Times loop

```ruby
5.times do
  puts "Hey"
end

5.times do |number|
  puts "Hey number #{number}"
end
```

## upto and downto loops

methods #upto and #downto

```ruby
5.upto(10) {|num| print "#{num} "}

10.downto(5) {|num| print "#{num} "}
```
