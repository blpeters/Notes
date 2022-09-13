# Ruby Methods

Equivalent of functions in Javascript.

D.R.Y. - "Don't Repeat Yourself"

We use methods to package code for repeated use.

## Method naming

use snake_case convention. Don't use reserved words, don't begin with a number, etc.

Make it descriptive!

## Parameters

method_name(parameter)

Allows for more useful methods.

parameters vs. Arguments: Parameters are the placeholder variables in the TEMPLATE for the method and arguments are the actual variables that get passed to the method when it's called.

### Default Parameter

just add it to the normal parameter like so:

```ruby
def greet(name = "Brett") #name will always be Brett unless an argument is provided in the method call.
```

## Method Returns

Always keep in mind what the method is returning - This is how you know what to do with the results!

Ruby has implicit returns, which is a little unique. You can omit the `return` keyword and Ruby will use the last expression that was evaluated as the return (which may or may not be the last line of code in the method...)

## Chaining Methods

Do a buch of stuff all in 1 line: `puts phrase.reverse.join(" ").capitalize` is valid!

## Predicate Methods

methods with a question mark are predicate methods, because they are predicated on the return of a boolean result. Make sure to name your custom predicate methods with a `?` for clarity, even if Ruby doesn't require it.

## Bang Methods

Make a method destructive. Will overwrite the original value
