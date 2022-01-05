# Clean code chapter 6 objects and data structures

## Tips & Learnings
- Data abstraction
    - Make everything private by default and change it when it is needed.
    - This hides the implementation
    - Do not expose the detail of your data. 
    - Watchout for adding getters and setters
- Objects: hide their data behind abstractions and expose functions that operate on that data.
    - Expose behavior and hide data
- Data structure: expose their data and have no meaningful functions.
    - Data structures expose data and have no significant behavior
- Procedural code (code using data structures )makes it easy to add new functions without chaning the existing data structures. 
- OO code makes it easy to add new classes without changing existing functions.
- The law of demeter: A module should not know about the innards of the objects it manipulates.
    - Methods should not invoke methods on objects that are returned by any of the allowed functions. 
    - Train wreck:
        - final string outputDir = ctxt.getOptions().getScratchDir(). getAbsolutePath()

## Own Opinion
Very good to see the difference between objects and data structures. This has effect on for instance the law of demeter. I will try to implement this in my code. 
