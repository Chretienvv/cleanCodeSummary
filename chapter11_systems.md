# Clean code chapter 11 Systems
Staying clean at higher levels of abstraction.

## Tips & Learnings
- Software systems should separate the startup process, when the application objects are constructed and the dependencies are wired together, from the runtime logic that taks over after startup.
- Lazy initialization/ evaluation idiom: In computer programming, lazy initialization is the tactic of delaying the creation of an object, the calculation of a value, or some other expensive process until the first time it is needed. It is a kind of lazy evaluation that refers specifically to the instantiation of objects or other resources.
- Separation of concerns
    - Consturction logic and runtime logic
    - Seperation of main
        - Objects are created at construction time.
- Factories
    - The abstract factory pattern provides a way to encapsulate a group of individual factories that have a common theme without specifying their concrete classes.
- Modularity and separation of concerns make decentralized management and ecision making possible.
- DIP principle: The Dependency Inversion Principle (DIP) states that high level modules should not depend on low level modules; both should depend on abstractions. Abstractions should not depend on details.  Details should depend upon abstractions.


## Own Opinion
This chapter was really focused on Java. It was interesting reading it but, for now it isnt that relevant for me at a high levels since im more in the details as a developer.