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

## Mocks, Doubles, Stubs, etc

useful in tests when the method being tested relies on results from outside methods or information at the boundary of our code and external "things" like HTTP requests or information from a hard drive. We can recreate these necessary snippets or functionality in testing.

### Stubs

rspec has a built-in library called rspec-mocks. Mocha is another popular library, among others.

from the rspec docs:

`allow(dbl).to receive(:foo).with(1).and_return(14)`

which basically says to allow an object (dbl) to "receive" a certain method call (:foo), with a certain argument (1), and return a certain value (14). So, this entire message send/receive is "faked" in the test itself to be able to isolate and test the subject component. In this context, maybe the `dbl` object in the actual program references something in a database, so can't be independently or easily tested on the local machine.

### Mocks

Mocks are similar to stubs, albeit different. Mocks are there to make assertions about methods being called during your tests. It doesn't replace the method being called, but rather asserts that the method actually is being called.

### Spies

Verifies that a stubbed method has been called after the fact.

## Double Objects

A double object is a fake object that can "double" as a more complicated object, while limiting the necessary scope to what is required for the test.

## When to use mocks, stubs, spies, doubles?

The answer is a complicated 'it depends'. However, if your application talks to an external API then that would be a very clear case for needing some combination of these to test. You don't want external calls in your tests - They make testing super slow and impossible to work on offline. Use a stub to fake the call to the external system.
