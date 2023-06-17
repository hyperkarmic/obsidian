# composition
## Composition

-   Composition involves combining several small (often pure) functions together
-   This can be done by chaining methods together using the dot notation or passing the output from one function to the next
***

## Composition

Inheritance is a powerful mechanism to extend entities but not every problem can fit into its mental model. Forcing the design of a solution with inheritance can lead to more complex and hard to maintain implementations.

Composition is an alternative approach that lets us put larger, more complex objects together by combining multiple small ones.
***
Compose, on the other hand, is a way to combine multiple functions such that the output of one function is passed as the input to the next, but with the functions being composed in the opposite order. In other words, the functions are executed from right to left instead of left to right.
***
Both pipe and compose can be used to make code more readable and maintainable by breaking down complex operations into smaller, more focused functions that can be easily reused and tested. They also allow you to more easily change or modify the behavior of your code by modifying or replacing individual functions within the pipe or compose chain.
***
In addition to using the Array.prototype.reduce() method to implement pipe and compose, you can also use other techniques such as recursion or a simple loop. The choice of implementation will depend on your needs and preferences, and may also be influenced by performance considerations.
***
![[compose-FP.jpg]]
***
![[composition.jpg]]
#CI #composition #fp #functional