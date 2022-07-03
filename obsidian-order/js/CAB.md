# call()
#### **Call** is a function that helps you change the context of the invoking function. In layperson's terms, it helps you replace the value of `this` inside a function with whatever value you want.
<hr>
# apply()
**Apply** is very similar to the `call` function. The only difference is that in `apply` you can pass an array as an argument list.
<hr>
# bind()
**Bind** is a function that helps you create another function that you can execute later with the new context of `this` that is provided.

The `bind` function creates a copy of a function with a new value to the `this` present inside the calling function.

The `bind` function then returns a new function that consists of a new context to the `this` variable present inside the calling function:
<hr>
###### Call, apply, and bind are the functions that help you change the context of the `this` keyword present inside the invoking function.
***

# The Explicit Binding

With the usage of `call`, `apply` or `bind` we tell the JavaScript engine to set `this` to point to a certain value.

`Call` and `apply` can be used to invoke a function with a specific value for `this`.
***
Both `call` and `apply` do the same. The first argument to both should be what `this` points to.

A difference comes up if additional arguments need to be passed to the invoked function.

With `call`, the additional arguments are passed as a normal comma-separated list of arguments, and with `apply` as an array of arguments.

With `bind` we create a new function and bind it to `this` permanently.
***

#js #javascript #call #apply #bind
