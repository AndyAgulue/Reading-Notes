# SOLID Principles [Samuel Oloruntoba](https://www.digitalocean.com/community/conceptual_articles/s-o-l-i-d-the-first-five-principles-of-object-oriented-design)

SOLID is an acronym for the first five object-oriented design principles by Robert C. Martin.

**S** Single-responsibility Principle: A class should have one and only one reason to change, meaning that a class should have only one job.

**O** Open-closed Principle: Objects or entities should be open for extension but closed for modification.

This means that a class should be extendable without modifying the class itself.

**L** Liskov Substitution Principle: This means that every subclass or derived class should be substitutable for their base or parent class.

**I** Interface Segregation Principle: A client should never be forced to implement an interface that it doesn’t use, or clients shouldn’t be forced to depend on methods they do not use.

**D** Dependency Inversion Principle: Entities must depend on abstractions, not on concretions. It states that the high-level module must not depend on the low-level module, but they should depend on abstractions. This principle allows for decoupling.