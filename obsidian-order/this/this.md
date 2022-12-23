# this

-   In a method, `this` refers to the **owner object**.
- #### When you create an object of a function using new keyword then `this` will point to that particular object
- .  When used alone, `this` refers to the **global object**.
-   In a function, `this` refers to the **global object**.
- #### When a function includes `this` keyword and is called from the global scope then `this` will point to the window object.
- In a function, in strict mode, `this` is `undefined`.
-   In an event, `this` refers to the **element** that received the event.
-   Methods like `call()`, and `apply()` can refer `this` to **any object**.
- #### The main purpose of call() and apply() is to set the context of `this` inside a function irrespective whether that function is being called in the global scope or as object's method.
***
This keyword:Is a context object!!!!
****
## This: What is **this**?The JavaScript `this` keyword refers to the object it belongs to.
***

**This:** The `this` keyword refers to an object so that you can access the properties within an object. It can also be used to set the value of a property within an object.
***
![[TDD/this'.png]]
***
![[TDD/this2.png]]
***
![[TDD/this3.png]]
***
**This has five scenarios:**

(1) The binding event points to the event itself

(2) Ordinary function, pointing to the method body

(3) The new function points to the current class

(4) Arrow function, pointing to the parent context

(5) call/apply/bind
***
# What is “`this`”?

When a function is called, an execution environment will be created. `this` is bound at runtime based on the execution environment of the function. It allows functions to reference execution variables in the context internally, making function programming more elegant and concise.
***
![[this-chart.png]]
***
The default binding rules are as follows:

1.  **Global function the** `**this**` **points to the** `**Window**`

When printing `this` directly in the global function, you can see that `this` points to `Window`.

**2. Independent function calls the**`**this**` **point to the** `**Window**`

Independent function calls, that is, direct calls to functions, such as `foo()`

**3. For self-executing function calls,** `**this**` **points to** `**window**`
4. **The** `**this**` **inside the closure points to the** `**Window**`
***
## Implicit binding

When a function is called as a method,`this` points to the direct parent object of the function, which is called implicit binding.

In the implicit binding rule, it is believed that `this` points to whoever called the function, and will point to the function’s immediate parent object.
***
**Implicit binding lost**

Implicit binding loss means that the implicitly bound function loses its binding object, so it is bound to `Window` by default. This method is easy to cause errors in our projects, but it is also common.


1.  **Implicitly bound functions are assigned as variables without** `**this**` **pointing.


2. **The implicitly bound function is passed to the function as a parameter, and the** `**this**` **point is lost.**

When an implicitly bound function is directly passed to another function as a parameter, the `this` binding will be lost, thus pointing to the global `Window`.

**3. Implicit binding of functions in built-in objects** `**setTimeout**` **and** `**setInterval**` **is lost**

The `this` of built-in functions `setTimeout` and `setInterval` points to `Window` by default.

***
## Explicit binding

When we want to bind the function to the specified object, we can use `call`, `apply`, `bind` and other methods to manually change the `this` direction, that is, explicit binding.
***
Let’s sum it up. The binding principles of `this` were as follows:

1.  Default binding, `this` pointed to the global `Window`.
2.  The one who called `this` would point to him. Don’t forget the loss of the hidden binding.
3.  It showed the bind. He changed this direction by using `call`, `apply` and `bind`.
4.  `new` binding, an instance of the construction `new`, and `this` pointing to the instance object of `new`.
***
![[this.jpg]]
. #this
