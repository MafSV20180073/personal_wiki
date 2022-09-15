# Refactoring code and optimization

***
**Aspects to pay attention when doing some code refactoring (tips inspired by SOLID principles):**

- Make your classes do one thing well;
- Avoid modifying existing classes (whenever possible, add new classes instead);
- Use only what’s relevant to your class;
- Decouple your classes (but careful with the explosion of new classes with every refactor you make).

***

When optimizing code or an application, it’s easier when you have a clear performance target.

Other tips:

- Replace loops with higher-order functions;
- Replace conditionals with data structures and polymorphism;
- Replace literal variable names with purposeful variable names;
- Forget global scope exists.
