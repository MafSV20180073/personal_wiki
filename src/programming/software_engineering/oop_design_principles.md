# Object Oriented Design Principles

***

**Top 10 OOP principles:**

1. DRY (don't repeat yourself) - avoids duplication in code.
2. Encapsulate what changes - hides implementation detail, helps in maintenance.
3. Open closed design principle - open for extension, closed for midification.
4. SRP (single responsability principle) - one class should do one thing and do it well.
5. DIP (dependency inversion principle) - don't ask, let framework give it to you.
6. Favor composition over inheritance - code reuse without cost of inflexibility;
7. LSP (Liskov substitution principle) - subtype must be substitutable for super type.
8. ISP (interface segregation principle) - avoid monolithic interface, reduce pain on client side.
9. Programming for interface - helps in maintenance, improves flexibility.
10. Delegation principle - don't do all things by yourself, delegate it.

***

### 1. DRY

Don't write duplicate code, instead use *Abstraction* to abstract common things in one place. The main benefit of this principle in maintenance.

### 2. Encapsulate what changes

Encapsulate the code you expect or suspect to be changed in the future. The main benefit of this principle is that will be easier to test and maintain proper encapsulated code.

For example, when coding in Java, one can follow the principle of making variables and methods private by default and increasing access step by step, like from private to protected and not public.

### 3. Open closed design principle

Classes, methods, or functions should be open for extension (new functionality) and closed for modification. This principle prevents someone from changing already tried and tested code. In other words, if we are adding new functionality only, then our code should be tested, and that's the goal of the Open Closed Design principle.

### 4. SRP

This principle states that there should not be more than one reason for a class to change, or a class should always handle single functionality.

Notice that when we introduce more than one functionality in one Class, it introduces *coupling* between two functionalities. This also means that when introducing changes into one feature, there is the chance of breaking the coupled functionality, which requires another round of testing to avoid any surprise on the production environment.

### 5. DIP

Don't ask for dependency; it will be provided to you by the framework.

One of the most known examples is the Spring Framework. Any class which is injected by the DI framework is easy to test with the mock object.

### 6. Favor composition over inheritance

Composition allows changing the behavior of a class at run-time by setting property during runtime, and by using Interfaces to compose a class, we use <i>polymorphism</i>, which provides flexibility to replace with better implementation at any time.

### 7. LSP

According to this principle, Subtypes must be substitutable for supertype, i.e., methods or functions which use superclass type must be able to work with the object of subclass with no problem.

This principle is also closely related to the SRP and ISP - if a class has more functionality, then the subclass might not support some of the functionality and does violate LSP. In order to follow LSP, derived classes or subclasses must enhance functionality, but not reduce them.

### 8. ISP

It states that a client should not implement an interface if it doesn't use that. This occurs mostly when one interface contains more than one functionality, and the client only needs one functionality and no other.

Another benefit of this principle is the interface has the disadvantage of implementing all methods before any class can use it, so having single functionality means less methods to implement.

### 9. Programming for Interface, not implementation

Always program for the interface and not for application - this will lead to flexible code that can work with any new implementation of the interface. In Java, it means using interface type on variables, return types of methods, or argument type of methods.

### 10. Delegation principles

Don't do all stuff by yourself, delegate it to the respective class. The key benefit of this principle is no duplication of code and it becomes pretty easy to modify the behavior.

<br>

<br>

**Main sources:**

- <https://javarevisited.blogspot.com/2018/07/10-object-oriented-design-principles.html>
