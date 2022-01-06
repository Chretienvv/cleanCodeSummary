# Clean code chapter 9 Unit tests

## Tips & Learnings
- The three laws of Test driven development (TDD)
    - You may not write production code until you have written a failing unit test
    - You may not write more of a nunit test than is sufficient to fail and not compiling is failing.
    - You may not write more production code that is sufficient to pass the currently failing test.

- Keeping tests clean
    - Test functions are short and descriptive
    - Tests need to change when the production code changes. So maintainability is important.
    - Test code is just as important as production code. 

- Tests keep our production code flexible, maintainable and reusable. (tests enable change)
- Clean tests are readable
    - Clarity, simplicity and density of expression

- Build-operate- check pattern
    - The first step is to build the input data and hold it in memory, then execute it on the actual code which means call/invoke the code to operate on that data. Finally check the results of that operation.

- Given when then convention
    - GivenPages() whenRequestIsIssued() thenREsponseShouldBeXML()

- template Method pattern
    - Template Method is a behavioral design pattern that defines the skeleton of an algorithm in the superclass but lets subclasses override specific steps of the algorithm without changing its structure.

- Preferable use one assert per test. 
- Single concept per test

- FIRST <- tests should follow these rules.
    - Fast: Tests should be fast
    - Independent: Tests should not depend on each other.
    - Repeatable: Tests should be repeatable in any environment
    - Self validating: Tests should have a bollean output
    - Timely: The tests need to be written in a timely fashion. Just before the production code. 

## Own Opinion
Tests are equally important as the production code. It enables maintainability and flexibility.  TDD is something that is a must and there need to be time created for it to properly approach it as a team. It is not a second class citizen. 
