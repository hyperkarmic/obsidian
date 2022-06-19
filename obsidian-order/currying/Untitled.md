# currying
## [Currying](https://en.wikipedia.org/wiki/Currying) is a technique that lets you work with unary functions -that is, functions with just a single parameter- even if you need functions with multiple parameters. Why would we need this? The method has do with theoretical considerations, because it allows us to work with a single type of functions, making logical analysis rather easier. This was invented back in the 19th Century, and later worked on by Moses Schönfinkel, a Russian logician, but the technique gets its name from Haskell Curry. (Yes, the same person whose name is a functional programming language!)

-   currying works only with functions with a known, fixed number of parameters; it won’t work with functions that can receive an undefined number of arguments.
-   currying applies to functions, not methods. If you want to curry methods such as `.map()` or `.filter()`, you could always first transform the method into a function (as we saw in [a previous article](https://blog.openreplay.com/forever-functional-from-methods-to-functions-and-back)) and then everything would be fine.

#currying
