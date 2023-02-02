# Object Oriented Programming (OOP)

A programming philosophy that arose because of the increasing complexity of code bases and software. The complexity made it difficult to maintain, and small changes would have large ripple effects throughout the code.

### Encapsulation

Hiding pieces of functionality or code and making it unavailable to the rest of the code base. Helps prevent data from being manipulated or changed unintentionally.

### Polymorphism

Ability for different types of data to share a common interface, and allows flexibility in using pre-written blocks of code as building blocks for new purposes with some of the same functionality.

### Inheritance

Where a class inherits the behaviors of another class (superclass). Helps programmers to set up basic classes with the minimum functionality common to subclasses. Allow the subclasses to inherit this functionality and then build more detailed functionality off the superclass.

### Mixin

The inclusion of a module in with a class using `include` is called a mixin. This allows the behaviors of the module to be available to the class and its objects

## Dependency Injection

dependency injection is a coding practice that allows you to ove a dependency from the guts of a class to the arguments of a method that needs it - often in the initialization

This is the D in SOLID - Dependency Inversion Principle

We need to avoid situations where a class has a strict dependency on the internal workings of another class. USE DEPENDENCY INJECTION - take whatever code is directly referencing another new object and throw it up into the arguments of the current method and name it. That way, you can easily mock that argument in the case of unit testing. Also, if the API of the other class changes, in the future, we simply adjust the way the dependency is referenced in the arguments, but the method remains unchanged!!
