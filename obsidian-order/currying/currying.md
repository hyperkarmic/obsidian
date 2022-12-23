# currying
## [Currying](https://en.wikipedia.org/wiki/Currying) is a technique that lets you work with unary functions -that is, functions with just a single parameter- even if you need functions with multiple parameters. Why would we need this? The method has do with theoretical considerations, because it allows us to work with a single type of functions, making logical analysis rather easier. This was invented back in the 19th Century, and later worked on by Moses Schönfinkel, a Russian logician, but the technique gets its name from Haskell Curry. (Yes, the same person whose name is a functional programming language!)

-   currying works only with functions with a known, fixed number of parameters; it won’t work with functions that can receive an undefined number of arguments.
-   currying applies to functions, not methods. If you want to curry methods such as `.map()` or `.filter()`, you could always first transform the method into a function (as we saw in [a previous article](https://blog.openreplay.com/forever-functional-from-methods-to-functions-and-back)) and then everything would be fine.
<hr>
Curry: Currying a function is breaking it down into smaller functions which each takes one of the arguments.Currying a function is breaking it down into smaller functions which each takes one of the arguments._

  

_Curryiing:_ _Currying is basically all about_ _[Higher Order Functions](https://dev.to/kozlovzxc/js-interview-in-2-minutes-higher-order-functions-38kb)__. It is an application of JavaScript's ability to return functions from other functions._

We are replacing a function that takes `n` arguments with a set of `n` functions, which applied one by one gives exactly the same answer as original functions.
***
Currying: _In mathematics and computer science,_ **_**currying is the technique of converting a function that takes multiple arguments into a sequence of functions that each take a single argument**_**_._
***
Currying is a transformation technique in the javascript functions. The currying is a function that takes one argument at a time and returns a new function.

Basically currying is a transformation of taking multiple parameters at a time taking arguments sequentially and returning a new function, the next function takes another argument and continues the flow like that.
***
# Currying

It is a method to transform the function with multiple arguments into several functions of a single argument in a sequence.

In simple words, a function instead of taking all arguments one at a time takes the first one and returns a new function that takes the second one and then returns a new function that takes the third one, and this process keeps going until all arguments have been fulfilled.
***


#currying
 #hof
 #curry 
 #functional-programming
 
 