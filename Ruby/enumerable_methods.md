# Enumerable Methods

## Basic Enumerable Methods

Enumerables are built-in methods in Ruby that are included for both arrays and hashes. These were designed to make looping and iterating and similar patterns much easier.

**Check out the Enumerable module in the Ruby docs for a full picture of what's available**

### The each Method

Possibly the most common enumerable method. However, think about whether it is the best or most efficent tool for the job you're trying to do. For example, you could do the same thing as the #select method above, however it would take more lines of code and probably some type of if statement.

for multi-line blocks of code, it's best practive to change up the syntax to the following do...end format:

```Ruby
my_array = [1,2]

my_array.each do |num|
  num *=2
  puts "The new number is #{num}."
end
```

When using each for hashes, you have the ability to call the key and value individually or the key-value pair together like so:

```ruby
my_hash.each { |key, value| puts "#{key} is #{value}" } #this actually calls them individually so you can work with them independently.

my_hash.each { |pair| puts "the pair is #{pair}" } #this (default) calls the key-value pair together in an array"
```

**RETURN VALUES FROM #each** : Keep in mind that no matter what you put in the block of code after each, the each method will still return the original array or hash.

### each_with_index

provides the element from each array index, but also the index number itself. Returns original array still.

### select (also called filter)

`friends.select { |friend| friends != 'Brian'} #Return an array with every friend that isn't Brian`

The |friend| between the "pipes" if called a **block variable**. In other words, the element from the array that the block of code is currently iterating over.

#reject: Reverse of select, return an array excluding the criteria of the {}

### map (also called #collect)

The #map method will actually procuded a new returned array rather than returning the original! Map takes the original array, sends it through the map machine (performing whatever block of code you want) and spits out a new, altered array. KEEP IN MIND THIS STILL DOESN'T CHANGE THE ORIGINAL ARRAY UNLESS YOU USE #map!

### reduce (also called inject)

Possibly the most difficult of the three conceptually. Take an array or hash down to a single object => gather up each item, doing something with them as you go along.

Classic example: sum of all numbers in an array.

```ruby
my_numbers = [5, 6, 7, 8]

my_numbers.reduce { |sum, number| sum + number}
# => 26
```

`sum` in the above example is the **accumulator**. The results of each iteration are stored in this accumulator. So the value of the accumulator after the last element is run becomes the return value. You can provide an initial value for an accumulator as well like the following variation on the previous example:

```ruby
my_numbers = [5, 6, 7, 8]

my_numbers.reduce(1000) { |sum, number| sum + number}
# => 1026
```
