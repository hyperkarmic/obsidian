#  Programming Interviews Exposed - John Mongan
### Parker Klein Notes
-   Are you a systems programmer or an application developer?
    
-   Do you like coding user interfaces?
    
-   Do you like debugging?
    
-   Do you like testing?
    
-   Are you an architect or a coder?
    
-   Initial screening with a company recruiter: they want to make sure you are interested in the open position, that you have the skills needed, that you are willing to accept logistical requirements
    
-   When you decline an offer, be sure to thank everyone you came into contact with and let them know your decision
    
-   Most questions are hard and are designed to take up to an hour to solve, don't get frustrated if you don't see the answer right away
    
-   Many problems require algorithmic tricks or uncommonly used features of a language
    
-   Most problems prohib you from using the most common way to do something or from using the ideal data structures
    
-   The ability to work within the particular constraints of a situation is an important skill too develop
    
-   The interviewer wants to hear your thought process throughout the interview
    
-   Showing an intelligent thought process and responding well to hints is also important
    
-   Break the answer down into discrete steps and explain the thought process behind each step
    
-   Keep talking, but talk slow
    
-   Basic steps to solving the problem: 1. make sure you understand the problem: don't make assumptions, ask questions about the problems 2. when you understand the problem, try a simple example: it will bring insight of how to solve the general problem and will uncover any misunderstandings 3. focus on the algorithm and data structures you will be using to solve the problem: don't start coding until you fully understand the problem and how you will approach it, think long and hard 4. explain your solution after you figure out algorithm and how to implement it 5. while you code, explain what you are doing: helps them follow your code more easily 6. ask questions when necessary: you won't be penalized for asking factual question you might otherwise look up 7. after you write the code, verify it by tracing through it with an example: demonstrates working code and your intention to check your work and search for bugs 8. check your work for all error and special cases, especially boundary conditions
    
-   When you get stuck, show interest in the problem and keep trying to solve it. Go back to an example: try performing the task and analyzing what you are doing, show persistence in finding the correct solution. Try a different data structure. Consider less commonly used and more advanced aspects of a language
    
-   Big-O analysis is runtime analysis that measures efficiency of an algorithm in terms of the time it runs as a function of the input size
    
-   General procedure for Big-O runtime analysis: 1. figure out what the input is and what n represents 2. express the number of operations the algorithm performs in terms of n 3. eliminate all but the highest-order terms 4. remove all constant factors
    
-   Memory footprint: determine the amount of storage required for each item
    
-   Linked lists are great for handling dynamic data
    
-   When traversing a linked list, you must always check that you haven't reached the end of the list
    
-   For larger projects, good planning and design is essential to success
    
-   Identify special cases by considering what circumstances are likely to lead to special cases being invoked. It's important to identify special cases while coding
    
-   Debugging: systematic analysis of every line of the function. 1. check that data comes into the function properly 2. check that each line of the function works correctly 3. check that the data comes out of the function correctly 4. check the common error conditions
    
-   A tree is made up of nodes with zero, one, or several references to other nodes
    
-   Root: top-level node with path to every other node
    
-   Binary tree: each node has no more than two children, left and right
    
-   When an interviewer says tree, they often mean a binary tree
    
-   Binary search tree (BST): most common way to store ordered data in a tree. Left is less than or equal to its value, right is greater than or equal to its value
    
-   Max-heap: each child of a node has a value less than or equal to the node's own value, find largest value in constant time
    
-   Min-heap: each child is greater than or equal to its parent
    
-   The height of a tree equals the height of its tallest subtree plus one
    
-   Recursive algorithms can be replaced with iterative algorithms that accomplish the same task in a fundamentally different manner using different data structures
    
-   Recursion implicitly uses a stack data structure by placing data on the call stack
    
-   In an abstract sense, a string is just an array of characteristics
    
-   An array is a sequence of variables arranged continuously in a block of memory
    
-   Many array and string problems require the use of additional temporary data structures to achieve the most efficient solutions
    
-   Recursion is useful for tasks that can be defined in terms of similar subtasks
    
-   Recursive algorithms have two cases: recursive cases and base cases
    
-   Tail recursive: the value returned by the recursive call is itself immediately returned
    
-   It may be useful to write a separate wrapper function to do initialization for a complex recursive function
    
-   Recursive calls create a large overhead
    
-   Iterative solutions are usually more efficient than recursive solutions
    
-   It's always possible to implement a recursive algorithm without using recursive calls
    
-   Useful for data presentation and optimizing algorithms by sorting input data or sorting as the algorithm runs
    
-   Most sorting algorithms are comparison algorithms
    
-   A class is an abstract definition of something that has attributes and actions
    
-   An object is a specific instance of a class
    
-   Encapsulation: the hiding of implementation details
    
-   Inheritance: allows a class to be defined as a modified or more specialized version of another class
    
-   An interface declares a set of related methods, outside of any class
    
-   Design patterns are abstract providing recommendations on how to solve specific kinds of programming problems. They help solve common software design problems based on the collected wisdom of many develops
    
-   3 basic categories: creational, behavioral, structural
    
-   Creational patterns manage class select and object creation. Rather than creating objects directly, it may be advantageous for code to delegate object creation to other parts of an application, or to restrict how object instances can be created and accessed
    
-   Singleton: ensures that at most one instance of a class exists at a given time
    
-   Builder: creates objects in a stepwise manner without knowing or caring how those objects are constructed
    
-   Factory method: any method whose privacy purpose is to create and return a new object
    
-   Abstract factory: separates the factory implementation from the code that uses the factory
    
-   Behavioral patterns: determine how classes and objects interact and communicate
    
-   Structural patterns: organize relationships between classes and objects, providing guidelines for combining and using related objects together to achieve designed behaviors
#Mongan
#programming #interviews #interview #classic-code 