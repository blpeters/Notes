# Pattern Matching

### Ways to pattern match

- Any Ruby object witch is matched using ===. The Object Pattern.
- A variable capture/Variable Pattern
- An As Pattern
- An Alternative Pattern
- A Guard Condition
- An Array Pattern
- A Hash Pattern
  \*\* Experimental conditions:
  - Rightward Assignment
  - A Find Pattern

Patterns can be matched using any combination of the above.

### Return Values

TWO POSSIBLE VALUES:

- `true`: returned when there's a match, even when the match is the else clause in a a statement
- `NoMatchingPatternError`: whenever no match can be found.

### Procs vs. Lambdas

Lambdas are much closer to a normal method than procs, but they are simply a special type of proc object - Hence the #lambda? method in the proc class.

Procs do not care about the number of arguments and will run regardless of a proper number of arguments/parameters provided. Procs will return in the context of the current scope, which means they will return nothing if already in the highest level of code (outside of any method scope, etc.) because there's no where else to go. Lambdas return like normal methods.

#### Closure
Procs will also capture the current execution scope with it (CLOSURE). This means a proc will carry the values of local variables and methods from the contect where the variables/methods were defined. The actual variables are not carried, only the reference to them, so the variables can still be mutated outside the scope of the proc.

Good quote on closure: when a function can be stored as a variable. (first-class function)

#### Binding

Create a Binding object via a binding method to create an ANCHOR to this point in the code. You can use this object anywhere later in code to reference back to the binding location and use variables defined back at that point, even if those variables are not available in other scopes if tried to reference directly.
