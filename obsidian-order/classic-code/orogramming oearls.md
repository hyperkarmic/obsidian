# Programming Pearls - John Bentley
### Parker Klein Notes
-   Careful analysis of a small problem can sometimes yield tremendous practical benefits
    
-   Focus on the right problem: defining the problem is 90% of the battle
    
-   Bitmap data structure: this data structure represents a dense set over a finite domain when element occurs at most once and no other data is associated with the element
    
-   A time-space tradeoff: by using more time, a program can run in less space, tradeoffs are common to all engineering disciplines
    
-   Simple design: a designer knows he has arrived at perfection not when there is no longer anything to add, but when there is no longer anything to take away
    
-   Simple programs are more reliable, secure, robust, efficient and are easier to build and maintain
    
-   A problem that seems difficult may have a simple, unexpected solution
    
-   Problem definition: determining what the user really wants to do is an essential part of programming
    
-   What primitives will we use to solve the problem?
    
-   What new basic operation will make the problem trivial?
    
-   A problem solver's perspective: be a bit lazy. Sit back and wait for an insight before rushing forward with your first idea
    
-   Judgment comes only with the experience of solving problems and reflecting on their solutions
    
-   You can make programs smaller and better by restructuring their initial data
    
-   The programmer at wits end for lack of space can often do best by disentangling himself for his code, rearing back, and contemplating his data
    
-   Encapsulate complex structures
    
-   When you read a sophisticated data structure, define it in abstract terms, and express those operations in a class
    
-   Let the data structure the program
    
-   Before writing code, good programmers thoroughly understand the input, the output and the intermediate data structures around which their programs are built
    
-   Correctness has 3 parts: initalization, preservation, termination
    
-   Assertions allow a programmer to enunciate the relations between input, program variables, and output, which describe the 'state' of a program, precisely
    
-   Functions: programs by contract. Precondition: the state that must be true before it is called. Postcondition: what is guaranteed on termination
    
-   Verify code correctness by executing the program by hand on one input
    
-   Understand the code at all times and resist those foul urges to 'just change it until it works'
    
-   Assertions are crucial for maintaining a program and can give invaluable insight about the program state
    
-   Keeping the code simple is usually the key to correctness
    
-   An assert is used to state a belief about an expression and will raise an error if it is not true
    
-   Correct code: walkthrough manually with input and check for output, use assertions throughout the code, use automated testing, check runtime with simple experiments
    
-   Coding: sketch a hard function in a convenient high-level pseudocode, then translate it into the implementation language
    
-   There has to be a logical explanation, no matter how mysterious the system's behavior may seem
    
-   Programmer's ultimate goal: a simple, powerful program that delights its users and does not vex its builders
    
-   Performance improvements: algorithms and data structures, algorithm tuning, data structure reorganization, code tuning, hardware
    
-   Decompose a large system into modules
    
-   The importance of simple design can't be overemphasized
    
-   Dynamic programming: save state to avoid recomputation
    
-   Preprocess information into data structures
    
-   Use divide-and-conquer algorithms
    
-   Cumulatives: use cumulative tables
    
-   Code tuning: locating expensive parts of an existing program and make little changes to improve its speed
    
-   Caching: data accessed most often should be the cheapest to access
    
-   Premature optimization is the root of much programming evil
    
-   Less data to manipulate usually means less time to manipulate it
    
-   Don't store, recompute
    
-   Store, don't retransmit over the network
    
-   Dynamic allocation: only allocating space when it is needed
    
-   Problem-solving: 1. understand the perceived problem 2. specify an abstract problem 3. explore the design space 4. implement one solution 5. retrospect
    
-   The purpose of software engineering is to control complexity, not create it
    
-   Design problem suggestions: 1. work on the right problem 2. look at the data 3. design with components 4. strive for elegance

#programming
#pearls
#bentlley
