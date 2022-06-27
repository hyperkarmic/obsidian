# partial application
## What is Partial Application?

_Partial Application_ is having a function with a certain number of parameters, and fixing the values of some of them, so you are left with a function with fewer parameters. Just so you know if you happen to come into it, the “official” name for the process of fixing some parameters and producing a function of the unfixed ones is called _projection_; you would have _projected_ the original function onto the three unfixed parameters.
***
-   partial application depends on functions having a known number of parameters; it won’t work with functions that receive an undefined number of arguments. This said, you could implement a workaround by modifying `partialByClosure()` so if the original function doesn’t have a fixed number of arguments, as soon as there are no `__` arguments present, it could produce a result. I’ll leave the change up to you!
-   partial application, as we have it, is meant for functions, not methods. If need be, you could first transform the method into a function (as we saw in [a previous article](https://blog.openreplay.com/forever-functional-from-methods-to-functions-and-back)), and then there would be no further problems


***


#partial-application #functions #functional #fp 