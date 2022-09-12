# Arrays

[Helpful Guide](https://www.rubyguides.com/2015/05/ruby-arrays/)

arrays contain elements, which can be anything

an array literal is the syntax used to create instances of an array object. Use square brackets `[]`. Another way is to used `Array.new`

Ruby has special `#first` and `#last` array methods, which return the corresponding number of items from either the beginning or end of an array - can be more than 1 item!

## Array methods

use the `#push` method or the shovel operator `<<` (preferred)

The `#pop` method will remove the last element from an array and also return it.

`#shift` and `#unshift` will add/remove elements at the beginning of the array. `#shift` is like `#pop` but for the beginning, not the end.

You can add and subtract arrays too!

Arrays within arrays are called _multi-dimensional arrays_

TIP: for string-only arrays, use the %w prefix like below to declare an array and avoid repeating quotation marks:

```ruby
peters = %w(camper karen brett)
```

Take a random element from your array with #sample
