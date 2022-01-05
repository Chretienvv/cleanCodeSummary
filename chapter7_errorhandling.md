# Clean code chapter 7 error handling

## Tips & Learnings
- Error handling is important but if it obscures logic, its wrong.
- Use exceptions (try catch blocks) instead of error codes.
- Write your try catch finally statement first. 
    - try to write test that forces exceptions.
- Use unchecked exceptions.
    - Watchout for low level functions that push up the error message to the higher level functions. This violates open closed principle.
- Provide context to the error messages.
- Wrapping third party apis is best practices. 
- Seperate error handling class can be usefull.
- Seperation between business and error handling logic is important.
- Special case pattern - interesting to dive into
- Dont return and pass null

## Own Opinion
The concept of error handling is good to have. I think it is difficult to seperate it with the business logic. In the future I will try and focus on that part more in the future. This increases the readability as well. 