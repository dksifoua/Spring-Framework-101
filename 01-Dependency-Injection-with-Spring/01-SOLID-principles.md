# SOLID principles of OOP

- **S**ingle Responsability Principle: *Just because you can doesn't mean you should.*
  - Every class should have a single responsibility.
  - There should never been more than one reason for a class to change.
  - Classes should be small. No more than a full screen of code. Avoid *God* classes (class that can do everything). Split big classes into smaller classes.
- **O**pen Closed Principle: *Open Chest Surgery is not needed when putting on a coat.*
  - Classes should be open for extension but closed for modification.
  - We should be able to extend a class behavior without modifying it.
  - Use private variables with getters and setters; ONLY when needed.
  - Use abstract base classes.
- **L**iskov Substitution Principle: *If it looks like a duck, quacks like a duck but needs batteries, you probably have the wrong abstraction.*
  - Objects in a programm would be replaceable with instances of their subtypes WITHOUT altering the correctness of the program.
  - Violations will often fail the *is a* test like a square is a rectangle however, a rectangle is not a square.
- **I**nterface Segragation Principle: *You want me to plug this in, where?*
  - Make fine grained interfaces that are client specific. Many clients specific interfaces are better than one general purpose interface.
  - Keep components focused and minimize dependencies between them.
  - Notice relationship to the single responsability principle ie avoid *god* interfaces.
- **D**ependency Inversion Principle: *Would you solder a lamp directly to the electrical wiring in a wall*
  - Abstractions should not depend upon details and details should depend upon abstractions.
  - Important that higher level and lower level objects depend on the same abstract interaction.
  - This is not the same as Dependency Injection, which is how objects obtain dependent objects.

In summary, the SOLID principles of OOP will lead us to better quality code. The code will be more testable and easier to maintain. A key theme is to avoiding tight coupling in the code and be pragmatic when following SOLID principles (for eg, with Spring Framework, every request path does not need its own controller class).
