# Testing with Rspec

## Basic Usage

terms like describe, it, eq?, expect, context, etc. are all used in this Domain-Specific Language (DSL) to make it read like a "story" of what you are trying to test. We describe the class and what we expect to happen.

`describe` defines an example group on which some test(s) will run.

Only one top level `describe` block is required to have some valid test code.

You can trade out `it` for the aliases `example` or `specify`

rspec does this automatically!! - Use subject {} notation to define a subject at the start of the describe block so you don't have to repeat in every describe block.

```ruby
describe Board do
  subject { Board.new } # rspec does this behind the scenes.
  describe '#make' do
    it 'returns 8 x 8 board' do
      expect subject.make.....
```

### Rspec.describe

use `described_class.new() ` to define objects in your test, along with `RSpec.describe Board do` at the top.

### Booleans return values in Rspec

use the `.to be` and `.to_not be` notation for boolean unit tests rather than .... = false or true.

### Context

use if there is an if or an if else, etc. use context for various paths through the code.

## Matchers

`expect`

`eq` returns an RSpec matcher that simply tests if the object passed to expect is equal to the object passed to eq.

In the RSpec docs, there's many matchers pre-defined, and you can even define your own.
