# Logic in Ruby

The big difference between Ruby and JavaScript here is that the ONLY falsy values in Ruby are `nil` and `false`.

`""` or `0` are NOT falsy values.

`elsif` is used in Ruby - Note the spelling

`#eql` checks both the value type and the value it holds, so:

```ruby
5.eql?(5.0) #=> false
5.eql?(5) #=> true
```

### Spaceship Operator

A special Ruby operator `<=>` that returns 1 of 3 values:

- -1 if the value on the left is less than the value on the right
- 0 if the values are equal
- 1 if the value on the left is greater than the value on the right

This is most commonly used in sorting functions.

### Case Statements

used instead of a long, messy if...else statement.
