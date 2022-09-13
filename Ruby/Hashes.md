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

Knowledge Check:

**-What are the differences between hashes and arrays?**

Hashes are like menu entrees, where each entree(key) has a variety of ingredients/sides/etc. (values) - or sometimes just one value (like french fries). Arrays are more like a vending machine where each individual item is in an ordered grid or list that you can choose from.

Arrays are typically used for ordered items or when all values are the same format while hashes are used for unordered lists (now they can be ordered too, however) or where there's many different data types involved. Hashes are a more in-depth array...

**-What are keys and values in a hash?**

Keys are the label/naming for a specific piece of data, while the values are the data themselves. Keys are like a sticky note on an object.

**-How can you create a new hash?**

You can declare it just like a local variable with lowercase naming, (using the hash literal {}) OR

You can use Hash.new (using the #new method on the Hash class)

**-How can you populate a hash with data**

If you simply use the hash literal {}, you can populate the hash with as much data as you want, separated by commas
Hashes are mutable in several ways. If you simply declare a new key using bracket notation hash[key] = value, you can add that key-value pair to an existing hash.

**-How can you change existing values within a hash?**

See above

**-How ca you delete existing data from a hash?**

hash.delete(item to be deleted)

**-How can you merge two hashes together?**

original_hash.merge(second_hash)

**-Why is it preferred to use symbols as hash keys?**

This allows for very clean Ruby code where you can omit the ":" from the original definition of the hash, so the code is very readable. You still must use the :key_name format when accessing the data, however. Example: `japanese_cars[:honda]`
