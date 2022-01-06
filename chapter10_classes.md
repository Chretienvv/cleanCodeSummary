# Clean code chapter 10 classes

## Tips & Learnings
- Classes organization
    - Stepdown rule: 
        - Start with variables -> public -> private -> public functions followed by the associated private utilities
    - Encapsulation
        - Keep variables and utility functions private. 
        - Loosing encapsulation is our last resort
    - Classes should be small
        - Small in responsibilities
        - Responsibility: reasons to change
    - The name of the class name should describe its responsibilies
    - The SRP Single responsibility principle
-  Cohesion
    - Variables and functions in the class need to be used by eachother inside the class
- Organizing for change
- Isolating from change
    - Concrete classes: A concrete class is a class that has an implementation for all of its methods. They cannot have any unimplemented methods. It can also extend an abstract class or implement an interface as long as it implements all their methods. It is a complete class and can be instantiated.
    - Abstract classes: An abstract class is a class that is declared abstract—it may or may not include abstract methods. Abstract classes cannot be instantiated, but they can be subclassed.

## Own Opinion
Usually I make my classes around concepts and responsibilities. But know I know that the real key is many small classes which are small in responsibility. I think this is very good for readability. I would rather dive into 500 small and predictable classes than 5 extremely big classes which can do virtually anything.
