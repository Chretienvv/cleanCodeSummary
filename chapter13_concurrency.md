# Clean code chapter 13 Concurrency

## Tips & Learnings
- concurrent programming
    - Concurrent computing is a form of computing in which several computations are executed concurrently—during overlapping time periods—instead of sequentially—with one completing before the next starts.
    - Concurrency is a decoupling strategy
        - helps decoupling what gets done from when it gets done 

- Myths and misconceptions about concurrency
    - Concurrency always improves performance
        - It only does improves somtimes when there is a lot of waiting time. 
    - Design does not change when writing concurrent programs.
        - Not true, the decopling of what from when usually has a huge effect on the structure of the system.
    - Understanding concurrency issues is not important when working with a container such as a web or ejb container. 
    - Concurrency incures some overhead, both in performance as well as writing additional code.
    - Correct concurrency is complex, even for simple problems.
    - Concurrency bugs arent usually repeatable, so they are often ignored as one-offs instead of the true defects they are.
    - Concurrency often requires a fundamental change in design strategy.

- Concurrency Defense principles
    - SRP
        - Keep your concurrency related code separate from other code
    - Corollary: Limit the scope of data
        - Take data encapsulation to heart; severely limit the acces of any data that may be shared
    - Corollary: Use copies of data
    - Corollary: Threads should be as independent as possible
        - Attempt to partition data into independent subsets than can be operated on by independent threads, possibly in different processors.

- Execution models:
    - Bound resources
        - Definition: Resources of a fixed size or number used in a concurrent environment. Examples include database connections and fixed-size/read write buffers.
    - Mutual exclusion
        - Definition: Only one thread can access shared data or a shared resource at a time.
    - Starvation
        - Definition: One thread or a groupd of threads is prohibited from proceeding for an excessivly long time or forever. For example always letting fast running threads through first could starve out longer running threads if there is no end to the fast running threads.
    - Deadlock
        - Definition: Two or more threads waiting for each other to finish. Each thread has a resource that the other thread requires and neither can finish until it gets the other resource.
    - Livelock
        - Definition: Threads in lockstep, each trying to do work but finding another in the way. Due to resonance threads continue trying to make progress but are unable to for an excessivly long time.

- Beware Dependencies between synchronized methods
    - Avoid using more than one method on a shared object.
    - Solutions:
        - Client based locking
        - Server based locking
        - Adapted server

- Writing correct shut down code is hard. 
    - Recommendation: Think about shut down early and get it working early. It is going to take longer than you expect. Review existing algorithmes because this is probably harder than you think.
- Testing threaded code
    - Recommendation: Write tests that have the potential to expose problems and then run them freaquently. 
- Treat spurious failures as candidate threading issues
    - Recommendation: Do not ignore system failures as one-offs
- Get your nonthreaded code working first
    - Do not try to chase down nonthreading bugs and threading bugs at the same time. Make sure your code works outside of threads.
- Make your threaded code pluggable
- Make your threaded code tunable.
- Run on different platforms

## Own Opinion
n.v.t.