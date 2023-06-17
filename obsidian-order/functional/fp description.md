# functional programming - definition
(aka Declarative Programming`)
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
## Characteristics of declarative (functional) programming

-   You declare what you want to happen, not how it’s done.
-   There are no loops or conditional statements (for a set-based language, like SQL, where you think of data in columns instead of in rows).
-   There are plenty of filters and operations on the data as a whole, but the data is often considered immutable values (not changeable).
***
# Overview of Functional Programming

-   Closures
-   First class functions
-   Lambdas

## What is functional programming?

Functional programming basically means writing code that _does_ something (declares what is done) but isn’t specific about how to do it (imperative).

One of the largest benefits of functional programming for me that it helps separate **mutable _variables_** from **non-mutable _constants_.**

I like being able to keep straight what I should mess with (variables) and what I should leave alone (constants) in my code. It’s a personal preference.

## What are first class functions and lambdas?

Functions are first-class objects in JavaScript, meaning they can be:

-   stored in an array, variable, or object
-   passed as one of the arguments to another function
-   returned from another function

## Lambdas make code more succinct

function (x) { return x * x };

Compared to the traditional function declaration above, a lambda removes the _function_ and _return_ keywords. That makes these expressions succinct.

range(1, 7).map(x => x * x); //-> [1, 4, 9, 16, 25, 36, 49]

Lambdas in JavaScript are usually called by “fat-arrow” functions:

var square = x => x * x;  
square(7); // 49

Lambda expressions are sometimes known as blocks or closures.

## What the heck is a closure?

Whenever you declare a new function and assign it to a variable, you store the function definition, as well as a closure.

The closure contains all the variables that are in scope at the time that the function definition is created. That lexical scope is maintained.

[Closures are analogous to a backpack](https://medium.com/dailyjs/i-never-understood-javascript-closures-9663703368e8). It’s like functions come with little backpacks, and in that pack are all the variables that were in scope.
***
Functional programming glossaries contain a large number of large words, but at its core, the essence of FP is really very simple; programs are built mostly with a handful of very small, very reusable, very predictable **pure functions.**

Pure functions have a few properties that make them extremely reusable and extremely useful for a variety of applications:

**Idempotence:** Given the same inputs, a pure function will always return the same output, regardless of the number of times the function is called. You may have heard this word used to describe HTTP GET requests. **Idempotence is an important feature for building RESTful web services,** but it also serves the very useful purpose of separating computation from dependency on both time and order of operations — **extremely valuable for parallel & distributed computation** (think horizontal scaling).

Because of idempotence, pure functions are also a great fit when you need to operate on continuous data sets. For instance, automated fade-ins and fade-outs in video or audio. Typically they’re designed as linear or logarithmic curves independent of framerates or sample rates, and only applied at the last possible moment to produce discrete data values. In graphics, this is analogous to scalable vector images like SVG, fonts, and Adobe Illustrator files. Key frames or control points are laid out relative to each other or to a timeline, rather than keyed to fixed pixels, frames, or samples.

Because idempotent functions don’t have any dependency on time or sample resolution, it’s possible to treat continuous data as unbounded (virtually infinite) data streams, which allows free scaling of data across time, (sampling rates), pixel resolution, audio volume, and so on.

**Free from Side-effects:** Pure functions can be safely applied with no side-effects, meaning that they do not mutate any shared state or mutable arguments, and other than their return value, they don’t produce any observable output, including thrown exceptions, triggered events, I/O devices, network, console, display, logs, etc...

Because of the lack of shared state and side-effects, pure functions are much less likely to conflict with each other or cause bugs in unrelated parts of the program.

In other words, for the OOP coding audience, **pure functions produce stronger guarantees of encapsulation than objects without function purity,** and those guarantees provide many of the same benefits as encapsulation in OOP: The ability to change implementation without impacting the rest of the program, a self-documenting public interface (the function signature), independence from outside code, the ability to move code around freely between files, modules, projects, and so on.
***
# Why Functional Programming

-   Its pure function, provides confidence of not changing things outside of its scope.
-   Its reduces the complexity, need not to worry about how it is doing it, focus will be only on what it is doing.
-   Ease of testing, because it does not depend on state of the application and result verification also will be easy.
-   It makes the code more readable.
-   Functional programming makes code easier to understand.
***

#functional-programming #fp

