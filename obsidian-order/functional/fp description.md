# functional programming - definition
Functional Programming: In contrast, functional programming is a form of declarative programming. You tell the computer what you want done by calling a method or function.

Functional Programming: Another principle of functional programming is to always declare your dependencies explicitly. This means if a function depends on a variable or object being present, then pass that variable or object directly into the function as an argument.

 Functional programming: The imperative style revolves around writing the instructions (statements).

Functional programming, on the other hand, is about describing our data.
***
Before starting, let me first introduce you to the main feature of Haskell, because of which Monads are needed in the very first place — Functional Programming. Functional Programming is a mindset where all design is just thought of in terms of pure functions.

-   Functions are first-class citizens. So, all simple logic is a function and all complex logic is handled by doing operations between functions.
-   Functions have to be pure. This means whatever input you give, the output should always remain the same. The only way to interact with pure functions is via input and output only. It cannot access global states or cannot print anything or cannot even throw exceptions until defined in the function definition.
***
In summary, there are three main reasons why functional languages do not need special-purpose `for` and `while` loop constructs. First, functional programming languages treat everything as an expression, whereas `for` and `while` loops are statements and not expressions. Second, functions, when defined in terms of themselves, are enough to formulate repeated computations. Finally, functional languages support tail-recursion optimization. This means a tail-recursive function uses a similar amount of memory as an equivalent loop and hence does not cause stack overflow problems.
***

#functional-programming #fp

