# Hashes

The big brother to arrays - similar to objects in javascript. A hash is to an array like a menu of entrees is to a vending machine with ordered selections.

Create a hash with the hash literal `{}` or the syntax Hash.new

most commonly, keys will be defined by hashes rather than strings. It shows up much more clearly and readable.

connect a key to a value with a hash rocket:

```ruby
# With the hash rocket:
hash_name = {key => value,
key2 => value2
}

# Or with symbols and no hash rocket:
japanese_cars = {
  honda: "Accord",
  toyota: "Corolla",
  nissan: "Altima"
}
```

Both the Ruby arrays and hases employ Ruby's Enumerable module, which means they share many of the same methods. A couple of methods unique to hashes are the #keys and #values methods which will return an array of the keys and values respectively.
