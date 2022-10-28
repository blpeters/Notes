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
