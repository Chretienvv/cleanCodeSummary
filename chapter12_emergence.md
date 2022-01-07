# Clean code chapter 12

## Tips & Learnings
- When is a design simple?
    - Runs all the tests
    - COntains no duplication
    - Expresses the intent of the programmer
    - Minimizes the number of classes and methods.

- Rule 1: Run all the tests
    - Systems that arent testable arent verifiable. 
    - "We need to have tests and run them continuously impacts our systems adherence to the primary OO goals of low coupling and high cohesion." Writing tests leads to better design.

- Rule 2- 4: Refactoring.
    - In this all the three other rules are applied.
    - COntains no duplication
        - Duplication represents: Additional work, additional risk, additional unnecessary complexity.
        - The template method: The template method is a method in a superclass, usually an abstract superclass, and defines the skeleton of an operation in terms of a number of high-level steps. These steps are themselves implemented by additional helper methods in the same class as the template method.
    - Expresses the intent of the programmer
        - The clearer the author can make the code, the less time others will have to spend understanding it. This will reduce defects and shrink the costs of maintenance.
        - Keep functions small
        - Choosing good names
        - Choosing the standard nomenclature. Design patterns. 
    - Minimizes the number of classes and methods.
      - Be carefull for splitting classes and functions just to make them smaller. This is not the goal.


## Own Opinion
These rules are very nice, because it can be acted on. I agree with all of these rules and think that the "pride" part is interesting. When something works it should also be clear to other developers.