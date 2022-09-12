# Variables

When naming variables, keep the following in mind:

> `"Always code as if the person who ends up maintaing your code will be a violent psychopath who knows where you live."`

in Ruby, variables should always be:
-lowercase
-multiple words split by underscore (snake_case)
-descriptive
-undestandable months later to someone else

## Types of Variables

- Constants
- Global
- Class
- Instance
- local

### Constants

Capitalize EVERY letter in the variables name. These are for variables that never need to change.

### Global

**_Don't use_**

Start with a $ to declare :

```ruby
$var = "I'm available everywhere"
```

### Class

**_Rarely used_**

start with 2 @ signs (@@) to declare. Accessible by instances of the class and the class itself. This is when you need a certain variable for every instance of the class, but each instance does not need it's own unique variable.

### Instance

Declared with only a single @ symbol. Don't use these yet. Available through the current instance of a class only.

### Local

These are the most common to come across. Obey all scope boundaries. Lowercase, simple declaration.
