# Clean code chapter 3 Functions

## Tips & Learnings
- Functions need to be small 
    - Approximately 20 lins 
    - lines need to be at max 150 characters long.
- indenting should not be greater than two
- Function do one thing
    - One level of abstraction per function
- The stepdown rule
    - Let each function introduce the next function when reading fromt top to bottom.
- Switch statements need to be avoided when possible. 
    - If you use them make sure to it is buried in a low level class and is never repeated. (polymorphism)
        - The polymorphism is a core concept of an object-oriented paradigm that provides a way to perform a single action in different forms. It provides an ability to call the same method on different JavaScript objects.
- Use descriptive names
    - Be consisten in the nouns, verbs and phrases you use.
- Function arguments
    - 0 is ideal, 1 and 2 are okay three should be avoided and more than three should not be used. 
    - Arguments make it harder to test the code.
- Flag arguments
    - Passing a boolean into a function is terrible practice. 
- Objects as arguments is not cheating it is likely they are part of an concept, so the object is justified.
- Have no side effects
    - Check password should not initialize another session.
- Command Query Separation
    - A function should do something or answer something but not both.
    - Prefer exceptions to returning error codes
        - With try catch you have two flows instead of nesting and checking for error codes.
- Extract Try/catch blocks
    - It can be done for whole functions and then catch the error if the function does not complete. Try catch blocks confuse the structure of code by mixing error and normal processing.
    - FUnctions should do one thing and error handling is one thing.
- DRY dont repeat yourself
    - Eliminate duplication.

## Own Opinion
It is interesting to see the examples and the level of abstraction for functions. I think "intelligent" functions that start different functions like "startBingo" are right around the corner. How to split those will be interesting. I will try this out. 