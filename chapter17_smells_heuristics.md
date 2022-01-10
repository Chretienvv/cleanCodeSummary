# Clean code chapter 17 Smells and Heuristics
More about refactoring is in a other book -> Refactoring by martin fowler. Chapter 17 includes all the smells, heuristics and practices. The setup of this chapter is a bit different than my previous ones. This chapter will be filled with additional information that I find online.

## Comments
- Inappropriate Information
    - Comments should be reserved for technical notes about the design and code.
    - Should not be used for: Change history, meta data etc.
- Obsolete Comment
    - Old comments, irrelevant comments. 
    - These comments can give the wrong intrepetation of how they system should work.
- Redundant Comment
    - For example describing code as i++ // increments i
- Poorly written Comment
    - Be brief, and choose your words carefully.
- Commented out code
    - Nobody dares to delete it. -> You should delete it!

## Environment
- Build requires more than one step
    - Building a project should be a single trivial operation. So not commenting out code, specifying the version, env etc.
- tests require more than one step
    - Should be able to run all unit tests with just one command. Quick, easy and obvious to do so.

## Functions
- Too many arguments
    - No arguments is best. More than three should be avoided.
- Output arguments
    - arguments should be inputs and not outputs. Have it change the object state if you want to set a state change.
- Flag arguments
    - For example boolean arguments -> then the function does more than one thing. 
- Dead function
    - Function that is never called. 

## Names
- Choose descriptive names
    - Names should be descriptive and evolve with the software.
- Choose names at the appropriate level of abstraction
    - Dont pick names that communicatie implementation. Choose names that reflect the level of abstraction of the class or function you are working in.
    - Dont make commitments on specifiying function names like ggetConnectectedPhoneNumber -> in the future it can be anything else.
- Use standard nomenclature where possible
    - Use the names of pattern like decorator pattern
    - Decorator pattern: A decorator is an object orientation design pattern that dynamically adds additional functionality to an object. This is more flexible than extending functionality through subclasses. Decorator belongs to the textured patterns.
- Unambigous Names
    - Choose names that make the working of a function or variable unambiguous.
- Use long names for long scopes
    - If the scope is very small for instance in a for loop then i = 0 is fine. rollCount = 0 would be to much for this scope. 
- Avoid encodings
    - Keep your names free of the hungarion pollution (see repo for more info)
    - no encodings like vis_blabla -> vis_ is the encoding for visual imaging system
- Names should describe side effects
    - Dont hide side effects from function names. For instance testOOS creates an oos if it isnt created. 

## Tests
- Insufficient Tests
    - A test should test everything that could break. 
    - Tests are insufficient when there is something left to be tested.
- Use a coverage tool
    - They make it easy to find gapes that are not tested yet. 
- Dont skip trivial tests
    - easy to write and provide documentation
- An ignored test is a question about an ambiguity
    - If the requirements are unclear than a test can be written with @ignore.
- Test boundary conditions
- Exhaustively test near bugs
    - If there is a bug, test it surroundings as well. 
- Patterns of failure are revealing
    - Look for patterns when there is a test failing.
- Test coverage patterns can be revealing
    - look at the code that is failing or not executing
- Tests should be fast

## General
- Multiple languages in one source file
    - The ideal for a source file is to contain one and only one languague. Minimize the languages in a src file.
- Obvious behavior is unimplemented
    - The principle of least surprise: The principle of least astonishment (POLA), aka principle of least surprise (alternatively a law or rule), applies to user interface and software design. It proposes that a component of a system should behave in a way that most users will expect it to behave. The behavior should not astonish or surprise users. The following is a formal statement of the principle: "If a necessary feature has a high astonishment factor, it may be necessary to redesign the feature."
- Incorrect behaviour at the boundaries
    - Prove that your code works even all the cases.
- Overridden safeties
    - Turing off failing tests/ warnings/ errors is as bad as pretending your credit cards are free money.
- Duplication
    - DRY: Dont repeat yourself
    - Template method: In object-oriented programming, the template method is one of the behavioral design patterns identified by Gamma et al. in the book Design Patterns. The template method is a method in a superclass, usually an abstract superclass, and defines the skeleton of an operation in terms of a number of high-level steps. These steps are themselves implemented by additional helper methods in the same class as the template method.
    - Strategy pattern: In computer programming, the strategy pattern (also known as the policy pattern) is a behavioral software design pattern that enables selecting an algorithm at runtime. Instead of implementing a single algorithm directly, code receives run-time instructions as to which in a family of algorithms to use.
- Code at the wrong level of abstraction
    - Lower level concepts should be in derivaties and the higher level concepts to be in in the base class.
- Base classes depending on their derivaties
    - create seperate base and derivative classes.
- Too much information
    - Well defined modules have very small interfaces.
    - Keep the coupling low.
    - Limit what you expose at the interface. 
    - less information is better. Hide your data and funcitonality
- Dead code
    - Code that isnt executed. -> delete it
- Vertical Separation
    - Concepts should be close to eachother.
- Inconsistency
    - for example: Variable names naming
- Clutter
    - Delete meaningless artifacts.
- Artificial coupling
    - Things that dont depend upon eachother should not be artificially coupled. Think about the scope of variables.
- Feature envy
- Selector arguments
    - Booleans, enums, ints or any other type of argument that is used to select the behavior of the function. 
    - In general it is better to have many funcitons than to pass some code into a function to select the behavior.
- OBscured intent
    - Code needs to be as expressive as possible.
- Misplaced responsibility
    - Where should the code be? Responsibility, performance etc.
- Inappropriate static
    - Sometimes functions  or other calls can be polymorphic instead of static.
- Use explanatory variables
- Function names should say what they do
- Understand the algorithm
- Make logical dependencies physical
- Prefer polymorphism to if else or switch case
    - "There may be no more than one switch statement for a given type of selection. The cases in that switch statement must create polymophic objects that take the place of other such switch statements in the rest of the system"
- Follow standard conventions
    - Based on industry norms.
- replace magice numbers with Named constants
- Be precise
- Structure over convention
- Encapsulate Conditionals
    - Extract functions that explain the intent of the conditional. If else statements if(shouldbeDeleted(timer)) instead of if(timer.hasExpired() && !timer,isRecurrent())
- Avoud negative conditionals
    - Conditionals should be expressed as positives.
- Functions should do one thing
- Hidden temporal couplings
    - More research is needed for this
- Dont be arbitrary
    - Have a reason for the way you structure your code.
- Encapsulate boundary conditions
    - Hard to track boundary conditions. Keep them in one place.
- Functions should descend only one level of abstraction
- Keep configurable data at high levels
- Avoid transitive navigation
    - The law of demeter.
    - Modules need to only know their direct collaborators.